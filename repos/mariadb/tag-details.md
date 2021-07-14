<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.39`](#mariadb10239)
-	[`mariadb:10.2.39-bionic`](#mariadb10239-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.30`](#mariadb10330)
-	[`mariadb:10.3.30-focal`](#mariadb10330-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.20`](#mariadb10420)
-	[`mariadb:10.4.20-focal`](#mariadb10420-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.11`](#mariadb10511)
-	[`mariadb:10.5.11-focal`](#mariadb10511-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.3`](#mariadb1063)
-	[`mariadb:10.6.3-focal`](#mariadb1063-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:04125527f956147e18df069b9e58064f03eb6c2b2dd3cdbe3ed3caa2dafbfcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:239e4679d65d9a44c983072b52312f8cbfaf505a805090aa97d1a65266c82669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124305174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5769943918c67f6492a009979e758470c83b2de2a83d1716402f1d4009b78479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:40:54 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:40:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:17 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:18 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44c338f719da6a7548fc4e647b9bd52225c5df3e2302badd4a3636d4ada6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0477462ca83c7a80d659335ac0c0d7eadd33db5bf3497027907f7c417dd036c5`  
		Last Modified: Tue, 13 Jul 2021 23:45:32 GMT  
		Size: 86.1 MB (86099760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af6cce3f74250abc9bdff500887dc7967e9af3afde38f6d863fde77572ed62`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e83376a3a79780723ee2f77623bca0817d59cac7d5edd216700e596ab9344b2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137504069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483574e8cdb21e02f00261a7f79687f57f662824805f3a9b2c2d43e35ebf08a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:26:26 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:36 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:41 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:31:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:32:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:32:16 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:27 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:32:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fef03d4d8ec5fdbff5a48b3b0bd2e4b89871abaea39af1025a6c3c13bc5a05`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99414d7cf31143b328d34986107ab9144e1e311e6bae8d5686c17b2a8faa43`  
		Last Modified: Tue, 13 Jul 2021 19:04:55 GMT  
		Size: 91.3 MB (91306505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704b6e12ccce455e8980f637eee2cc9c2dc93e364a9dc504ed7d1073f107f7d2`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:04125527f956147e18df069b9e58064f03eb6c2b2dd3cdbe3ed3caa2dafbfcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:239e4679d65d9a44c983072b52312f8cbfaf505a805090aa97d1a65266c82669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124305174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5769943918c67f6492a009979e758470c83b2de2a83d1716402f1d4009b78479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:40:54 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:40:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:17 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:18 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44c338f719da6a7548fc4e647b9bd52225c5df3e2302badd4a3636d4ada6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0477462ca83c7a80d659335ac0c0d7eadd33db5bf3497027907f7c417dd036c5`  
		Last Modified: Tue, 13 Jul 2021 23:45:32 GMT  
		Size: 86.1 MB (86099760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af6cce3f74250abc9bdff500887dc7967e9af3afde38f6d863fde77572ed62`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e83376a3a79780723ee2f77623bca0817d59cac7d5edd216700e596ab9344b2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137504069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483574e8cdb21e02f00261a7f79687f57f662824805f3a9b2c2d43e35ebf08a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:26:26 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:36 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:41 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:31:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:32:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:32:16 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:27 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:32:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fef03d4d8ec5fdbff5a48b3b0bd2e4b89871abaea39af1025a6c3c13bc5a05`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99414d7cf31143b328d34986107ab9144e1e311e6bae8d5686c17b2a8faa43`  
		Last Modified: Tue, 13 Jul 2021 19:04:55 GMT  
		Size: 91.3 MB (91306505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704b6e12ccce455e8980f637eee2cc9c2dc93e364a9dc504ed7d1073f107f7d2`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:3a56ade2bc086445696d6a7eee3098f256a686a2944b77d104ea3d42154058d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:5c0e9eb27ad2c186cb9b10d0310f3f30eeb5ecc09e9ecf36e432f782f570e9e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecaf9c767e5b4386e0943490478c267578da00339064a347064fdccabf6ac8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:59:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:59:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:59:41 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:59:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 01:00:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 01:00:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:00:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 01:00:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 01:00:23 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:26 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:28 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:30 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 01:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 01:01:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 01:01:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 01:01:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 01:01:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 01:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 01:01:38 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 01:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f3767f093ff77f35d70e64fabf43d7e4f3328f83e55442f0496a755cc4d64b`  
		Last Modified: Wed, 14 Jul 2021 01:05:30 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f57ce2f183ce7276382d0923cc09ec6d5b032340a6e77fae51524c3d53e1cd`  
		Last Modified: Wed, 14 Jul 2021 01:05:29 GMT  
		Size: 4.8 MB (4813397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72574b5b8e280c2c544716ac987bb628a29dffddf0b834fe1f49ac5cc597e668`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 3.5 MB (3547597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b95e8526938e2cfe043471fa153a469217921fefd07794dc79b692a9ec070`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73bc88eeea165da977334c6a9b104bab922ac53ee71c974a3a2d24cd323e8e6`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 1.6 MB (1585899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fbed1b6870267362f5204259d106fb13d92c0573c9f16e4e151ccf98b2035`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1976b29470905458e13aab07a8c0662107ea44f4f2be580aaa7f05409390f96`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ec62c50c2339447743375b73310b58b3553a584c23819c8a8a6b750e6d0ae0`  
		Last Modified: Wed, 14 Jul 2021 01:05:37 GMT  
		Size: 72.6 MB (72638596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f53eb6cd79a22c0ea3ee1450aba9c8eadd87915610aed9b86159e1acd565be`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b9776cfa8c66e0b0996411fda717994fd2616e335532df5e6150a2a528cd5`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ed44fdfac14863449badc323af635fd968773eff787cb9894976d77582574d96
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104312483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c34c41db269abbf10ab0ed9b5934db68369fe8769012172e052cf52a6dc8a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:09 GMT
ADD file:f5aca23bd8c77beda7e17bb71fc4df34d91662b6179de87029f24d21b9e799ad in / 
# Tue, 13 Jul 2021 23:01:09 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:43:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:43:22 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:43:23 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:43:37 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:43:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:43:46 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:43:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:43:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:43:48 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 23:43:48 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 23:43:48 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 23:43:49 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 23:43:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Tue, 13 Jul 2021 23:43:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:44:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:44:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:44:15 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:44:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:44:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:44:17 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:44:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b9bb7af7248f30dd1b1f9807608f5f532133384e4db55caa6dbc69b9cf15ddcc`  
		Last Modified: Tue, 13 Jul 2021 23:03:17 GMT  
		Size: 23.7 MB (23729498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502273c3f4d3cca6957ee7ad312fccf2a58f474dd4470f4d57fd81c7ccbbad6f`  
		Last Modified: Tue, 13 Jul 2021 23:47:59 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec2b94cdaf1d8183985236813593ca75ec1a93fd8749766a671eed3cb5084a9`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 4.4 MB (4395559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235bbb8ac48487daf075dffd4eeb87748124db368791f39c6291097fd8087907`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 3.2 MB (3204623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab6f216bf65e3ea1463da1a6f3a0c8e6e9a218dccdc525833fd4522258f1d81`  
		Last Modified: Tue, 13 Jul 2021 23:47:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c19647916f33368a8ad9c2261897d199b6c7f12d2fc0c78c68c5e94afc1983`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 1.5 MB (1532405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d482ed8bb6a6891a996239552a67845de3dd3878f25bebaa82503aa8bc89d47`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a41688a5253433e744ebbe4627c25ab47b0385250213199257226e0cb70bfe`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143ff3d76f78be60926ec476578c670f933471a9fcf678dfb26104f87ec4248`  
		Last Modified: Tue, 13 Jul 2021 23:48:06 GMT  
		Size: 71.4 MB (71437154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66adf06926d7de93b5a38027e70481343436196027cc982871cd87684975c9`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48b2a34851fd54047498d82409a6366486970136fc7ce3151b38dd1e1a1a660`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a4c79ab4f05d4088c934e62b52f58c794e8c94e73a3dcfad5ded42252aa3df8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117628870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0361d567d7920a770863e8fade1d338b3edae167dd86259883e39141120cb2b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:51:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:52:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:53:02 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:53:53 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:54:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:55:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:55:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:56:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:56:14 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 18:56:22 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 18:56:29 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 18:56:38 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 18:56:48 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Tue, 13 Jul 2021 18:57:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 19:02:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 19:02:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 19:02:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 19:02:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 19:03:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 19:03:16 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 19:03:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f58409e900735b3af04414a2eac25dcf2479f264457522587a2d3b713cb1d54`  
		Last Modified: Tue, 13 Jul 2021 19:07:28 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0832199508426a244908601f7a3fafb898620be6f90658b526f29fcccc7ccf50`  
		Last Modified: Tue, 13 Jul 2021 19:07:28 GMT  
		Size: 5.6 MB (5630513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c69e1972a6436931f30c95a56fdfc15d48c27ac84d60eedeaf40742b613731`  
		Last Modified: Tue, 13 Jul 2021 19:07:27 GMT  
		Size: 3.5 MB (3528890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea947a3fe9cdc3598e8c581207c216fdb3ff0f0f363d6355e8c3b519679e925`  
		Last Modified: Tue, 13 Jul 2021 19:07:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb53ae5254fffcbc388441f70643e8e1f8d4012f20900d2f38c07ab4bf5092`  
		Last Modified: Tue, 13 Jul 2021 19:07:26 GMT  
		Size: 1.9 MB (1938748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e8ec4a32b9707ce15e0b2615457ebe1363cb69ac9fc661be956c391f800788`  
		Last Modified: Tue, 13 Jul 2021 19:07:24 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166205ee57ab5a5cc638447f66eb909d6180afdc0b8b91422bd6e505c2fa94e8`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f0c8ad70d2e4bc7211ce6bff737a24b294e38caac31b81400b9737a4c9665f`  
		Last Modified: Tue, 13 Jul 2021 19:07:39 GMT  
		Size: 76.1 MB (76092107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bb9b897fbedc49e30c200909402110b6f9216b784a0eee10f60f07718e071d`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96e91da134b7450e3adf4341191479190b484764c762c49f916f6ebb1b89931`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:3a56ade2bc086445696d6a7eee3098f256a686a2944b77d104ea3d42154058d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:5c0e9eb27ad2c186cb9b10d0310f3f30eeb5ecc09e9ecf36e432f782f570e9e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecaf9c767e5b4386e0943490478c267578da00339064a347064fdccabf6ac8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:59:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:59:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:59:41 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:59:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 01:00:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 01:00:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:00:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 01:00:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 01:00:23 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:26 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:28 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:30 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 01:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 01:01:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 01:01:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 01:01:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 01:01:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 01:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 01:01:38 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 01:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f3767f093ff77f35d70e64fabf43d7e4f3328f83e55442f0496a755cc4d64b`  
		Last Modified: Wed, 14 Jul 2021 01:05:30 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f57ce2f183ce7276382d0923cc09ec6d5b032340a6e77fae51524c3d53e1cd`  
		Last Modified: Wed, 14 Jul 2021 01:05:29 GMT  
		Size: 4.8 MB (4813397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72574b5b8e280c2c544716ac987bb628a29dffddf0b834fe1f49ac5cc597e668`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 3.5 MB (3547597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b95e8526938e2cfe043471fa153a469217921fefd07794dc79b692a9ec070`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73bc88eeea165da977334c6a9b104bab922ac53ee71c974a3a2d24cd323e8e6`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 1.6 MB (1585899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fbed1b6870267362f5204259d106fb13d92c0573c9f16e4e151ccf98b2035`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1976b29470905458e13aab07a8c0662107ea44f4f2be580aaa7f05409390f96`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ec62c50c2339447743375b73310b58b3553a584c23819c8a8a6b750e6d0ae0`  
		Last Modified: Wed, 14 Jul 2021 01:05:37 GMT  
		Size: 72.6 MB (72638596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f53eb6cd79a22c0ea3ee1450aba9c8eadd87915610aed9b86159e1acd565be`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b9776cfa8c66e0b0996411fda717994fd2616e335532df5e6150a2a528cd5`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ed44fdfac14863449badc323af635fd968773eff787cb9894976d77582574d96
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104312483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c34c41db269abbf10ab0ed9b5934db68369fe8769012172e052cf52a6dc8a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:09 GMT
ADD file:f5aca23bd8c77beda7e17bb71fc4df34d91662b6179de87029f24d21b9e799ad in / 
# Tue, 13 Jul 2021 23:01:09 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:43:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:43:22 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:43:23 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:43:37 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:43:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:43:46 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:43:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:43:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:43:48 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 23:43:48 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 23:43:48 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 23:43:49 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 23:43:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Tue, 13 Jul 2021 23:43:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:44:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:44:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:44:15 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:44:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:44:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:44:17 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:44:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b9bb7af7248f30dd1b1f9807608f5f532133384e4db55caa6dbc69b9cf15ddcc`  
		Last Modified: Tue, 13 Jul 2021 23:03:17 GMT  
		Size: 23.7 MB (23729498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502273c3f4d3cca6957ee7ad312fccf2a58f474dd4470f4d57fd81c7ccbbad6f`  
		Last Modified: Tue, 13 Jul 2021 23:47:59 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec2b94cdaf1d8183985236813593ca75ec1a93fd8749766a671eed3cb5084a9`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 4.4 MB (4395559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235bbb8ac48487daf075dffd4eeb87748124db368791f39c6291097fd8087907`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 3.2 MB (3204623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab6f216bf65e3ea1463da1a6f3a0c8e6e9a218dccdc525833fd4522258f1d81`  
		Last Modified: Tue, 13 Jul 2021 23:47:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c19647916f33368a8ad9c2261897d199b6c7f12d2fc0c78c68c5e94afc1983`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 1.5 MB (1532405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d482ed8bb6a6891a996239552a67845de3dd3878f25bebaa82503aa8bc89d47`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a41688a5253433e744ebbe4627c25ab47b0385250213199257226e0cb70bfe`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143ff3d76f78be60926ec476578c670f933471a9fcf678dfb26104f87ec4248`  
		Last Modified: Tue, 13 Jul 2021 23:48:06 GMT  
		Size: 71.4 MB (71437154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66adf06926d7de93b5a38027e70481343436196027cc982871cd87684975c9`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48b2a34851fd54047498d82409a6366486970136fc7ce3151b38dd1e1a1a660`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a4c79ab4f05d4088c934e62b52f58c794e8c94e73a3dcfad5ded42252aa3df8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117628870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0361d567d7920a770863e8fade1d338b3edae167dd86259883e39141120cb2b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:51:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:52:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:53:02 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:53:53 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:54:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:55:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:55:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:56:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:56:14 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 18:56:22 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 18:56:29 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 18:56:38 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 18:56:48 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Tue, 13 Jul 2021 18:57:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 19:02:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 19:02:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 19:02:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 19:02:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 19:03:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 19:03:16 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 19:03:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f58409e900735b3af04414a2eac25dcf2479f264457522587a2d3b713cb1d54`  
		Last Modified: Tue, 13 Jul 2021 19:07:28 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0832199508426a244908601f7a3fafb898620be6f90658b526f29fcccc7ccf50`  
		Last Modified: Tue, 13 Jul 2021 19:07:28 GMT  
		Size: 5.6 MB (5630513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c69e1972a6436931f30c95a56fdfc15d48c27ac84d60eedeaf40742b613731`  
		Last Modified: Tue, 13 Jul 2021 19:07:27 GMT  
		Size: 3.5 MB (3528890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea947a3fe9cdc3598e8c581207c216fdb3ff0f0f363d6355e8c3b519679e925`  
		Last Modified: Tue, 13 Jul 2021 19:07:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb53ae5254fffcbc388441f70643e8e1f8d4012f20900d2f38c07ab4bf5092`  
		Last Modified: Tue, 13 Jul 2021 19:07:26 GMT  
		Size: 1.9 MB (1938748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e8ec4a32b9707ce15e0b2615457ebe1363cb69ac9fc661be956c391f800788`  
		Last Modified: Tue, 13 Jul 2021 19:07:24 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166205ee57ab5a5cc638447f66eb909d6180afdc0b8b91422bd6e505c2fa94e8`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f0c8ad70d2e4bc7211ce6bff737a24b294e38caac31b81400b9737a4c9665f`  
		Last Modified: Tue, 13 Jul 2021 19:07:39 GMT  
		Size: 76.1 MB (76092107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bb9b897fbedc49e30c200909402110b6f9216b784a0eee10f60f07718e071d`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96e91da134b7450e3adf4341191479190b484764c762c49f916f6ebb1b89931`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.39`

```console
$ docker pull mariadb@sha256:3a56ade2bc086445696d6a7eee3098f256a686a2944b77d104ea3d42154058d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.39` - linux; amd64

```console
$ docker pull mariadb@sha256:5c0e9eb27ad2c186cb9b10d0310f3f30eeb5ecc09e9ecf36e432f782f570e9e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecaf9c767e5b4386e0943490478c267578da00339064a347064fdccabf6ac8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:59:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:59:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:59:41 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:59:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 01:00:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 01:00:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:00:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 01:00:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 01:00:23 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:26 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:28 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:30 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 01:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 01:01:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 01:01:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 01:01:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 01:01:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 01:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 01:01:38 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 01:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f3767f093ff77f35d70e64fabf43d7e4f3328f83e55442f0496a755cc4d64b`  
		Last Modified: Wed, 14 Jul 2021 01:05:30 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f57ce2f183ce7276382d0923cc09ec6d5b032340a6e77fae51524c3d53e1cd`  
		Last Modified: Wed, 14 Jul 2021 01:05:29 GMT  
		Size: 4.8 MB (4813397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72574b5b8e280c2c544716ac987bb628a29dffddf0b834fe1f49ac5cc597e668`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 3.5 MB (3547597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b95e8526938e2cfe043471fa153a469217921fefd07794dc79b692a9ec070`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73bc88eeea165da977334c6a9b104bab922ac53ee71c974a3a2d24cd323e8e6`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 1.6 MB (1585899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fbed1b6870267362f5204259d106fb13d92c0573c9f16e4e151ccf98b2035`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1976b29470905458e13aab07a8c0662107ea44f4f2be580aaa7f05409390f96`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ec62c50c2339447743375b73310b58b3553a584c23819c8a8a6b750e6d0ae0`  
		Last Modified: Wed, 14 Jul 2021 01:05:37 GMT  
		Size: 72.6 MB (72638596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f53eb6cd79a22c0ea3ee1450aba9c8eadd87915610aed9b86159e1acd565be`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b9776cfa8c66e0b0996411fda717994fd2616e335532df5e6150a2a528cd5`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.39` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ed44fdfac14863449badc323af635fd968773eff787cb9894976d77582574d96
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104312483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c34c41db269abbf10ab0ed9b5934db68369fe8769012172e052cf52a6dc8a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:09 GMT
ADD file:f5aca23bd8c77beda7e17bb71fc4df34d91662b6179de87029f24d21b9e799ad in / 
# Tue, 13 Jul 2021 23:01:09 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:43:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:43:22 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:43:23 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:43:37 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:43:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:43:46 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:43:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:43:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:43:48 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 23:43:48 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 23:43:48 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 23:43:49 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 23:43:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Tue, 13 Jul 2021 23:43:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:44:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:44:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:44:15 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:44:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:44:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:44:17 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:44:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b9bb7af7248f30dd1b1f9807608f5f532133384e4db55caa6dbc69b9cf15ddcc`  
		Last Modified: Tue, 13 Jul 2021 23:03:17 GMT  
		Size: 23.7 MB (23729498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502273c3f4d3cca6957ee7ad312fccf2a58f474dd4470f4d57fd81c7ccbbad6f`  
		Last Modified: Tue, 13 Jul 2021 23:47:59 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec2b94cdaf1d8183985236813593ca75ec1a93fd8749766a671eed3cb5084a9`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 4.4 MB (4395559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235bbb8ac48487daf075dffd4eeb87748124db368791f39c6291097fd8087907`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 3.2 MB (3204623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab6f216bf65e3ea1463da1a6f3a0c8e6e9a218dccdc525833fd4522258f1d81`  
		Last Modified: Tue, 13 Jul 2021 23:47:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c19647916f33368a8ad9c2261897d199b6c7f12d2fc0c78c68c5e94afc1983`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 1.5 MB (1532405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d482ed8bb6a6891a996239552a67845de3dd3878f25bebaa82503aa8bc89d47`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a41688a5253433e744ebbe4627c25ab47b0385250213199257226e0cb70bfe`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143ff3d76f78be60926ec476578c670f933471a9fcf678dfb26104f87ec4248`  
		Last Modified: Tue, 13 Jul 2021 23:48:06 GMT  
		Size: 71.4 MB (71437154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66adf06926d7de93b5a38027e70481343436196027cc982871cd87684975c9`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48b2a34851fd54047498d82409a6366486970136fc7ce3151b38dd1e1a1a660`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.39` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a4c79ab4f05d4088c934e62b52f58c794e8c94e73a3dcfad5ded42252aa3df8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117628870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0361d567d7920a770863e8fade1d338b3edae167dd86259883e39141120cb2b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:51:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:52:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:53:02 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:53:53 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:54:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:55:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:55:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:56:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:56:14 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 18:56:22 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 18:56:29 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 18:56:38 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 18:56:48 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Tue, 13 Jul 2021 18:57:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 19:02:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 19:02:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 19:02:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 19:02:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 19:03:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 19:03:16 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 19:03:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f58409e900735b3af04414a2eac25dcf2479f264457522587a2d3b713cb1d54`  
		Last Modified: Tue, 13 Jul 2021 19:07:28 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0832199508426a244908601f7a3fafb898620be6f90658b526f29fcccc7ccf50`  
		Last Modified: Tue, 13 Jul 2021 19:07:28 GMT  
		Size: 5.6 MB (5630513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c69e1972a6436931f30c95a56fdfc15d48c27ac84d60eedeaf40742b613731`  
		Last Modified: Tue, 13 Jul 2021 19:07:27 GMT  
		Size: 3.5 MB (3528890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea947a3fe9cdc3598e8c581207c216fdb3ff0f0f363d6355e8c3b519679e925`  
		Last Modified: Tue, 13 Jul 2021 19:07:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb53ae5254fffcbc388441f70643e8e1f8d4012f20900d2f38c07ab4bf5092`  
		Last Modified: Tue, 13 Jul 2021 19:07:26 GMT  
		Size: 1.9 MB (1938748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e8ec4a32b9707ce15e0b2615457ebe1363cb69ac9fc661be956c391f800788`  
		Last Modified: Tue, 13 Jul 2021 19:07:24 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166205ee57ab5a5cc638447f66eb909d6180afdc0b8b91422bd6e505c2fa94e8`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f0c8ad70d2e4bc7211ce6bff737a24b294e38caac31b81400b9737a4c9665f`  
		Last Modified: Tue, 13 Jul 2021 19:07:39 GMT  
		Size: 76.1 MB (76092107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bb9b897fbedc49e30c200909402110b6f9216b784a0eee10f60f07718e071d`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96e91da134b7450e3adf4341191479190b484764c762c49f916f6ebb1b89931`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.39-bionic`

```console
$ docker pull mariadb@sha256:3a56ade2bc086445696d6a7eee3098f256a686a2944b77d104ea3d42154058d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.39-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:5c0e9eb27ad2c186cb9b10d0310f3f30eeb5ecc09e9ecf36e432f782f570e9e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecaf9c767e5b4386e0943490478c267578da00339064a347064fdccabf6ac8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:59:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:59:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:59:41 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:59:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 01:00:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 01:00:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:00:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 01:00:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 01:00:23 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:26 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:28 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:30 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 01:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 01:01:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 01:01:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 01:01:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 01:01:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 01:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 01:01:38 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 01:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f3767f093ff77f35d70e64fabf43d7e4f3328f83e55442f0496a755cc4d64b`  
		Last Modified: Wed, 14 Jul 2021 01:05:30 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f57ce2f183ce7276382d0923cc09ec6d5b032340a6e77fae51524c3d53e1cd`  
		Last Modified: Wed, 14 Jul 2021 01:05:29 GMT  
		Size: 4.8 MB (4813397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72574b5b8e280c2c544716ac987bb628a29dffddf0b834fe1f49ac5cc597e668`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 3.5 MB (3547597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b95e8526938e2cfe043471fa153a469217921fefd07794dc79b692a9ec070`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73bc88eeea165da977334c6a9b104bab922ac53ee71c974a3a2d24cd323e8e6`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 1.6 MB (1585899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fbed1b6870267362f5204259d106fb13d92c0573c9f16e4e151ccf98b2035`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1976b29470905458e13aab07a8c0662107ea44f4f2be580aaa7f05409390f96`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ec62c50c2339447743375b73310b58b3553a584c23819c8a8a6b750e6d0ae0`  
		Last Modified: Wed, 14 Jul 2021 01:05:37 GMT  
		Size: 72.6 MB (72638596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f53eb6cd79a22c0ea3ee1450aba9c8eadd87915610aed9b86159e1acd565be`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b9776cfa8c66e0b0996411fda717994fd2616e335532df5e6150a2a528cd5`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.39-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ed44fdfac14863449badc323af635fd968773eff787cb9894976d77582574d96
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104312483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c34c41db269abbf10ab0ed9b5934db68369fe8769012172e052cf52a6dc8a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:09 GMT
ADD file:f5aca23bd8c77beda7e17bb71fc4df34d91662b6179de87029f24d21b9e799ad in / 
# Tue, 13 Jul 2021 23:01:09 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:43:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:43:22 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:43:23 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:43:37 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:43:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:43:46 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:43:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:43:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:43:48 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 23:43:48 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 23:43:48 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 23:43:49 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 23:43:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Tue, 13 Jul 2021 23:43:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:44:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:44:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:44:15 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:44:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:44:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:44:17 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:44:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b9bb7af7248f30dd1b1f9807608f5f532133384e4db55caa6dbc69b9cf15ddcc`  
		Last Modified: Tue, 13 Jul 2021 23:03:17 GMT  
		Size: 23.7 MB (23729498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502273c3f4d3cca6957ee7ad312fccf2a58f474dd4470f4d57fd81c7ccbbad6f`  
		Last Modified: Tue, 13 Jul 2021 23:47:59 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec2b94cdaf1d8183985236813593ca75ec1a93fd8749766a671eed3cb5084a9`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 4.4 MB (4395559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235bbb8ac48487daf075dffd4eeb87748124db368791f39c6291097fd8087907`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 3.2 MB (3204623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab6f216bf65e3ea1463da1a6f3a0c8e6e9a218dccdc525833fd4522258f1d81`  
		Last Modified: Tue, 13 Jul 2021 23:47:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c19647916f33368a8ad9c2261897d199b6c7f12d2fc0c78c68c5e94afc1983`  
		Last Modified: Tue, 13 Jul 2021 23:47:57 GMT  
		Size: 1.5 MB (1532405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d482ed8bb6a6891a996239552a67845de3dd3878f25bebaa82503aa8bc89d47`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a41688a5253433e744ebbe4627c25ab47b0385250213199257226e0cb70bfe`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143ff3d76f78be60926ec476578c670f933471a9fcf678dfb26104f87ec4248`  
		Last Modified: Tue, 13 Jul 2021 23:48:06 GMT  
		Size: 71.4 MB (71437154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66adf06926d7de93b5a38027e70481343436196027cc982871cd87684975c9`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48b2a34851fd54047498d82409a6366486970136fc7ce3151b38dd1e1a1a660`  
		Last Modified: Tue, 13 Jul 2021 23:47:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.39-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a4c79ab4f05d4088c934e62b52f58c794e8c94e73a3dcfad5ded42252aa3df8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117628870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0361d567d7920a770863e8fade1d338b3edae167dd86259883e39141120cb2b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:51:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:52:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:53:02 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:53:53 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:54:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:55:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:55:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:56:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:56:14 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 18:56:22 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 13 Jul 2021 18:56:29 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 18:56:38 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Tue, 13 Jul 2021 18:56:48 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Tue, 13 Jul 2021 18:57:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 19:02:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 19:02:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 19:02:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 19:02:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 19:03:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 19:03:16 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 19:03:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f58409e900735b3af04414a2eac25dcf2479f264457522587a2d3b713cb1d54`  
		Last Modified: Tue, 13 Jul 2021 19:07:28 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0832199508426a244908601f7a3fafb898620be6f90658b526f29fcccc7ccf50`  
		Last Modified: Tue, 13 Jul 2021 19:07:28 GMT  
		Size: 5.6 MB (5630513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c69e1972a6436931f30c95a56fdfc15d48c27ac84d60eedeaf40742b613731`  
		Last Modified: Tue, 13 Jul 2021 19:07:27 GMT  
		Size: 3.5 MB (3528890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea947a3fe9cdc3598e8c581207c216fdb3ff0f0f363d6355e8c3b519679e925`  
		Last Modified: Tue, 13 Jul 2021 19:07:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb53ae5254fffcbc388441f70643e8e1f8d4012f20900d2f38c07ab4bf5092`  
		Last Modified: Tue, 13 Jul 2021 19:07:26 GMT  
		Size: 1.9 MB (1938748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e8ec4a32b9707ce15e0b2615457ebe1363cb69ac9fc661be956c391f800788`  
		Last Modified: Tue, 13 Jul 2021 19:07:24 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166205ee57ab5a5cc638447f66eb909d6180afdc0b8b91422bd6e505c2fa94e8`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f0c8ad70d2e4bc7211ce6bff737a24b294e38caac31b81400b9737a4c9665f`  
		Last Modified: Tue, 13 Jul 2021 19:07:39 GMT  
		Size: 76.1 MB (76092107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bb9b897fbedc49e30c200909402110b6f9216b784a0eee10f60f07718e071d`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96e91da134b7450e3adf4341191479190b484764c762c49f916f6ebb1b89931`  
		Last Modified: Tue, 13 Jul 2021 19:07:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:dff9668b5710e0ab57926bcd4a6c37025dbfe937f24f32173ba713703e5563a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:2200220af8c594c85bec2f87015d556864bd09bf79ec400e4352736c2cce0cff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120006043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea064dffdcbbab8e6c0474e513499b6f69e8b8c5b9e7d41b0daa515f21a59ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:58:29 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:30 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:31 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:31 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:58:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:59:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:59:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:59:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:59:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:59:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:59:07 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:59:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7485473b128a37cd5bc980f9d450777b261aa523889ed65a8d9639852e3eae`  
		Last Modified: Wed, 14 Jul 2021 01:04:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c09395a910de4b94bff08d273244e33aecc775ab7a2716597a3b1d7e1aaf8`  
		Last Modified: Wed, 14 Jul 2021 01:05:07 GMT  
		Size: 80.1 MB (80084453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae821e04294bc113a0af411372e4882c95010797b6c4f1699ea571cc9e9989a`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fa297a84b058873441d197f56558c7e377dcd8e0f09f5a182faf1475bdc52`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:af7d14ed5d4bdcb5c5ca1ac124c148f0be07eb652c33f0bd5993ece2a9a7a98b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117602195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9125427b1aabfe2b93830624a24746a9305b7c3bcd13f439a772824ec38423bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:42:34 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 23:42:34 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 23:42:35 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 23:42:35 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 23:42:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:42:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:43:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:43:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:43:02 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:43:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:43:03 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:43:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43268ea17b1c1d1c8631b184cc5a9f47c2708af140c0cba92c962538b66691bc`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd88600d54d9e6036c96c272728aab05a2a0eac7d3fed68e36aa7017f248cdf`  
		Last Modified: Tue, 13 Jul 2021 23:47:33 GMT  
		Size: 79.4 MB (79396660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db297bf843017efffb82d89c86f3e1640a13434ddbf98cc60cef5362d3b91dd`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4333b160e7a5511b09d3495174a23d16566dfb2890e931fca35ddc8a40240cd6`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b2c552fc7a7d6ee5db05ac791788df2bb2e13594e61acdf82847bee9d9533656
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130856605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d8a560fb11e0a38789e17a75bc49f382ea95c3471fc8cba0beea9bf296253b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:43:32 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 18:43:40 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 18:43:44 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 18:43:49 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 18:43:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:44:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:50:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:50:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:50:26 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:50:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 18:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:50:48 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:50:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c37b77f222c35386cdcdfe28385f12ceab99a56a60ed48e17388733ac9d3e1`  
		Last Modified: Tue, 13 Jul 2021 19:06:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f600a611d6f900d7aacdc5beb2cba123ec10617ec1a46eb579dca2dda784d27c`  
		Last Modified: Tue, 13 Jul 2021 19:07:03 GMT  
		Size: 84.7 MB (84658918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5de95fe32eee38a71f34a6ee41659b4a6d40d7f8c2896548d7e0156b40b9e6`  
		Last Modified: Tue, 13 Jul 2021 19:06:45 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96a3a3d50a9a9b8b6e2c370b7a0248cb4796da01e3cfdf8cb4a9dcaa61dfb22`  
		Last Modified: Tue, 13 Jul 2021 19:06:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:dff9668b5710e0ab57926bcd4a6c37025dbfe937f24f32173ba713703e5563a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2200220af8c594c85bec2f87015d556864bd09bf79ec400e4352736c2cce0cff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120006043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea064dffdcbbab8e6c0474e513499b6f69e8b8c5b9e7d41b0daa515f21a59ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:58:29 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:30 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:31 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:31 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:58:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:59:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:59:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:59:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:59:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:59:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:59:07 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:59:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7485473b128a37cd5bc980f9d450777b261aa523889ed65a8d9639852e3eae`  
		Last Modified: Wed, 14 Jul 2021 01:04:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c09395a910de4b94bff08d273244e33aecc775ab7a2716597a3b1d7e1aaf8`  
		Last Modified: Wed, 14 Jul 2021 01:05:07 GMT  
		Size: 80.1 MB (80084453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae821e04294bc113a0af411372e4882c95010797b6c4f1699ea571cc9e9989a`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fa297a84b058873441d197f56558c7e377dcd8e0f09f5a182faf1475bdc52`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:af7d14ed5d4bdcb5c5ca1ac124c148f0be07eb652c33f0bd5993ece2a9a7a98b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117602195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9125427b1aabfe2b93830624a24746a9305b7c3bcd13f439a772824ec38423bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:42:34 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 23:42:34 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 23:42:35 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 23:42:35 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 23:42:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:42:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:43:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:43:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:43:02 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:43:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:43:03 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:43:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43268ea17b1c1d1c8631b184cc5a9f47c2708af140c0cba92c962538b66691bc`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd88600d54d9e6036c96c272728aab05a2a0eac7d3fed68e36aa7017f248cdf`  
		Last Modified: Tue, 13 Jul 2021 23:47:33 GMT  
		Size: 79.4 MB (79396660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db297bf843017efffb82d89c86f3e1640a13434ddbf98cc60cef5362d3b91dd`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4333b160e7a5511b09d3495174a23d16566dfb2890e931fca35ddc8a40240cd6`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b2c552fc7a7d6ee5db05ac791788df2bb2e13594e61acdf82847bee9d9533656
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130856605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d8a560fb11e0a38789e17a75bc49f382ea95c3471fc8cba0beea9bf296253b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:43:32 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 18:43:40 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 18:43:44 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 18:43:49 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 18:43:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:44:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:50:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:50:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:50:26 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:50:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 18:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:50:48 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:50:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c37b77f222c35386cdcdfe28385f12ceab99a56a60ed48e17388733ac9d3e1`  
		Last Modified: Tue, 13 Jul 2021 19:06:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f600a611d6f900d7aacdc5beb2cba123ec10617ec1a46eb579dca2dda784d27c`  
		Last Modified: Tue, 13 Jul 2021 19:07:03 GMT  
		Size: 84.7 MB (84658918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5de95fe32eee38a71f34a6ee41659b4a6d40d7f8c2896548d7e0156b40b9e6`  
		Last Modified: Tue, 13 Jul 2021 19:06:45 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96a3a3d50a9a9b8b6e2c370b7a0248cb4796da01e3cfdf8cb4a9dcaa61dfb22`  
		Last Modified: Tue, 13 Jul 2021 19:06:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.30`

```console
$ docker pull mariadb@sha256:dff9668b5710e0ab57926bcd4a6c37025dbfe937f24f32173ba713703e5563a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.30` - linux; amd64

```console
$ docker pull mariadb@sha256:2200220af8c594c85bec2f87015d556864bd09bf79ec400e4352736c2cce0cff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120006043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea064dffdcbbab8e6c0474e513499b6f69e8b8c5b9e7d41b0daa515f21a59ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:58:29 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:30 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:31 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:31 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:58:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:59:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:59:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:59:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:59:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:59:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:59:07 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:59:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7485473b128a37cd5bc980f9d450777b261aa523889ed65a8d9639852e3eae`  
		Last Modified: Wed, 14 Jul 2021 01:04:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c09395a910de4b94bff08d273244e33aecc775ab7a2716597a3b1d7e1aaf8`  
		Last Modified: Wed, 14 Jul 2021 01:05:07 GMT  
		Size: 80.1 MB (80084453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae821e04294bc113a0af411372e4882c95010797b6c4f1699ea571cc9e9989a`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fa297a84b058873441d197f56558c7e377dcd8e0f09f5a182faf1475bdc52`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.30` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:af7d14ed5d4bdcb5c5ca1ac124c148f0be07eb652c33f0bd5993ece2a9a7a98b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117602195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9125427b1aabfe2b93830624a24746a9305b7c3bcd13f439a772824ec38423bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:42:34 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 23:42:34 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 23:42:35 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 23:42:35 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 23:42:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:42:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:43:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:43:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:43:02 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:43:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:43:03 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:43:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43268ea17b1c1d1c8631b184cc5a9f47c2708af140c0cba92c962538b66691bc`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd88600d54d9e6036c96c272728aab05a2a0eac7d3fed68e36aa7017f248cdf`  
		Last Modified: Tue, 13 Jul 2021 23:47:33 GMT  
		Size: 79.4 MB (79396660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db297bf843017efffb82d89c86f3e1640a13434ddbf98cc60cef5362d3b91dd`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4333b160e7a5511b09d3495174a23d16566dfb2890e931fca35ddc8a40240cd6`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.30` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b2c552fc7a7d6ee5db05ac791788df2bb2e13594e61acdf82847bee9d9533656
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130856605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d8a560fb11e0a38789e17a75bc49f382ea95c3471fc8cba0beea9bf296253b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:43:32 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 18:43:40 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 18:43:44 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 18:43:49 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 18:43:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:44:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:50:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:50:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:50:26 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:50:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 18:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:50:48 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:50:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c37b77f222c35386cdcdfe28385f12ceab99a56a60ed48e17388733ac9d3e1`  
		Last Modified: Tue, 13 Jul 2021 19:06:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f600a611d6f900d7aacdc5beb2cba123ec10617ec1a46eb579dca2dda784d27c`  
		Last Modified: Tue, 13 Jul 2021 19:07:03 GMT  
		Size: 84.7 MB (84658918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5de95fe32eee38a71f34a6ee41659b4a6d40d7f8c2896548d7e0156b40b9e6`  
		Last Modified: Tue, 13 Jul 2021 19:06:45 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96a3a3d50a9a9b8b6e2c370b7a0248cb4796da01e3cfdf8cb4a9dcaa61dfb22`  
		Last Modified: Tue, 13 Jul 2021 19:06:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.30-focal`

```console
$ docker pull mariadb@sha256:dff9668b5710e0ab57926bcd4a6c37025dbfe937f24f32173ba713703e5563a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.30-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2200220af8c594c85bec2f87015d556864bd09bf79ec400e4352736c2cce0cff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120006043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea064dffdcbbab8e6c0474e513499b6f69e8b8c5b9e7d41b0daa515f21a59ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:58:29 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:30 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:31 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:31 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:58:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:59:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:59:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:59:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:59:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:59:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:59:07 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:59:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7485473b128a37cd5bc980f9d450777b261aa523889ed65a8d9639852e3eae`  
		Last Modified: Wed, 14 Jul 2021 01:04:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c09395a910de4b94bff08d273244e33aecc775ab7a2716597a3b1d7e1aaf8`  
		Last Modified: Wed, 14 Jul 2021 01:05:07 GMT  
		Size: 80.1 MB (80084453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae821e04294bc113a0af411372e4882c95010797b6c4f1699ea571cc9e9989a`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fa297a84b058873441d197f56558c7e377dcd8e0f09f5a182faf1475bdc52`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.30-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:af7d14ed5d4bdcb5c5ca1ac124c148f0be07eb652c33f0bd5993ece2a9a7a98b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117602195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9125427b1aabfe2b93830624a24746a9305b7c3bcd13f439a772824ec38423bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:42:34 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 23:42:34 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 23:42:35 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 23:42:35 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 23:42:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:42:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:43:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:43:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:43:02 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:43:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:43:03 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:43:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43268ea17b1c1d1c8631b184cc5a9f47c2708af140c0cba92c962538b66691bc`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd88600d54d9e6036c96c272728aab05a2a0eac7d3fed68e36aa7017f248cdf`  
		Last Modified: Tue, 13 Jul 2021 23:47:33 GMT  
		Size: 79.4 MB (79396660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db297bf843017efffb82d89c86f3e1640a13434ddbf98cc60cef5362d3b91dd`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4333b160e7a5511b09d3495174a23d16566dfb2890e931fca35ddc8a40240cd6`  
		Last Modified: Tue, 13 Jul 2021 23:47:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.30-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b2c552fc7a7d6ee5db05ac791788df2bb2e13594e61acdf82847bee9d9533656
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130856605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d8a560fb11e0a38789e17a75bc49f382ea95c3471fc8cba0beea9bf296253b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:43:32 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 18:43:40 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 13 Jul 2021 18:43:44 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 18:43:49 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Tue, 13 Jul 2021 18:43:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:44:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:50:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:50:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:50:26 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:50:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 18:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:50:48 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:50:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c37b77f222c35386cdcdfe28385f12ceab99a56a60ed48e17388733ac9d3e1`  
		Last Modified: Tue, 13 Jul 2021 19:06:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f600a611d6f900d7aacdc5beb2cba123ec10617ec1a46eb579dca2dda784d27c`  
		Last Modified: Tue, 13 Jul 2021 19:07:03 GMT  
		Size: 84.7 MB (84658918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5de95fe32eee38a71f34a6ee41659b4a6d40d7f8c2896548d7e0156b40b9e6`  
		Last Modified: Tue, 13 Jul 2021 19:06:45 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96a3a3d50a9a9b8b6e2c370b7a0248cb4796da01e3cfdf8cb4a9dcaa61dfb22`  
		Last Modified: Tue, 13 Jul 2021 19:06:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:ebc9529442d9c74eb9faab11afebd33120e0e09b4c7e5da3ed98353db3c0b5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:873e9aaaa7780da10c339f3337abf52882a310cae2ddfd2fb3fa85c78dd44350
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124698892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4271ce8f6f798b83d152e870b3fbeaf9729badd41cf51a61c004be0ac7b578d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:57:51 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:58:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:58:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:58:21 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:58:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:58:23 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:58:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22892204a1dcc32ac7a09fbaabbd878f2b4eef3ee20dd0c577d92294c8b11a26`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a277be0f6c45f67f0267866a6cf0c2bc8d2111ba881cb0973953afd23c3164`  
		Last Modified: Wed, 14 Jul 2021 01:04:23 GMT  
		Size: 84.8 MB (84777306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54988cc2ae8f9e448e7d2bd52f22bebe8bea5b0a54fc645d6d767f63429e59f4`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1763fc3dea70e993f8df4666cd3011f50983aabcfc90380564544584389cda`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:57e3590caa89ddf35f600349c697e342db3186861533037879195af23e95c071
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122212693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da19a7da07ae42245a6c192e4b824cf09269aa87c330086e388a178057361fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:42:02 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 23:42:02 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 23:42:03 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 23:42:03 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 23:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:42:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:42:26 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:42:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:42:28 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:42:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b16d3b824d146bc8f021562fbb7af6ec58b79c24991f5190058badc39454f5`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37388efb3dcb4e552624965e0fdf4161aff488db6474985830aa1f51b543fa`  
		Last Modified: Tue, 13 Jul 2021 23:46:58 GMT  
		Size: 84.0 MB (84007160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17003f507248f7de1c6c44cec099a9d9f18be52d257f56db6a9ecf3f821496f7`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 5.6 KB (5591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134cc878d2d2d05235a40c4bb41dcfedca417ebec331118f825fdeccfdcc567c`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7fd82f16093dc926c2a5f134c7ea8c11da1e88cbbc04d8bf765f20dd31c23d6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135427867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7c91cccdefa1ef2eee18000ea4ae147bbd04e905ce86ad3e599d1d2f54a0c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:37:10 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 18:37:13 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 18:37:16 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 18:37:18 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 18:37:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:37:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:41:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:42:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:42:04 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 18:42:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:42:54 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:43:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdba9bdc7a685b07e118e09ef8dec601bb462e55c413f9632fd74989b08838a`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd51d2c8a50ee959f075adb75e4bf9982ca10843df4e07b59156f7ee5f5b6b46`  
		Last Modified: Tue, 13 Jul 2021 19:06:25 GMT  
		Size: 89.2 MB (89230180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a280eae3846126956894661f132ca6dac5d1e8c57736a5e77a13b05399de9fa`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2e7e9297225091bf214d4aefb57f3a2f8005d779ae3434fb3667efee518b7f`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:ebc9529442d9c74eb9faab11afebd33120e0e09b4c7e5da3ed98353db3c0b5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:873e9aaaa7780da10c339f3337abf52882a310cae2ddfd2fb3fa85c78dd44350
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124698892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4271ce8f6f798b83d152e870b3fbeaf9729badd41cf51a61c004be0ac7b578d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:57:51 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:58:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:58:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:58:21 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:58:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:58:23 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:58:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22892204a1dcc32ac7a09fbaabbd878f2b4eef3ee20dd0c577d92294c8b11a26`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a277be0f6c45f67f0267866a6cf0c2bc8d2111ba881cb0973953afd23c3164`  
		Last Modified: Wed, 14 Jul 2021 01:04:23 GMT  
		Size: 84.8 MB (84777306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54988cc2ae8f9e448e7d2bd52f22bebe8bea5b0a54fc645d6d767f63429e59f4`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1763fc3dea70e993f8df4666cd3011f50983aabcfc90380564544584389cda`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:57e3590caa89ddf35f600349c697e342db3186861533037879195af23e95c071
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122212693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da19a7da07ae42245a6c192e4b824cf09269aa87c330086e388a178057361fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:42:02 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 23:42:02 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 23:42:03 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 23:42:03 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 23:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:42:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:42:26 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:42:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:42:28 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:42:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b16d3b824d146bc8f021562fbb7af6ec58b79c24991f5190058badc39454f5`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37388efb3dcb4e552624965e0fdf4161aff488db6474985830aa1f51b543fa`  
		Last Modified: Tue, 13 Jul 2021 23:46:58 GMT  
		Size: 84.0 MB (84007160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17003f507248f7de1c6c44cec099a9d9f18be52d257f56db6a9ecf3f821496f7`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 5.6 KB (5591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134cc878d2d2d05235a40c4bb41dcfedca417ebec331118f825fdeccfdcc567c`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7fd82f16093dc926c2a5f134c7ea8c11da1e88cbbc04d8bf765f20dd31c23d6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135427867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7c91cccdefa1ef2eee18000ea4ae147bbd04e905ce86ad3e599d1d2f54a0c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:37:10 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 18:37:13 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 18:37:16 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 18:37:18 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 18:37:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:37:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:41:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:42:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:42:04 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 18:42:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:42:54 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:43:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdba9bdc7a685b07e118e09ef8dec601bb462e55c413f9632fd74989b08838a`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd51d2c8a50ee959f075adb75e4bf9982ca10843df4e07b59156f7ee5f5b6b46`  
		Last Modified: Tue, 13 Jul 2021 19:06:25 GMT  
		Size: 89.2 MB (89230180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a280eae3846126956894661f132ca6dac5d1e8c57736a5e77a13b05399de9fa`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2e7e9297225091bf214d4aefb57f3a2f8005d779ae3434fb3667efee518b7f`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.20`

```console
$ docker pull mariadb@sha256:ebc9529442d9c74eb9faab11afebd33120e0e09b4c7e5da3ed98353db3c0b5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.20` - linux; amd64

```console
$ docker pull mariadb@sha256:873e9aaaa7780da10c339f3337abf52882a310cae2ddfd2fb3fa85c78dd44350
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124698892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4271ce8f6f798b83d152e870b3fbeaf9729badd41cf51a61c004be0ac7b578d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:57:51 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:58:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:58:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:58:21 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:58:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:58:23 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:58:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22892204a1dcc32ac7a09fbaabbd878f2b4eef3ee20dd0c577d92294c8b11a26`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a277be0f6c45f67f0267866a6cf0c2bc8d2111ba881cb0973953afd23c3164`  
		Last Modified: Wed, 14 Jul 2021 01:04:23 GMT  
		Size: 84.8 MB (84777306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54988cc2ae8f9e448e7d2bd52f22bebe8bea5b0a54fc645d6d767f63429e59f4`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1763fc3dea70e993f8df4666cd3011f50983aabcfc90380564544584389cda`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.20` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:57e3590caa89ddf35f600349c697e342db3186861533037879195af23e95c071
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122212693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da19a7da07ae42245a6c192e4b824cf09269aa87c330086e388a178057361fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:42:02 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 23:42:02 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 23:42:03 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 23:42:03 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 23:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:42:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:42:26 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:42:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:42:28 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:42:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b16d3b824d146bc8f021562fbb7af6ec58b79c24991f5190058badc39454f5`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37388efb3dcb4e552624965e0fdf4161aff488db6474985830aa1f51b543fa`  
		Last Modified: Tue, 13 Jul 2021 23:46:58 GMT  
		Size: 84.0 MB (84007160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17003f507248f7de1c6c44cec099a9d9f18be52d257f56db6a9ecf3f821496f7`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 5.6 KB (5591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134cc878d2d2d05235a40c4bb41dcfedca417ebec331118f825fdeccfdcc567c`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.20` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7fd82f16093dc926c2a5f134c7ea8c11da1e88cbbc04d8bf765f20dd31c23d6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135427867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7c91cccdefa1ef2eee18000ea4ae147bbd04e905ce86ad3e599d1d2f54a0c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:37:10 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 18:37:13 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 18:37:16 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 18:37:18 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 18:37:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:37:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:41:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:42:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:42:04 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 18:42:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:42:54 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:43:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdba9bdc7a685b07e118e09ef8dec601bb462e55c413f9632fd74989b08838a`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd51d2c8a50ee959f075adb75e4bf9982ca10843df4e07b59156f7ee5f5b6b46`  
		Last Modified: Tue, 13 Jul 2021 19:06:25 GMT  
		Size: 89.2 MB (89230180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a280eae3846126956894661f132ca6dac5d1e8c57736a5e77a13b05399de9fa`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2e7e9297225091bf214d4aefb57f3a2f8005d779ae3434fb3667efee518b7f`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.20-focal`

```console
$ docker pull mariadb@sha256:ebc9529442d9c74eb9faab11afebd33120e0e09b4c7e5da3ed98353db3c0b5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.20-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:873e9aaaa7780da10c339f3337abf52882a310cae2ddfd2fb3fa85c78dd44350
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124698892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4271ce8f6f798b83d152e870b3fbeaf9729badd41cf51a61c004be0ac7b578d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:57:51 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:58:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:58:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:58:21 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:58:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:58:23 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:58:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22892204a1dcc32ac7a09fbaabbd878f2b4eef3ee20dd0c577d92294c8b11a26`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a277be0f6c45f67f0267866a6cf0c2bc8d2111ba881cb0973953afd23c3164`  
		Last Modified: Wed, 14 Jul 2021 01:04:23 GMT  
		Size: 84.8 MB (84777306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54988cc2ae8f9e448e7d2bd52f22bebe8bea5b0a54fc645d6d767f63429e59f4`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1763fc3dea70e993f8df4666cd3011f50983aabcfc90380564544584389cda`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.20-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:57e3590caa89ddf35f600349c697e342db3186861533037879195af23e95c071
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122212693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da19a7da07ae42245a6c192e4b824cf09269aa87c330086e388a178057361fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:42:02 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 23:42:02 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 23:42:03 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 23:42:03 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 23:42:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:42:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:42:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:42:26 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:42:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 23:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:42:28 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:42:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b16d3b824d146bc8f021562fbb7af6ec58b79c24991f5190058badc39454f5`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37388efb3dcb4e552624965e0fdf4161aff488db6474985830aa1f51b543fa`  
		Last Modified: Tue, 13 Jul 2021 23:46:58 GMT  
		Size: 84.0 MB (84007160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17003f507248f7de1c6c44cec099a9d9f18be52d257f56db6a9ecf3f821496f7`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 5.6 KB (5591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134cc878d2d2d05235a40c4bb41dcfedca417ebec331118f825fdeccfdcc567c`  
		Last Modified: Tue, 13 Jul 2021 23:46:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.20-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7fd82f16093dc926c2a5f134c7ea8c11da1e88cbbc04d8bf765f20dd31c23d6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135427867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7c91cccdefa1ef2eee18000ea4ae147bbd04e905ce86ad3e599d1d2f54a0c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:37:10 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 18:37:13 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 13 Jul 2021 18:37:16 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 18:37:18 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Tue, 13 Jul 2021 18:37:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:37:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:41:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:42:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:42:04 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:42:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 13 Jul 2021 18:42:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:42:54 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:43:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdba9bdc7a685b07e118e09ef8dec601bb462e55c413f9632fd74989b08838a`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd51d2c8a50ee959f075adb75e4bf9982ca10843df4e07b59156f7ee5f5b6b46`  
		Last Modified: Tue, 13 Jul 2021 19:06:25 GMT  
		Size: 89.2 MB (89230180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a280eae3846126956894661f132ca6dac5d1e8c57736a5e77a13b05399de9fa`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2e7e9297225091bf214d4aefb57f3a2f8005d779ae3434fb3667efee518b7f`  
		Last Modified: Tue, 13 Jul 2021 19:06:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:578dcf77454f6c9e5703df918d9ff5f69b48c8d46559b613ab7e303eb122fec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:274de17495adb706879e52d682a4874e8a854c11ecd4d751af997b7ad6d5a15f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126864725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff83ee8fca90abb3f0ff9891da7de437edecef4e1a8e4108a90d8304caebc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:59 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:57:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:57:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:57:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:57:44 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720369b47fdd0f149e8c143bdf5c51dd13c1b27ef04d1342b05069c361ce1b3`  
		Last Modified: Wed, 14 Jul 2021 01:03:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c976e521f0a64e4b3f652b4a3773e75bfae5c9cd6e6faeeaa3ed055b6f24030`  
		Last Modified: Wed, 14 Jul 2021 01:03:51 GMT  
		Size: 86.9 MB (86943256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09dfea021b87a2385efabc7278606a4b2c7b29a8ef8d4a5261b6ebd14a81c6`  
		Last Modified: Wed, 14 Jul 2021 01:03:37 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8ef684c95a2e940fe537ef9a73d7580e30a07de334d6e60c21b34607bfbdbe38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124297465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a3a576ce7e6b353fd132f872360a916b8e68231f967ce5a41685d1b60c7e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:41:31 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 23:41:31 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 23:41:31 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 23:41:32 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 23:41:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:41:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:54 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:54 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599f73b8461eca5b74755637bd0bee655873ecd8a60e9f2685136b3c95d18f6`  
		Last Modified: Tue, 13 Jul 2021 23:46:06 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31862b9eb243c3e684b4ee6de425d39982bb69bf124d58030470691681dec156`  
		Last Modified: Tue, 13 Jul 2021 23:46:22 GMT  
		Size: 86.1 MB (86092056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3628e06e034599173349c2993e2f60aa39b38f88a714ab813b9cfc0866abdde3`  
		Last Modified: Tue, 13 Jul 2021 23:46:06 GMT  
		Size: 5.6 KB (5590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9cf78d86507c53c26cc476d52cd5538e69d29be9543f947365459857bce04240
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137538955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec132bda7b0a57f17df73d85683d5185bab64c2afd2ec123e4225815451d959c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:32:57 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 18:33:01 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 18:33:06 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 18:33:14 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 18:33:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:33:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:36:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:36:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:36:41 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:36:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:36:50 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:36:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79d7181537052b57e8f56d1b03c9081a56b1f468194318b6112c5d669d3f8f4`  
		Last Modified: Tue, 13 Jul 2021 19:05:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13154635bf5454dfc1d3473e53786ccc2123877921618ffda6adea0defe03a1`  
		Last Modified: Tue, 13 Jul 2021 19:05:46 GMT  
		Size: 91.3 MB (91341389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7ecd187b32672194646c1fafac119499c8acbddd0b81e53859cccf7badfde8`  
		Last Modified: Tue, 13 Jul 2021 19:05:27 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:578dcf77454f6c9e5703df918d9ff5f69b48c8d46559b613ab7e303eb122fec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:274de17495adb706879e52d682a4874e8a854c11ecd4d751af997b7ad6d5a15f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126864725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff83ee8fca90abb3f0ff9891da7de437edecef4e1a8e4108a90d8304caebc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:59 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:57:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:57:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:57:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:57:44 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720369b47fdd0f149e8c143bdf5c51dd13c1b27ef04d1342b05069c361ce1b3`  
		Last Modified: Wed, 14 Jul 2021 01:03:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c976e521f0a64e4b3f652b4a3773e75bfae5c9cd6e6faeeaa3ed055b6f24030`  
		Last Modified: Wed, 14 Jul 2021 01:03:51 GMT  
		Size: 86.9 MB (86943256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09dfea021b87a2385efabc7278606a4b2c7b29a8ef8d4a5261b6ebd14a81c6`  
		Last Modified: Wed, 14 Jul 2021 01:03:37 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8ef684c95a2e940fe537ef9a73d7580e30a07de334d6e60c21b34607bfbdbe38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124297465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a3a576ce7e6b353fd132f872360a916b8e68231f967ce5a41685d1b60c7e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:41:31 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 23:41:31 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 23:41:31 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 23:41:32 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 23:41:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:41:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:54 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:54 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599f73b8461eca5b74755637bd0bee655873ecd8a60e9f2685136b3c95d18f6`  
		Last Modified: Tue, 13 Jul 2021 23:46:06 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31862b9eb243c3e684b4ee6de425d39982bb69bf124d58030470691681dec156`  
		Last Modified: Tue, 13 Jul 2021 23:46:22 GMT  
		Size: 86.1 MB (86092056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3628e06e034599173349c2993e2f60aa39b38f88a714ab813b9cfc0866abdde3`  
		Last Modified: Tue, 13 Jul 2021 23:46:06 GMT  
		Size: 5.6 KB (5590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9cf78d86507c53c26cc476d52cd5538e69d29be9543f947365459857bce04240
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137538955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec132bda7b0a57f17df73d85683d5185bab64c2afd2ec123e4225815451d959c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:32:57 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 18:33:01 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 18:33:06 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 18:33:14 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 18:33:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:33:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:36:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:36:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:36:41 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:36:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:36:50 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:36:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79d7181537052b57e8f56d1b03c9081a56b1f468194318b6112c5d669d3f8f4`  
		Last Modified: Tue, 13 Jul 2021 19:05:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13154635bf5454dfc1d3473e53786ccc2123877921618ffda6adea0defe03a1`  
		Last Modified: Tue, 13 Jul 2021 19:05:46 GMT  
		Size: 91.3 MB (91341389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7ecd187b32672194646c1fafac119499c8acbddd0b81e53859cccf7badfde8`  
		Last Modified: Tue, 13 Jul 2021 19:05:27 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.11`

```console
$ docker pull mariadb@sha256:578dcf77454f6c9e5703df918d9ff5f69b48c8d46559b613ab7e303eb122fec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.11` - linux; amd64

```console
$ docker pull mariadb@sha256:274de17495adb706879e52d682a4874e8a854c11ecd4d751af997b7ad6d5a15f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126864725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff83ee8fca90abb3f0ff9891da7de437edecef4e1a8e4108a90d8304caebc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:59 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:57:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:57:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:57:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:57:44 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720369b47fdd0f149e8c143bdf5c51dd13c1b27ef04d1342b05069c361ce1b3`  
		Last Modified: Wed, 14 Jul 2021 01:03:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c976e521f0a64e4b3f652b4a3773e75bfae5c9cd6e6faeeaa3ed055b6f24030`  
		Last Modified: Wed, 14 Jul 2021 01:03:51 GMT  
		Size: 86.9 MB (86943256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09dfea021b87a2385efabc7278606a4b2c7b29a8ef8d4a5261b6ebd14a81c6`  
		Last Modified: Wed, 14 Jul 2021 01:03:37 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.11` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8ef684c95a2e940fe537ef9a73d7580e30a07de334d6e60c21b34607bfbdbe38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124297465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a3a576ce7e6b353fd132f872360a916b8e68231f967ce5a41685d1b60c7e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:41:31 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 23:41:31 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 23:41:31 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 23:41:32 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 23:41:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:41:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:54 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:54 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599f73b8461eca5b74755637bd0bee655873ecd8a60e9f2685136b3c95d18f6`  
		Last Modified: Tue, 13 Jul 2021 23:46:06 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31862b9eb243c3e684b4ee6de425d39982bb69bf124d58030470691681dec156`  
		Last Modified: Tue, 13 Jul 2021 23:46:22 GMT  
		Size: 86.1 MB (86092056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3628e06e034599173349c2993e2f60aa39b38f88a714ab813b9cfc0866abdde3`  
		Last Modified: Tue, 13 Jul 2021 23:46:06 GMT  
		Size: 5.6 KB (5590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.11` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9cf78d86507c53c26cc476d52cd5538e69d29be9543f947365459857bce04240
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137538955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec132bda7b0a57f17df73d85683d5185bab64c2afd2ec123e4225815451d959c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:32:57 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 18:33:01 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 18:33:06 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 18:33:14 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 18:33:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:33:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:36:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:36:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:36:41 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:36:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:36:50 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:36:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79d7181537052b57e8f56d1b03c9081a56b1f468194318b6112c5d669d3f8f4`  
		Last Modified: Tue, 13 Jul 2021 19:05:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13154635bf5454dfc1d3473e53786ccc2123877921618ffda6adea0defe03a1`  
		Last Modified: Tue, 13 Jul 2021 19:05:46 GMT  
		Size: 91.3 MB (91341389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7ecd187b32672194646c1fafac119499c8acbddd0b81e53859cccf7badfde8`  
		Last Modified: Tue, 13 Jul 2021 19:05:27 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.11-focal`

```console
$ docker pull mariadb@sha256:578dcf77454f6c9e5703df918d9ff5f69b48c8d46559b613ab7e303eb122fec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.11-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:274de17495adb706879e52d682a4874e8a854c11ecd4d751af997b7ad6d5a15f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126864725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff83ee8fca90abb3f0ff9891da7de437edecef4e1a8e4108a90d8304caebc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:59 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:57:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:57:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:57:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:57:44 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720369b47fdd0f149e8c143bdf5c51dd13c1b27ef04d1342b05069c361ce1b3`  
		Last Modified: Wed, 14 Jul 2021 01:03:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c976e521f0a64e4b3f652b4a3773e75bfae5c9cd6e6faeeaa3ed055b6f24030`  
		Last Modified: Wed, 14 Jul 2021 01:03:51 GMT  
		Size: 86.9 MB (86943256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09dfea021b87a2385efabc7278606a4b2c7b29a8ef8d4a5261b6ebd14a81c6`  
		Last Modified: Wed, 14 Jul 2021 01:03:37 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.11-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8ef684c95a2e940fe537ef9a73d7580e30a07de334d6e60c21b34607bfbdbe38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124297465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a3a576ce7e6b353fd132f872360a916b8e68231f967ce5a41685d1b60c7e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:41:31 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 23:41:31 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 23:41:31 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 23:41:32 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 23:41:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:41:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:54 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:54 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599f73b8461eca5b74755637bd0bee655873ecd8a60e9f2685136b3c95d18f6`  
		Last Modified: Tue, 13 Jul 2021 23:46:06 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31862b9eb243c3e684b4ee6de425d39982bb69bf124d58030470691681dec156`  
		Last Modified: Tue, 13 Jul 2021 23:46:22 GMT  
		Size: 86.1 MB (86092056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3628e06e034599173349c2993e2f60aa39b38f88a714ab813b9cfc0866abdde3`  
		Last Modified: Tue, 13 Jul 2021 23:46:06 GMT  
		Size: 5.6 KB (5590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.11-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9cf78d86507c53c26cc476d52cd5538e69d29be9543f947365459857bce04240
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137538955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec132bda7b0a57f17df73d85683d5185bab64c2afd2ec123e4225815451d959c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:32:57 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 18:33:01 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 13 Jul 2021 18:33:06 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 18:33:14 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Tue, 13 Jul 2021 18:33:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:33:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:36:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:36:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:36:41 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:36:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:36:50 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:36:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79d7181537052b57e8f56d1b03c9081a56b1f468194318b6112c5d669d3f8f4`  
		Last Modified: Tue, 13 Jul 2021 19:05:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13154635bf5454dfc1d3473e53786ccc2123877921618ffda6adea0defe03a1`  
		Last Modified: Tue, 13 Jul 2021 19:05:46 GMT  
		Size: 91.3 MB (91341389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7ecd187b32672194646c1fafac119499c8acbddd0b81e53859cccf7badfde8`  
		Last Modified: Tue, 13 Jul 2021 19:05:27 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:04125527f956147e18df069b9e58064f03eb6c2b2dd3cdbe3ed3caa2dafbfcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:239e4679d65d9a44c983072b52312f8cbfaf505a805090aa97d1a65266c82669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124305174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5769943918c67f6492a009979e758470c83b2de2a83d1716402f1d4009b78479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:40:54 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:40:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:17 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:18 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44c338f719da6a7548fc4e647b9bd52225c5df3e2302badd4a3636d4ada6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0477462ca83c7a80d659335ac0c0d7eadd33db5bf3497027907f7c417dd036c5`  
		Last Modified: Tue, 13 Jul 2021 23:45:32 GMT  
		Size: 86.1 MB (86099760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af6cce3f74250abc9bdff500887dc7967e9af3afde38f6d863fde77572ed62`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e83376a3a79780723ee2f77623bca0817d59cac7d5edd216700e596ab9344b2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137504069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483574e8cdb21e02f00261a7f79687f57f662824805f3a9b2c2d43e35ebf08a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:26:26 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:36 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:41 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:31:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:32:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:32:16 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:27 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:32:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fef03d4d8ec5fdbff5a48b3b0bd2e4b89871abaea39af1025a6c3c13bc5a05`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99414d7cf31143b328d34986107ab9144e1e311e6bae8d5686c17b2a8faa43`  
		Last Modified: Tue, 13 Jul 2021 19:04:55 GMT  
		Size: 91.3 MB (91306505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704b6e12ccce455e8980f637eee2cc9c2dc93e364a9dc504ed7d1073f107f7d2`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:04125527f956147e18df069b9e58064f03eb6c2b2dd3cdbe3ed3caa2dafbfcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:239e4679d65d9a44c983072b52312f8cbfaf505a805090aa97d1a65266c82669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124305174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5769943918c67f6492a009979e758470c83b2de2a83d1716402f1d4009b78479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:40:54 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:40:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:17 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:18 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44c338f719da6a7548fc4e647b9bd52225c5df3e2302badd4a3636d4ada6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0477462ca83c7a80d659335ac0c0d7eadd33db5bf3497027907f7c417dd036c5`  
		Last Modified: Tue, 13 Jul 2021 23:45:32 GMT  
		Size: 86.1 MB (86099760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af6cce3f74250abc9bdff500887dc7967e9af3afde38f6d863fde77572ed62`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e83376a3a79780723ee2f77623bca0817d59cac7d5edd216700e596ab9344b2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137504069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483574e8cdb21e02f00261a7f79687f57f662824805f3a9b2c2d43e35ebf08a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:26:26 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:36 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:41 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:31:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:32:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:32:16 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:27 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:32:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fef03d4d8ec5fdbff5a48b3b0bd2e4b89871abaea39af1025a6c3c13bc5a05`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99414d7cf31143b328d34986107ab9144e1e311e6bae8d5686c17b2a8faa43`  
		Last Modified: Tue, 13 Jul 2021 19:04:55 GMT  
		Size: 91.3 MB (91306505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704b6e12ccce455e8980f637eee2cc9c2dc93e364a9dc504ed7d1073f107f7d2`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.3`

```console
$ docker pull mariadb@sha256:04125527f956147e18df069b9e58064f03eb6c2b2dd3cdbe3ed3caa2dafbfcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.3` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:239e4679d65d9a44c983072b52312f8cbfaf505a805090aa97d1a65266c82669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124305174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5769943918c67f6492a009979e758470c83b2de2a83d1716402f1d4009b78479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:40:54 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:40:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:17 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:18 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44c338f719da6a7548fc4e647b9bd52225c5df3e2302badd4a3636d4ada6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0477462ca83c7a80d659335ac0c0d7eadd33db5bf3497027907f7c417dd036c5`  
		Last Modified: Tue, 13 Jul 2021 23:45:32 GMT  
		Size: 86.1 MB (86099760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af6cce3f74250abc9bdff500887dc7967e9af3afde38f6d863fde77572ed62`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e83376a3a79780723ee2f77623bca0817d59cac7d5edd216700e596ab9344b2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137504069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483574e8cdb21e02f00261a7f79687f57f662824805f3a9b2c2d43e35ebf08a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:26:26 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:36 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:41 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:31:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:32:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:32:16 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:27 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:32:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fef03d4d8ec5fdbff5a48b3b0bd2e4b89871abaea39af1025a6c3c13bc5a05`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99414d7cf31143b328d34986107ab9144e1e311e6bae8d5686c17b2a8faa43`  
		Last Modified: Tue, 13 Jul 2021 19:04:55 GMT  
		Size: 91.3 MB (91306505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704b6e12ccce455e8980f637eee2cc9c2dc93e364a9dc504ed7d1073f107f7d2`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.3-focal`

```console
$ docker pull mariadb@sha256:04125527f956147e18df069b9e58064f03eb6c2b2dd3cdbe3ed3caa2dafbfcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:239e4679d65d9a44c983072b52312f8cbfaf505a805090aa97d1a65266c82669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124305174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5769943918c67f6492a009979e758470c83b2de2a83d1716402f1d4009b78479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:40:54 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:40:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:17 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:18 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44c338f719da6a7548fc4e647b9bd52225c5df3e2302badd4a3636d4ada6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0477462ca83c7a80d659335ac0c0d7eadd33db5bf3497027907f7c417dd036c5`  
		Last Modified: Tue, 13 Jul 2021 23:45:32 GMT  
		Size: 86.1 MB (86099760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af6cce3f74250abc9bdff500887dc7967e9af3afde38f6d863fde77572ed62`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e83376a3a79780723ee2f77623bca0817d59cac7d5edd216700e596ab9344b2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137504069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483574e8cdb21e02f00261a7f79687f57f662824805f3a9b2c2d43e35ebf08a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:26:26 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:36 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:41 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:31:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:32:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:32:16 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:27 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:32:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fef03d4d8ec5fdbff5a48b3b0bd2e4b89871abaea39af1025a6c3c13bc5a05`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99414d7cf31143b328d34986107ab9144e1e311e6bae8d5686c17b2a8faa43`  
		Last Modified: Tue, 13 Jul 2021 19:04:55 GMT  
		Size: 91.3 MB (91306505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704b6e12ccce455e8980f637eee2cc9c2dc93e364a9dc504ed7d1073f107f7d2`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:04125527f956147e18df069b9e58064f03eb6c2b2dd3cdbe3ed3caa2dafbfcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:239e4679d65d9a44c983072b52312f8cbfaf505a805090aa97d1a65266c82669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124305174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5769943918c67f6492a009979e758470c83b2de2a83d1716402f1d4009b78479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:40:54 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:40:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:17 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:18 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44c338f719da6a7548fc4e647b9bd52225c5df3e2302badd4a3636d4ada6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0477462ca83c7a80d659335ac0c0d7eadd33db5bf3497027907f7c417dd036c5`  
		Last Modified: Tue, 13 Jul 2021 23:45:32 GMT  
		Size: 86.1 MB (86099760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af6cce3f74250abc9bdff500887dc7967e9af3afde38f6d863fde77572ed62`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e83376a3a79780723ee2f77623bca0817d59cac7d5edd216700e596ab9344b2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137504069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483574e8cdb21e02f00261a7f79687f57f662824805f3a9b2c2d43e35ebf08a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:26:26 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:36 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:41 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:31:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:32:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:32:16 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:27 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:32:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fef03d4d8ec5fdbff5a48b3b0bd2e4b89871abaea39af1025a6c3c13bc5a05`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99414d7cf31143b328d34986107ab9144e1e311e6bae8d5686c17b2a8faa43`  
		Last Modified: Tue, 13 Jul 2021 19:04:55 GMT  
		Size: 91.3 MB (91306505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704b6e12ccce455e8980f637eee2cc9c2dc93e364a9dc504ed7d1073f107f7d2`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:04125527f956147e18df069b9e58064f03eb6c2b2dd3cdbe3ed3caa2dafbfcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:239e4679d65d9a44c983072b52312f8cbfaf505a805090aa97d1a65266c82669
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124305174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5769943918c67f6492a009979e758470c83b2de2a83d1716402f1d4009b78479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:40:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 23:40:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:29 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 23:40:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:40:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:40:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 23:40:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:40:54 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 23:40:55 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 23:40:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 23:40:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 23:41:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 23:41:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 23:41:17 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:41:18 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 23:41:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866247a8c244dc65add23238c2be8aa4860fb8463050c215ed786bb4a39b29c`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d83b1c8ef82d33928af5183a83be2534a72522727ed2de9041c24b82b3c16`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 5.5 MB (5455146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a77417ecdb153ca7a104f3a35e99fe0c9ffbc8fb2ce8ce543cc95c108db6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:20 GMT  
		Size: 3.4 MB (3367280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451fd044ee319a728a9c2e769b5a430ae91313fe520417d7a885d86f8b8a435f`  
		Last Modified: Tue, 13 Jul 2021 23:45:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cb10aa0678e7db1d957917646d80aa856048258f79128ad45b59741de94b0`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.2 MB (2203601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b43a94638739874436239325e26cbdf7cbbe69cc50ca4f1b3e25066281b23f`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44c338f719da6a7548fc4e647b9bd52225c5df3e2302badd4a3636d4ada6ee`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0477462ca83c7a80d659335ac0c0d7eadd33db5bf3497027907f7c417dd036c5`  
		Last Modified: Tue, 13 Jul 2021 23:45:32 GMT  
		Size: 86.1 MB (86099760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af6cce3f74250abc9bdff500887dc7967e9af3afde38f6d863fde77572ed62`  
		Last Modified: Tue, 13 Jul 2021 23:45:17 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e83376a3a79780723ee2f77623bca0817d59cac7d5edd216700e596ab9344b2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137504069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483574e8cdb21e02f00261a7f79687f57f662824805f3a9b2c2d43e35ebf08a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 18:21:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Jul 2021 18:23:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:23:28 GMT
ENV GOSU_VERSION=1.13
# Tue, 13 Jul 2021 18:24:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 18:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 18:25:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 18:26:00 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 13 Jul 2021 18:26:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 18:26:26 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 13 Jul 2021 18:26:36 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:41 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Tue, 13 Jul 2021 18:26:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Tue, 13 Jul 2021 18:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 13 Jul 2021 18:31:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 13 Jul 2021 18:32:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Jul 2021 18:32:16 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Tue, 13 Jul 2021 18:32:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:27 GMT
EXPOSE 3306
# Tue, 13 Jul 2021 18:32:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabec7e267782eb04117e151b4ae19dbd31828ac2327aa93ceb2e762f739708`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957801e75b45ced792206a25e9311ed87151bf7d982ccf96992cce8b662053cd`  
		Last Modified: Tue, 13 Jul 2021 19:04:41 GMT  
		Size: 6.7 MB (6668034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8978e5ad4aae012ca56e61e9ed998a3174b826149ab640e7be855f155a590`  
		Last Modified: Tue, 13 Jul 2021 19:04:40 GMT  
		Size: 3.7 MB (3670940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac67211566b51edb92685cb1614825334340a130bee9ab9e779b7f59b12cff4`  
		Last Modified: Tue, 13 Jul 2021 19:04:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eef40a00322a6a1bd02a11873d77eed0ffc51bce8069d4a33c1e4cb19b25b1`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.6 MB (2570014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe88f0e23af781797ca57a993657d37f40c970b0f1c34648b770da1c3b60f99`  
		Last Modified: Tue, 13 Jul 2021 19:04:36 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fef03d4d8ec5fdbff5a48b3b0bd2e4b89871abaea39af1025a6c3c13bc5a05`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99414d7cf31143b328d34986107ab9144e1e311e6bae8d5686c17b2a8faa43`  
		Last Modified: Tue, 13 Jul 2021 19:04:55 GMT  
		Size: 91.3 MB (91306505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704b6e12ccce455e8980f637eee2cc9c2dc93e364a9dc504ed7d1073f107f7d2`  
		Last Modified: Tue, 13 Jul 2021 19:04:35 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
