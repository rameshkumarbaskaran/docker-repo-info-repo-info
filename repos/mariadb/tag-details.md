<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.38`](#mariadb10238)
-	[`mariadb:10.2.38-bionic`](#mariadb10238-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.29`](#mariadb10329)
-	[`mariadb:10.3.29-focal`](#mariadb10329-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.19`](#mariadb10419)
-	[`mariadb:10.4.19-focal`](#mariadb10419-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.10`](#mariadb10510)
-	[`mariadb:10.5.10-focal`](#mariadb10510-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.1`](#mariadb1061)
-	[`mariadb:10.6.1-focal`](#mariadb1061-focal)
-	[`mariadb:beta`](#mariadbbeta)
-	[`mariadb:beta-focal`](#mariadbbeta-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:be1b339b181ba9f4f95d3aebed9c88ada73273f9474f8413e3fcd1d11e64cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:ca4b2789ac74d0e7c1f9fe32c66a100115ab77d50298158e81fb7e55451a016e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126882173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d89055e5ca272ed7d5da8019d5f92dab1ca588704ffb069829ff723b1fcd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 04:57:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:50 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:50 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb173802fc8683da7adc0f470fbc24dbd74bd845bc7cab75baa6895934e8ae`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2f79f6e6e7563887ee568524407a5c92cee94c22ec47bf46378218ab0be25d`  
		Last Modified: Fri, 18 Jun 2021 05:02:09 GMT  
		Size: 86.9 MB (86939363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2faf917bfb21b3be0ab8246736bca42c357831b873cf405c4f10e153e35c90`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a245b8604e5653edd82713f107d13fc9aef08210c51f5575682997dbedcb384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137576307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62822aca60556dacde47fa40c413245c5cfe3cd9fa3e586a6c6fa65d401d0389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:41:08 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 02:41:14 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 02:41:21 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:44:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:45:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:45:12 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:45:24 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:45:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e4a51f683a867a9b9940cab2319fe7761520236e4d3bb7d8bff8c3e6b2b31b`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17466f0a629dce0359714b749814b8513747e81dbcb854c3cb7d730f638b294b`  
		Last Modified: Fri, 18 Jun 2021 03:04:08 GMT  
		Size: 91.3 MB (91324318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f253cd53c36c6ac73a52fc3a015c8307a251d301d69070270ddd98197941e`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:be1b339b181ba9f4f95d3aebed9c88ada73273f9474f8413e3fcd1d11e64cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:ca4b2789ac74d0e7c1f9fe32c66a100115ab77d50298158e81fb7e55451a016e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126882173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d89055e5ca272ed7d5da8019d5f92dab1ca588704ffb069829ff723b1fcd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 04:57:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:50 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:50 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb173802fc8683da7adc0f470fbc24dbd74bd845bc7cab75baa6895934e8ae`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2f79f6e6e7563887ee568524407a5c92cee94c22ec47bf46378218ab0be25d`  
		Last Modified: Fri, 18 Jun 2021 05:02:09 GMT  
		Size: 86.9 MB (86939363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2faf917bfb21b3be0ab8246736bca42c357831b873cf405c4f10e153e35c90`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a245b8604e5653edd82713f107d13fc9aef08210c51f5575682997dbedcb384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137576307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62822aca60556dacde47fa40c413245c5cfe3cd9fa3e586a6c6fa65d401d0389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:41:08 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 02:41:14 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 02:41:21 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:44:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:45:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:45:12 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:45:24 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:45:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e4a51f683a867a9b9940cab2319fe7761520236e4d3bb7d8bff8c3e6b2b31b`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17466f0a629dce0359714b749814b8513747e81dbcb854c3cb7d730f638b294b`  
		Last Modified: Fri, 18 Jun 2021 03:04:08 GMT  
		Size: 91.3 MB (91324318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f253cd53c36c6ac73a52fc3a015c8307a251d301d69070270ddd98197941e`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:29214543ff0ee76c736a87a2fba50f558e9c9b0842defc8dc8f801706c6e0e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:e3bd0d803d905b4e05b145375632e305b0aff4f8d7d4259d41323469ed3e5713
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109325247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d057535e68a6485d1d57071d78709deafd4bd31f32cfb4f4dbdc6852f4a63a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:59:29 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:59:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:59:44 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:59:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:59:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 05:00:10 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 05:00:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 05:00:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 05:00:11 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 05:00:12 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 05:00:13 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 05:00:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 05:00:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 05:00:48 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 05:00:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 05:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 05:00:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 05:00:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d7f527a85d567884b86652e590f5d484b9ab84b150e4925b7d87699f93fea1`  
		Last Modified: Fri, 18 Jun 2021 05:03:42 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffc1a82bccd839baf9aee65bea12f39144d2f71d17f7a478729e5033a3483e`  
		Last Modified: Fri, 18 Jun 2021 05:03:41 GMT  
		Size: 4.8 MB (4813831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499ae120a92cf69045b499c6e9acb4746dd8021ca8ad5f655d75ba962e197ae7`  
		Last Modified: Fri, 18 Jun 2021 05:03:41 GMT  
		Size: 3.6 MB (3586283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1026105733a2b0dd715260634aaa9732338ff49ff7893ebb9f536c4a0426cf9`  
		Last Modified: Fri, 18 Jun 2021 05:03:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bac60c3e9fdd643565e5a529771c84d07d037eea7fc536305a2fea14df6b6e`  
		Last Modified: Fri, 18 Jun 2021 05:03:40 GMT  
		Size: 1.6 MB (1586353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a653fb76f6ce606f18dd610531fc02f7a8c20d238663a411d947e88ed94fc8c5`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327c24fb71c5e64a91d1a2ee5b01b14a8bba3eb0d74a8c00617b22cca76a9c84`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93199981c2aa0ce26a3d17f67ecb0f03e0f051a2c87f7d5cfe2af6d7897d0cd0`  
		Last Modified: Fri, 18 Jun 2021 05:03:53 GMT  
		Size: 72.6 MB (72624882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058762c3c8cf9767892d8d7663b3bc9248da01aece8d63db504287e255cf876`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84e5966efde401000fa8bcbdf335340d6bf18b52b1c4ed4e24c58a4bf416e99`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7b1a1ff4e326f56971555cfcbf4db5c1e4b23bec5507c855edbb2852d4e662e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104332994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291bcc00a47b79f17b38d111e9999ddf5ba59c0b6cf38c532f21673df3a638a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:50 GMT
ADD file:1c098d4ee63884766899c72e542e107525f0b7ade5528de87642587389864bcc in / 
# Thu, 17 Jun 2021 23:53:51 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:48:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:49:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:06 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:49:20 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:49:28 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:49:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:49:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 00:49:30 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 00:49:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:49:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:49:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:49:55 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:49:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:49:56 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:49:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:55c604a74c4b0b41ef666f811f5e160693236be8ea130c6df723480f59cbb9b8`  
		Last Modified: Thu, 17 Jun 2021 23:55:41 GMT  
		Size: 23.7 MB (23728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d37d33072a857afa7a7c06848aba6896f13885f8f60b3288503be9131f7d1`  
		Last Modified: Fri, 18 Jun 2021 00:54:00 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5240ac600f4c5cb6f6e1e67752ff54f6ea68150858733712e557f7769cf0ec94`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 4.4 MB (4395498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e9bdca319f24e8555f3cc5cb0acb5431f17160b3f7d1ace9bc0d7d2dd080c`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 3.2 MB (3247122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae8ab6f6a79453a733f4e0dd53ce34be50da7dff4919815b2649f1b095974e`  
		Last Modified: Fri, 18 Jun 2021 00:53:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ebc4960024e7df847b1995a4d1e11c2f81ae4edbead7f68449c74383fa911`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 1.5 MB (1532347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8c8f439f7efa7e04a46f45243abad39666469cb385e0299cb542a9bbdd56b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99574e259d6718e436f1f0ab6d909f8c69bcce6b13b1bde103af2271daa9007b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad85a7503ad56c12cdfcd667090e916b05f1d668c267105cb26d70634ff6f7e5`  
		Last Modified: Fri, 18 Jun 2021 00:54:07 GMT  
		Size: 71.4 MB (71416655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfea2eb314ce55b831611e3d40eb0a1362e0ef0346342a907d4f29763b214`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbce75f791185b5361c4bec16b7d33a7ec64fac370f69625c3e5322dfe53ae6`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:54915b4f249dcd4396a2b282ad0b19115b267aff7e91a2c291d76182a1427350
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117673163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cb1eb98fc85074b87fba443f1cb60dd0896e28d275c9a7cfabc3c2b6fc05bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:54:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:56:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:56:15 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:56:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:57:59 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:58:05 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:58:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:58:26 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 02:58:31 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 02:58:41 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 03:01:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 03:01:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 03:01:34 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 03:01:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 03:01:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 03:01:58 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 03:02:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3af44a6beabcd2b603da746b157e55dee62f2a14b730d5e5148d32525712b`  
		Last Modified: Fri, 18 Jun 2021 03:05:56 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27be2226c864d17eb448038b50b60568b10f6aaece2f78d586761d64da019d7f`  
		Last Modified: Fri, 18 Jun 2021 03:05:54 GMT  
		Size: 5.6 MB (5630493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fa716ade46f6351173d6e4409bcfd8d66b20a1afe34a6fad238320e5216104`  
		Last Modified: Fri, 18 Jun 2021 03:05:53 GMT  
		Size: 3.6 MB (3584735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c3777fff0af4d7e256e3c0ef6f069b23fbe190464ab5be5f5a00cc41d15797`  
		Last Modified: Fri, 18 Jun 2021 03:05:52 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4274dc17263656c73d4b038214a098cf8b313ade40614b830cea6d0f09ca9c`  
		Last Modified: Fri, 18 Jun 2021 03:05:53 GMT  
		Size: 1.9 MB (1938724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7a9a47e10f1c4737e8178b5c0a0c02b96b086c4c4f73c457428944593a06d3`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c7fb36f081c214c2bb06d1c704526fc6529d3618ea803ea60792c32b02f1a9`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5e8c6bb30249b712767233ac32cfe1896110791e47404d53a95ac9197b8b2f`  
		Last Modified: Fri, 18 Jun 2021 03:06:05 GMT  
		Size: 76.1 MB (76080650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a009d1160129d0c6f3436955d89142bc3e72ba1243aa0f86b727cd5f0b3196d`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae44fcb48914e64041394b463b7d7133788e637930f575569d641beec6bb5571`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:29214543ff0ee76c736a87a2fba50f558e9c9b0842defc8dc8f801706c6e0e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:e3bd0d803d905b4e05b145375632e305b0aff4f8d7d4259d41323469ed3e5713
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109325247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d057535e68a6485d1d57071d78709deafd4bd31f32cfb4f4dbdc6852f4a63a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:59:29 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:59:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:59:44 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:59:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:59:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 05:00:10 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 05:00:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 05:00:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 05:00:11 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 05:00:12 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 05:00:13 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 05:00:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 05:00:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 05:00:48 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 05:00:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 05:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 05:00:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 05:00:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d7f527a85d567884b86652e590f5d484b9ab84b150e4925b7d87699f93fea1`  
		Last Modified: Fri, 18 Jun 2021 05:03:42 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffc1a82bccd839baf9aee65bea12f39144d2f71d17f7a478729e5033a3483e`  
		Last Modified: Fri, 18 Jun 2021 05:03:41 GMT  
		Size: 4.8 MB (4813831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499ae120a92cf69045b499c6e9acb4746dd8021ca8ad5f655d75ba962e197ae7`  
		Last Modified: Fri, 18 Jun 2021 05:03:41 GMT  
		Size: 3.6 MB (3586283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1026105733a2b0dd715260634aaa9732338ff49ff7893ebb9f536c4a0426cf9`  
		Last Modified: Fri, 18 Jun 2021 05:03:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bac60c3e9fdd643565e5a529771c84d07d037eea7fc536305a2fea14df6b6e`  
		Last Modified: Fri, 18 Jun 2021 05:03:40 GMT  
		Size: 1.6 MB (1586353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a653fb76f6ce606f18dd610531fc02f7a8c20d238663a411d947e88ed94fc8c5`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327c24fb71c5e64a91d1a2ee5b01b14a8bba3eb0d74a8c00617b22cca76a9c84`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93199981c2aa0ce26a3d17f67ecb0f03e0f051a2c87f7d5cfe2af6d7897d0cd0`  
		Last Modified: Fri, 18 Jun 2021 05:03:53 GMT  
		Size: 72.6 MB (72624882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058762c3c8cf9767892d8d7663b3bc9248da01aece8d63db504287e255cf876`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84e5966efde401000fa8bcbdf335340d6bf18b52b1c4ed4e24c58a4bf416e99`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7b1a1ff4e326f56971555cfcbf4db5c1e4b23bec5507c855edbb2852d4e662e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104332994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291bcc00a47b79f17b38d111e9999ddf5ba59c0b6cf38c532f21673df3a638a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:50 GMT
ADD file:1c098d4ee63884766899c72e542e107525f0b7ade5528de87642587389864bcc in / 
# Thu, 17 Jun 2021 23:53:51 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:48:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:49:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:06 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:49:20 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:49:28 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:49:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:49:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 00:49:30 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 00:49:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:49:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:49:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:49:55 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:49:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:49:56 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:49:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:55c604a74c4b0b41ef666f811f5e160693236be8ea130c6df723480f59cbb9b8`  
		Last Modified: Thu, 17 Jun 2021 23:55:41 GMT  
		Size: 23.7 MB (23728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d37d33072a857afa7a7c06848aba6896f13885f8f60b3288503be9131f7d1`  
		Last Modified: Fri, 18 Jun 2021 00:54:00 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5240ac600f4c5cb6f6e1e67752ff54f6ea68150858733712e557f7769cf0ec94`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 4.4 MB (4395498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e9bdca319f24e8555f3cc5cb0acb5431f17160b3f7d1ace9bc0d7d2dd080c`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 3.2 MB (3247122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae8ab6f6a79453a733f4e0dd53ce34be50da7dff4919815b2649f1b095974e`  
		Last Modified: Fri, 18 Jun 2021 00:53:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ebc4960024e7df847b1995a4d1e11c2f81ae4edbead7f68449c74383fa911`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 1.5 MB (1532347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8c8f439f7efa7e04a46f45243abad39666469cb385e0299cb542a9bbdd56b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99574e259d6718e436f1f0ab6d909f8c69bcce6b13b1bde103af2271daa9007b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad85a7503ad56c12cdfcd667090e916b05f1d668c267105cb26d70634ff6f7e5`  
		Last Modified: Fri, 18 Jun 2021 00:54:07 GMT  
		Size: 71.4 MB (71416655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfea2eb314ce55b831611e3d40eb0a1362e0ef0346342a907d4f29763b214`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbce75f791185b5361c4bec16b7d33a7ec64fac370f69625c3e5322dfe53ae6`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:54915b4f249dcd4396a2b282ad0b19115b267aff7e91a2c291d76182a1427350
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117673163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cb1eb98fc85074b87fba443f1cb60dd0896e28d275c9a7cfabc3c2b6fc05bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:54:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:56:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:56:15 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:56:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:57:59 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:58:05 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:58:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:58:26 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 02:58:31 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 02:58:41 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 03:01:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 03:01:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 03:01:34 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 03:01:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 03:01:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 03:01:58 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 03:02:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3af44a6beabcd2b603da746b157e55dee62f2a14b730d5e5148d32525712b`  
		Last Modified: Fri, 18 Jun 2021 03:05:56 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27be2226c864d17eb448038b50b60568b10f6aaece2f78d586761d64da019d7f`  
		Last Modified: Fri, 18 Jun 2021 03:05:54 GMT  
		Size: 5.6 MB (5630493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fa716ade46f6351173d6e4409bcfd8d66b20a1afe34a6fad238320e5216104`  
		Last Modified: Fri, 18 Jun 2021 03:05:53 GMT  
		Size: 3.6 MB (3584735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c3777fff0af4d7e256e3c0ef6f069b23fbe190464ab5be5f5a00cc41d15797`  
		Last Modified: Fri, 18 Jun 2021 03:05:52 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4274dc17263656c73d4b038214a098cf8b313ade40614b830cea6d0f09ca9c`  
		Last Modified: Fri, 18 Jun 2021 03:05:53 GMT  
		Size: 1.9 MB (1938724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7a9a47e10f1c4737e8178b5c0a0c02b96b086c4c4f73c457428944593a06d3`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c7fb36f081c214c2bb06d1c704526fc6529d3618ea803ea60792c32b02f1a9`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5e8c6bb30249b712767233ac32cfe1896110791e47404d53a95ac9197b8b2f`  
		Last Modified: Fri, 18 Jun 2021 03:06:05 GMT  
		Size: 76.1 MB (76080650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a009d1160129d0c6f3436955d89142bc3e72ba1243aa0f86b727cd5f0b3196d`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae44fcb48914e64041394b463b7d7133788e637930f575569d641beec6bb5571`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.38`

```console
$ docker pull mariadb@sha256:29214543ff0ee76c736a87a2fba50f558e9c9b0842defc8dc8f801706c6e0e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.38` - linux; amd64

```console
$ docker pull mariadb@sha256:e3bd0d803d905b4e05b145375632e305b0aff4f8d7d4259d41323469ed3e5713
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109325247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d057535e68a6485d1d57071d78709deafd4bd31f32cfb4f4dbdc6852f4a63a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:59:29 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:59:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:59:44 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:59:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:59:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 05:00:10 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 05:00:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 05:00:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 05:00:11 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 05:00:12 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 05:00:13 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 05:00:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 05:00:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 05:00:48 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 05:00:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 05:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 05:00:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 05:00:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d7f527a85d567884b86652e590f5d484b9ab84b150e4925b7d87699f93fea1`  
		Last Modified: Fri, 18 Jun 2021 05:03:42 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffc1a82bccd839baf9aee65bea12f39144d2f71d17f7a478729e5033a3483e`  
		Last Modified: Fri, 18 Jun 2021 05:03:41 GMT  
		Size: 4.8 MB (4813831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499ae120a92cf69045b499c6e9acb4746dd8021ca8ad5f655d75ba962e197ae7`  
		Last Modified: Fri, 18 Jun 2021 05:03:41 GMT  
		Size: 3.6 MB (3586283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1026105733a2b0dd715260634aaa9732338ff49ff7893ebb9f536c4a0426cf9`  
		Last Modified: Fri, 18 Jun 2021 05:03:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bac60c3e9fdd643565e5a529771c84d07d037eea7fc536305a2fea14df6b6e`  
		Last Modified: Fri, 18 Jun 2021 05:03:40 GMT  
		Size: 1.6 MB (1586353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a653fb76f6ce606f18dd610531fc02f7a8c20d238663a411d947e88ed94fc8c5`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327c24fb71c5e64a91d1a2ee5b01b14a8bba3eb0d74a8c00617b22cca76a9c84`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93199981c2aa0ce26a3d17f67ecb0f03e0f051a2c87f7d5cfe2af6d7897d0cd0`  
		Last Modified: Fri, 18 Jun 2021 05:03:53 GMT  
		Size: 72.6 MB (72624882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058762c3c8cf9767892d8d7663b3bc9248da01aece8d63db504287e255cf876`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84e5966efde401000fa8bcbdf335340d6bf18b52b1c4ed4e24c58a4bf416e99`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.38` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7b1a1ff4e326f56971555cfcbf4db5c1e4b23bec5507c855edbb2852d4e662e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104332994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291bcc00a47b79f17b38d111e9999ddf5ba59c0b6cf38c532f21673df3a638a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:50 GMT
ADD file:1c098d4ee63884766899c72e542e107525f0b7ade5528de87642587389864bcc in / 
# Thu, 17 Jun 2021 23:53:51 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:48:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:49:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:06 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:49:20 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:49:28 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:49:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:49:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 00:49:30 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 00:49:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:49:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:49:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:49:55 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:49:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:49:56 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:49:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:55c604a74c4b0b41ef666f811f5e160693236be8ea130c6df723480f59cbb9b8`  
		Last Modified: Thu, 17 Jun 2021 23:55:41 GMT  
		Size: 23.7 MB (23728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d37d33072a857afa7a7c06848aba6896f13885f8f60b3288503be9131f7d1`  
		Last Modified: Fri, 18 Jun 2021 00:54:00 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5240ac600f4c5cb6f6e1e67752ff54f6ea68150858733712e557f7769cf0ec94`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 4.4 MB (4395498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e9bdca319f24e8555f3cc5cb0acb5431f17160b3f7d1ace9bc0d7d2dd080c`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 3.2 MB (3247122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae8ab6f6a79453a733f4e0dd53ce34be50da7dff4919815b2649f1b095974e`  
		Last Modified: Fri, 18 Jun 2021 00:53:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ebc4960024e7df847b1995a4d1e11c2f81ae4edbead7f68449c74383fa911`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 1.5 MB (1532347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8c8f439f7efa7e04a46f45243abad39666469cb385e0299cb542a9bbdd56b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99574e259d6718e436f1f0ab6d909f8c69bcce6b13b1bde103af2271daa9007b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad85a7503ad56c12cdfcd667090e916b05f1d668c267105cb26d70634ff6f7e5`  
		Last Modified: Fri, 18 Jun 2021 00:54:07 GMT  
		Size: 71.4 MB (71416655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfea2eb314ce55b831611e3d40eb0a1362e0ef0346342a907d4f29763b214`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbce75f791185b5361c4bec16b7d33a7ec64fac370f69625c3e5322dfe53ae6`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.38` - linux; ppc64le

```console
$ docker pull mariadb@sha256:54915b4f249dcd4396a2b282ad0b19115b267aff7e91a2c291d76182a1427350
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117673163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cb1eb98fc85074b87fba443f1cb60dd0896e28d275c9a7cfabc3c2b6fc05bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:54:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:56:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:56:15 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:56:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:57:59 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:58:05 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:58:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:58:26 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 02:58:31 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 02:58:41 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 03:01:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 03:01:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 03:01:34 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 03:01:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 03:01:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 03:01:58 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 03:02:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3af44a6beabcd2b603da746b157e55dee62f2a14b730d5e5148d32525712b`  
		Last Modified: Fri, 18 Jun 2021 03:05:56 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27be2226c864d17eb448038b50b60568b10f6aaece2f78d586761d64da019d7f`  
		Last Modified: Fri, 18 Jun 2021 03:05:54 GMT  
		Size: 5.6 MB (5630493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fa716ade46f6351173d6e4409bcfd8d66b20a1afe34a6fad238320e5216104`  
		Last Modified: Fri, 18 Jun 2021 03:05:53 GMT  
		Size: 3.6 MB (3584735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c3777fff0af4d7e256e3c0ef6f069b23fbe190464ab5be5f5a00cc41d15797`  
		Last Modified: Fri, 18 Jun 2021 03:05:52 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4274dc17263656c73d4b038214a098cf8b313ade40614b830cea6d0f09ca9c`  
		Last Modified: Fri, 18 Jun 2021 03:05:53 GMT  
		Size: 1.9 MB (1938724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7a9a47e10f1c4737e8178b5c0a0c02b96b086c4c4f73c457428944593a06d3`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c7fb36f081c214c2bb06d1c704526fc6529d3618ea803ea60792c32b02f1a9`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5e8c6bb30249b712767233ac32cfe1896110791e47404d53a95ac9197b8b2f`  
		Last Modified: Fri, 18 Jun 2021 03:06:05 GMT  
		Size: 76.1 MB (76080650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a009d1160129d0c6f3436955d89142bc3e72ba1243aa0f86b727cd5f0b3196d`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae44fcb48914e64041394b463b7d7133788e637930f575569d641beec6bb5571`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.38-bionic`

```console
$ docker pull mariadb@sha256:29214543ff0ee76c736a87a2fba50f558e9c9b0842defc8dc8f801706c6e0e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.38-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:e3bd0d803d905b4e05b145375632e305b0aff4f8d7d4259d41323469ed3e5713
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109325247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d057535e68a6485d1d57071d78709deafd4bd31f32cfb4f4dbdc6852f4a63a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:59:29 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:59:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:59:44 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:59:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:59:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 05:00:10 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 05:00:10 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 05:00:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 05:00:11 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 05:00:12 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 05:00:13 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 05:00:47 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 05:00:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 05:00:48 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 05:00:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 05:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 05:00:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 05:00:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d7f527a85d567884b86652e590f5d484b9ab84b150e4925b7d87699f93fea1`  
		Last Modified: Fri, 18 Jun 2021 05:03:42 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffc1a82bccd839baf9aee65bea12f39144d2f71d17f7a478729e5033a3483e`  
		Last Modified: Fri, 18 Jun 2021 05:03:41 GMT  
		Size: 4.8 MB (4813831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499ae120a92cf69045b499c6e9acb4746dd8021ca8ad5f655d75ba962e197ae7`  
		Last Modified: Fri, 18 Jun 2021 05:03:41 GMT  
		Size: 3.6 MB (3586283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1026105733a2b0dd715260634aaa9732338ff49ff7893ebb9f536c4a0426cf9`  
		Last Modified: Fri, 18 Jun 2021 05:03:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bac60c3e9fdd643565e5a529771c84d07d037eea7fc536305a2fea14df6b6e`  
		Last Modified: Fri, 18 Jun 2021 05:03:40 GMT  
		Size: 1.6 MB (1586353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a653fb76f6ce606f18dd610531fc02f7a8c20d238663a411d947e88ed94fc8c5`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327c24fb71c5e64a91d1a2ee5b01b14a8bba3eb0d74a8c00617b22cca76a9c84`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93199981c2aa0ce26a3d17f67ecb0f03e0f051a2c87f7d5cfe2af6d7897d0cd0`  
		Last Modified: Fri, 18 Jun 2021 05:03:53 GMT  
		Size: 72.6 MB (72624882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058762c3c8cf9767892d8d7663b3bc9248da01aece8d63db504287e255cf876`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84e5966efde401000fa8bcbdf335340d6bf18b52b1c4ed4e24c58a4bf416e99`  
		Last Modified: Fri, 18 Jun 2021 05:03:37 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.38-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7b1a1ff4e326f56971555cfcbf4db5c1e4b23bec5507c855edbb2852d4e662e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104332994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291bcc00a47b79f17b38d111e9999ddf5ba59c0b6cf38c532f21673df3a638a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:50 GMT
ADD file:1c098d4ee63884766899c72e542e107525f0b7ade5528de87642587389864bcc in / 
# Thu, 17 Jun 2021 23:53:51 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:48:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:49:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:06 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:49:20 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:49:28 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:49:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:49:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 00:49:30 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 00:49:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:49:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:49:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:49:55 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:49:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:49:56 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:49:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:55c604a74c4b0b41ef666f811f5e160693236be8ea130c6df723480f59cbb9b8`  
		Last Modified: Thu, 17 Jun 2021 23:55:41 GMT  
		Size: 23.7 MB (23728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d37d33072a857afa7a7c06848aba6896f13885f8f60b3288503be9131f7d1`  
		Last Modified: Fri, 18 Jun 2021 00:54:00 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5240ac600f4c5cb6f6e1e67752ff54f6ea68150858733712e557f7769cf0ec94`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 4.4 MB (4395498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e9bdca319f24e8555f3cc5cb0acb5431f17160b3f7d1ace9bc0d7d2dd080c`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 3.2 MB (3247122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae8ab6f6a79453a733f4e0dd53ce34be50da7dff4919815b2649f1b095974e`  
		Last Modified: Fri, 18 Jun 2021 00:53:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ebc4960024e7df847b1995a4d1e11c2f81ae4edbead7f68449c74383fa911`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 1.5 MB (1532347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8c8f439f7efa7e04a46f45243abad39666469cb385e0299cb542a9bbdd56b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99574e259d6718e436f1f0ab6d909f8c69bcce6b13b1bde103af2271daa9007b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad85a7503ad56c12cdfcd667090e916b05f1d668c267105cb26d70634ff6f7e5`  
		Last Modified: Fri, 18 Jun 2021 00:54:07 GMT  
		Size: 71.4 MB (71416655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfea2eb314ce55b831611e3d40eb0a1362e0ef0346342a907d4f29763b214`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbce75f791185b5361c4bec16b7d33a7ec64fac370f69625c3e5322dfe53ae6`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.38-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:54915b4f249dcd4396a2b282ad0b19115b267aff7e91a2c291d76182a1427350
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117673163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cb1eb98fc85074b87fba443f1cb60dd0896e28d275c9a7cfabc3c2b6fc05bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:54:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:56:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:56:15 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:56:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:57:59 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:58:05 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:58:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:58:26 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 02:58:31 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 02:58:41 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 03:01:25 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 03:01:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 03:01:34 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 03:01:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 03:01:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 03:01:58 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 03:02:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3af44a6beabcd2b603da746b157e55dee62f2a14b730d5e5148d32525712b`  
		Last Modified: Fri, 18 Jun 2021 03:05:56 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27be2226c864d17eb448038b50b60568b10f6aaece2f78d586761d64da019d7f`  
		Last Modified: Fri, 18 Jun 2021 03:05:54 GMT  
		Size: 5.6 MB (5630493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fa716ade46f6351173d6e4409bcfd8d66b20a1afe34a6fad238320e5216104`  
		Last Modified: Fri, 18 Jun 2021 03:05:53 GMT  
		Size: 3.6 MB (3584735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c3777fff0af4d7e256e3c0ef6f069b23fbe190464ab5be5f5a00cc41d15797`  
		Last Modified: Fri, 18 Jun 2021 03:05:52 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4274dc17263656c73d4b038214a098cf8b313ade40614b830cea6d0f09ca9c`  
		Last Modified: Fri, 18 Jun 2021 03:05:53 GMT  
		Size: 1.9 MB (1938724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7a9a47e10f1c4737e8178b5c0a0c02b96b086c4c4f73c457428944593a06d3`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c7fb36f081c214c2bb06d1c704526fc6529d3618ea803ea60792c32b02f1a9`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5e8c6bb30249b712767233ac32cfe1896110791e47404d53a95ac9197b8b2f`  
		Last Modified: Fri, 18 Jun 2021 03:06:05 GMT  
		Size: 76.1 MB (76080650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a009d1160129d0c6f3436955d89142bc3e72ba1243aa0f86b727cd5f0b3196d`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae44fcb48914e64041394b463b7d7133788e637930f575569d641beec6bb5571`  
		Last Modified: Fri, 18 Jun 2021 03:05:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:a8a03802fcd59d5482ae1996137e6f073be80746e82fc7cf22e934e8d2102e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:b1b6642782ded113856daf31cb48e96b64af861d54182acbd61b6a0e38c70f43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120022754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87f2efbb6ad4decaaa3752613badced2ab82855803e43eda5d25eb6b78f20e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:58:37 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 04:58:37 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 04:58:38 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:59:19 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:59:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:59:19 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:59:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 04:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:59:21 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:59:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34136f02944f1519398da6be3fab15bfb91553e7d4f056d9af5fa9dc23e25776`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b52de8f0a748ab083714bc5b97abb8c490bfa0e62806188309db0dce8e4695c`  
		Last Modified: Fri, 18 Jun 2021 05:03:19 GMT  
		Size: 80.1 MB (80079822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4906eba5fa0d8be69e4653cabb71c7947701324eaa908d573871deb3913d20`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c481ed9c56fa32f74c4aacd0dd2f22a195d7a7f093c3d86b13381995e28f021`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:05ff2732c1990967a3395d6930deb04235372e724c7da356267c3118603ed9b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117617654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276bab2fb248e858dae13121ec7aa60d159c923acd2a52744ba4f039b589e808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 00:48:23 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:47 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760c30d6dbfa45dc14eb4a99ce6717ff04fce410c9df6b19e2316c24e3c0277`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf847301ed0bae6f944b6b36e057cb9bd51224a86f5a2b76935bbb73e5078cbe`  
		Last Modified: Fri, 18 Jun 2021 00:53:35 GMT  
		Size: 79.4 MB (79380839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015aaec3f93fb58e45b19e5781020acfa46c5f58f9225473dfdbdde9ebf9ff61`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163dd26927d877159c8477b3ea75082a5271c65a1c50861d1463690100d7541e`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d5380d75882e95be32377b879b5795887b495bd055db7579f77b9d46d648dfb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130902542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bde91ddd0d12a726bdc83b011f5a3c64e7a9d481b990c19a06940210c0f5f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:50:47 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 02:50:56 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 02:51:08 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:53:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:53:59 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:54:04 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 02:54:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:54:18 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:54:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ff377b76ae8706d5cdeb8c5bb0ac65cd688d5ddeddc54bb9275675896d29c8`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b083c03dbcd716610d1bc087492c90470d5fd01491bd52e78ece7cb166086a39`  
		Last Modified: Fri, 18 Jun 2021 03:05:31 GMT  
		Size: 84.7 MB (84650431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9660ffafc12e71553e85df09e7ac56082ac05c98de2397474a5b62c3d15ba87`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d85e77e75fe69436dd384ba119d006dd97042726fc12258c2df25f9be41ae`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:a8a03802fcd59d5482ae1996137e6f073be80746e82fc7cf22e934e8d2102e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b1b6642782ded113856daf31cb48e96b64af861d54182acbd61b6a0e38c70f43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120022754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87f2efbb6ad4decaaa3752613badced2ab82855803e43eda5d25eb6b78f20e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:58:37 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 04:58:37 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 04:58:38 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:59:19 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:59:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:59:19 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:59:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 04:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:59:21 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:59:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34136f02944f1519398da6be3fab15bfb91553e7d4f056d9af5fa9dc23e25776`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b52de8f0a748ab083714bc5b97abb8c490bfa0e62806188309db0dce8e4695c`  
		Last Modified: Fri, 18 Jun 2021 05:03:19 GMT  
		Size: 80.1 MB (80079822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4906eba5fa0d8be69e4653cabb71c7947701324eaa908d573871deb3913d20`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c481ed9c56fa32f74c4aacd0dd2f22a195d7a7f093c3d86b13381995e28f021`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:05ff2732c1990967a3395d6930deb04235372e724c7da356267c3118603ed9b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117617654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276bab2fb248e858dae13121ec7aa60d159c923acd2a52744ba4f039b589e808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 00:48:23 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:47 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760c30d6dbfa45dc14eb4a99ce6717ff04fce410c9df6b19e2316c24e3c0277`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf847301ed0bae6f944b6b36e057cb9bd51224a86f5a2b76935bbb73e5078cbe`  
		Last Modified: Fri, 18 Jun 2021 00:53:35 GMT  
		Size: 79.4 MB (79380839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015aaec3f93fb58e45b19e5781020acfa46c5f58f9225473dfdbdde9ebf9ff61`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163dd26927d877159c8477b3ea75082a5271c65a1c50861d1463690100d7541e`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d5380d75882e95be32377b879b5795887b495bd055db7579f77b9d46d648dfb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130902542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bde91ddd0d12a726bdc83b011f5a3c64e7a9d481b990c19a06940210c0f5f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:50:47 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 02:50:56 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 02:51:08 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:53:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:53:59 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:54:04 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 02:54:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:54:18 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:54:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ff377b76ae8706d5cdeb8c5bb0ac65cd688d5ddeddc54bb9275675896d29c8`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b083c03dbcd716610d1bc087492c90470d5fd01491bd52e78ece7cb166086a39`  
		Last Modified: Fri, 18 Jun 2021 03:05:31 GMT  
		Size: 84.7 MB (84650431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9660ffafc12e71553e85df09e7ac56082ac05c98de2397474a5b62c3d15ba87`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d85e77e75fe69436dd384ba119d006dd97042726fc12258c2df25f9be41ae`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.29`

```console
$ docker pull mariadb@sha256:a8a03802fcd59d5482ae1996137e6f073be80746e82fc7cf22e934e8d2102e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.29` - linux; amd64

```console
$ docker pull mariadb@sha256:b1b6642782ded113856daf31cb48e96b64af861d54182acbd61b6a0e38c70f43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120022754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87f2efbb6ad4decaaa3752613badced2ab82855803e43eda5d25eb6b78f20e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:58:37 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 04:58:37 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 04:58:38 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:59:19 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:59:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:59:19 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:59:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 04:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:59:21 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:59:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34136f02944f1519398da6be3fab15bfb91553e7d4f056d9af5fa9dc23e25776`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b52de8f0a748ab083714bc5b97abb8c490bfa0e62806188309db0dce8e4695c`  
		Last Modified: Fri, 18 Jun 2021 05:03:19 GMT  
		Size: 80.1 MB (80079822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4906eba5fa0d8be69e4653cabb71c7947701324eaa908d573871deb3913d20`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c481ed9c56fa32f74c4aacd0dd2f22a195d7a7f093c3d86b13381995e28f021`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.29` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:05ff2732c1990967a3395d6930deb04235372e724c7da356267c3118603ed9b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117617654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276bab2fb248e858dae13121ec7aa60d159c923acd2a52744ba4f039b589e808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 00:48:23 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:47 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760c30d6dbfa45dc14eb4a99ce6717ff04fce410c9df6b19e2316c24e3c0277`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf847301ed0bae6f944b6b36e057cb9bd51224a86f5a2b76935bbb73e5078cbe`  
		Last Modified: Fri, 18 Jun 2021 00:53:35 GMT  
		Size: 79.4 MB (79380839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015aaec3f93fb58e45b19e5781020acfa46c5f58f9225473dfdbdde9ebf9ff61`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163dd26927d877159c8477b3ea75082a5271c65a1c50861d1463690100d7541e`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.29` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d5380d75882e95be32377b879b5795887b495bd055db7579f77b9d46d648dfb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130902542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bde91ddd0d12a726bdc83b011f5a3c64e7a9d481b990c19a06940210c0f5f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:50:47 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 02:50:56 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 02:51:08 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:53:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:53:59 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:54:04 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 02:54:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:54:18 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:54:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ff377b76ae8706d5cdeb8c5bb0ac65cd688d5ddeddc54bb9275675896d29c8`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b083c03dbcd716610d1bc087492c90470d5fd01491bd52e78ece7cb166086a39`  
		Last Modified: Fri, 18 Jun 2021 03:05:31 GMT  
		Size: 84.7 MB (84650431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9660ffafc12e71553e85df09e7ac56082ac05c98de2397474a5b62c3d15ba87`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d85e77e75fe69436dd384ba119d006dd97042726fc12258c2df25f9be41ae`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.29-focal`

```console
$ docker pull mariadb@sha256:a8a03802fcd59d5482ae1996137e6f073be80746e82fc7cf22e934e8d2102e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.29-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b1b6642782ded113856daf31cb48e96b64af861d54182acbd61b6a0e38c70f43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120022754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87f2efbb6ad4decaaa3752613badced2ab82855803e43eda5d25eb6b78f20e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:58:37 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 04:58:37 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 04:58:38 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:59:19 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:59:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:59:19 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:59:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 04:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:59:21 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:59:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34136f02944f1519398da6be3fab15bfb91553e7d4f056d9af5fa9dc23e25776`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b52de8f0a748ab083714bc5b97abb8c490bfa0e62806188309db0dce8e4695c`  
		Last Modified: Fri, 18 Jun 2021 05:03:19 GMT  
		Size: 80.1 MB (80079822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4906eba5fa0d8be69e4653cabb71c7947701324eaa908d573871deb3913d20`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c481ed9c56fa32f74c4aacd0dd2f22a195d7a7f093c3d86b13381995e28f021`  
		Last Modified: Fri, 18 Jun 2021 05:03:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.29-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:05ff2732c1990967a3395d6930deb04235372e724c7da356267c3118603ed9b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117617654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276bab2fb248e858dae13121ec7aa60d159c923acd2a52744ba4f039b589e808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 00:48:23 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:47 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760c30d6dbfa45dc14eb4a99ce6717ff04fce410c9df6b19e2316c24e3c0277`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf847301ed0bae6f944b6b36e057cb9bd51224a86f5a2b76935bbb73e5078cbe`  
		Last Modified: Fri, 18 Jun 2021 00:53:35 GMT  
		Size: 79.4 MB (79380839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015aaec3f93fb58e45b19e5781020acfa46c5f58f9225473dfdbdde9ebf9ff61`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163dd26927d877159c8477b3ea75082a5271c65a1c50861d1463690100d7541e`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.29-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d5380d75882e95be32377b879b5795887b495bd055db7579f77b9d46d648dfb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130902542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bde91ddd0d12a726bdc83b011f5a3c64e7a9d481b990c19a06940210c0f5f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:50:47 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 02:50:56 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 02:51:08 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:53:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:53:59 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:54:04 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 02:54:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:54:18 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:54:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ff377b76ae8706d5cdeb8c5bb0ac65cd688d5ddeddc54bb9275675896d29c8`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b083c03dbcd716610d1bc087492c90470d5fd01491bd52e78ece7cb166086a39`  
		Last Modified: Fri, 18 Jun 2021 03:05:31 GMT  
		Size: 84.7 MB (84650431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9660ffafc12e71553e85df09e7ac56082ac05c98de2397474a5b62c3d15ba87`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d85e77e75fe69436dd384ba119d006dd97042726fc12258c2df25f9be41ae`  
		Last Modified: Fri, 18 Jun 2021 03:05:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:28c29e7b6a1fa532f7c861afc50481484d4c3ab94500adbbf2bb04f30d43438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:adc4a70494ebc1b02610ecb1168ff473d652ca5196d8d4fa1cf157e872f4f63d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124705038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a944f83f9aa0cb97c8ad4f9918d604ee92493e48d9a218f2fdccc4b555e3f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 04:57:55 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 04:57:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:58:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:58:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:58:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:58:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 04:58:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:58:32 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:58:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ef9abc9b41fa7caea275854656ca5b5c0b1bb1d25a4c86048df0ee9602b1b4`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c50005ed8962db0bea6fe576986feb6c5aafb24b49f1636fc5aabc7eb3fc177`  
		Last Modified: Fri, 18 Jun 2021 05:02:50 GMT  
		Size: 84.8 MB (84762105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5d1015d51e4976c975638e4837e5e96355ff2f5dc5fa7211344c890c7dac2d`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71ccf4086082fd9460bf5a85c46ca8eeab0a8a90ec1b54d234ed7bd071b0da`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e19adfc2335a54d0ffe2fb525d2777923fc2d71620f6d3130db9ea821d2b7c82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122225628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0305fc9557048568c4565579e95dd3507804bf10c123db402334da91c82209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 00:47:56 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 00:47:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:15 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:16 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c30f3e876b59214b89a16eaf140ef175bfd090b6420a808ff095a385d7d792`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b6168d649c8cd42a6cd59b90b0da9f35a12e25c6834b36f10b2e06292c428`  
		Last Modified: Fri, 18 Jun 2021 00:52:57 GMT  
		Size: 84.0 MB (83988817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9324009e782ea65db1057a9534d407c4d034db9363bfbc499a06f692b1a5f7`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff93debfa336b5bbd05bb6f7b7258d1641d98cec22f79d3c4fb4bf0e0aa59a6b`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:035fdb0985179258cf6ae3247adc34a12bc89b0a66aa6ee484739e087c21ed77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135481343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8bd03e2d29053b80e7dcedc73c45e00955985f67b88bf22a83f357ebb36945`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:45:54 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 02:45:57 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 02:46:11 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:49:29 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:49:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:49:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:49:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 02:50:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:50:29 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:50:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c09b410705b361a1012b80dc8cb4d9eea7ced4c34fb58046d2392d7bd09359`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e4987aed889e4d1fddeaae728c2eb6fa7b97385f24b1df1c693a6e4f61bfa`  
		Last Modified: Fri, 18 Jun 2021 03:04:52 GMT  
		Size: 89.2 MB (89229232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c4800093cbe177437c888c875bd23e38189d25fa2e39a0dc08b450170d5dac`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263f3a75f4b837a5a4d163a33b550a944b7167672b80488124aa03a6fb58ef9c`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:28c29e7b6a1fa532f7c861afc50481484d4c3ab94500adbbf2bb04f30d43438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:adc4a70494ebc1b02610ecb1168ff473d652ca5196d8d4fa1cf157e872f4f63d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124705038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a944f83f9aa0cb97c8ad4f9918d604ee92493e48d9a218f2fdccc4b555e3f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 04:57:55 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 04:57:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:58:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:58:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:58:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:58:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 04:58:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:58:32 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:58:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ef9abc9b41fa7caea275854656ca5b5c0b1bb1d25a4c86048df0ee9602b1b4`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c50005ed8962db0bea6fe576986feb6c5aafb24b49f1636fc5aabc7eb3fc177`  
		Last Modified: Fri, 18 Jun 2021 05:02:50 GMT  
		Size: 84.8 MB (84762105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5d1015d51e4976c975638e4837e5e96355ff2f5dc5fa7211344c890c7dac2d`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71ccf4086082fd9460bf5a85c46ca8eeab0a8a90ec1b54d234ed7bd071b0da`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e19adfc2335a54d0ffe2fb525d2777923fc2d71620f6d3130db9ea821d2b7c82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122225628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0305fc9557048568c4565579e95dd3507804bf10c123db402334da91c82209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 00:47:56 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 00:47:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:15 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:16 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c30f3e876b59214b89a16eaf140ef175bfd090b6420a808ff095a385d7d792`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b6168d649c8cd42a6cd59b90b0da9f35a12e25c6834b36f10b2e06292c428`  
		Last Modified: Fri, 18 Jun 2021 00:52:57 GMT  
		Size: 84.0 MB (83988817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9324009e782ea65db1057a9534d407c4d034db9363bfbc499a06f692b1a5f7`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff93debfa336b5bbd05bb6f7b7258d1641d98cec22f79d3c4fb4bf0e0aa59a6b`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:035fdb0985179258cf6ae3247adc34a12bc89b0a66aa6ee484739e087c21ed77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135481343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8bd03e2d29053b80e7dcedc73c45e00955985f67b88bf22a83f357ebb36945`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:45:54 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 02:45:57 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 02:46:11 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:49:29 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:49:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:49:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:49:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 02:50:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:50:29 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:50:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c09b410705b361a1012b80dc8cb4d9eea7ced4c34fb58046d2392d7bd09359`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e4987aed889e4d1fddeaae728c2eb6fa7b97385f24b1df1c693a6e4f61bfa`  
		Last Modified: Fri, 18 Jun 2021 03:04:52 GMT  
		Size: 89.2 MB (89229232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c4800093cbe177437c888c875bd23e38189d25fa2e39a0dc08b450170d5dac`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263f3a75f4b837a5a4d163a33b550a944b7167672b80488124aa03a6fb58ef9c`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.19`

```console
$ docker pull mariadb@sha256:28c29e7b6a1fa532f7c861afc50481484d4c3ab94500adbbf2bb04f30d43438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.19` - linux; amd64

```console
$ docker pull mariadb@sha256:adc4a70494ebc1b02610ecb1168ff473d652ca5196d8d4fa1cf157e872f4f63d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124705038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a944f83f9aa0cb97c8ad4f9918d604ee92493e48d9a218f2fdccc4b555e3f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 04:57:55 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 04:57:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:58:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:58:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:58:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:58:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 04:58:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:58:32 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:58:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ef9abc9b41fa7caea275854656ca5b5c0b1bb1d25a4c86048df0ee9602b1b4`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c50005ed8962db0bea6fe576986feb6c5aafb24b49f1636fc5aabc7eb3fc177`  
		Last Modified: Fri, 18 Jun 2021 05:02:50 GMT  
		Size: 84.8 MB (84762105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5d1015d51e4976c975638e4837e5e96355ff2f5dc5fa7211344c890c7dac2d`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71ccf4086082fd9460bf5a85c46ca8eeab0a8a90ec1b54d234ed7bd071b0da`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.19` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e19adfc2335a54d0ffe2fb525d2777923fc2d71620f6d3130db9ea821d2b7c82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122225628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0305fc9557048568c4565579e95dd3507804bf10c123db402334da91c82209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 00:47:56 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 00:47:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:15 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:16 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c30f3e876b59214b89a16eaf140ef175bfd090b6420a808ff095a385d7d792`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b6168d649c8cd42a6cd59b90b0da9f35a12e25c6834b36f10b2e06292c428`  
		Last Modified: Fri, 18 Jun 2021 00:52:57 GMT  
		Size: 84.0 MB (83988817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9324009e782ea65db1057a9534d407c4d034db9363bfbc499a06f692b1a5f7`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff93debfa336b5bbd05bb6f7b7258d1641d98cec22f79d3c4fb4bf0e0aa59a6b`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.19` - linux; ppc64le

```console
$ docker pull mariadb@sha256:035fdb0985179258cf6ae3247adc34a12bc89b0a66aa6ee484739e087c21ed77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135481343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8bd03e2d29053b80e7dcedc73c45e00955985f67b88bf22a83f357ebb36945`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:45:54 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 02:45:57 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 02:46:11 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:49:29 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:49:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:49:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:49:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 02:50:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:50:29 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:50:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c09b410705b361a1012b80dc8cb4d9eea7ced4c34fb58046d2392d7bd09359`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e4987aed889e4d1fddeaae728c2eb6fa7b97385f24b1df1c693a6e4f61bfa`  
		Last Modified: Fri, 18 Jun 2021 03:04:52 GMT  
		Size: 89.2 MB (89229232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c4800093cbe177437c888c875bd23e38189d25fa2e39a0dc08b450170d5dac`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263f3a75f4b837a5a4d163a33b550a944b7167672b80488124aa03a6fb58ef9c`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.19-focal`

```console
$ docker pull mariadb@sha256:28c29e7b6a1fa532f7c861afc50481484d4c3ab94500adbbf2bb04f30d43438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.19-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:adc4a70494ebc1b02610ecb1168ff473d652ca5196d8d4fa1cf157e872f4f63d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124705038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a944f83f9aa0cb97c8ad4f9918d604ee92493e48d9a218f2fdccc4b555e3f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 04:57:55 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 04:57:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:58:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:58:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:58:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:58:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 04:58:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:58:32 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:58:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ef9abc9b41fa7caea275854656ca5b5c0b1bb1d25a4c86048df0ee9602b1b4`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c50005ed8962db0bea6fe576986feb6c5aafb24b49f1636fc5aabc7eb3fc177`  
		Last Modified: Fri, 18 Jun 2021 05:02:50 GMT  
		Size: 84.8 MB (84762105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5d1015d51e4976c975638e4837e5e96355ff2f5dc5fa7211344c890c7dac2d`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71ccf4086082fd9460bf5a85c46ca8eeab0a8a90ec1b54d234ed7bd071b0da`  
		Last Modified: Fri, 18 Jun 2021 05:02:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.19-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e19adfc2335a54d0ffe2fb525d2777923fc2d71620f6d3130db9ea821d2b7c82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122225628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0305fc9557048568c4565579e95dd3507804bf10c123db402334da91c82209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 00:47:56 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 00:47:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:15 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:16 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c30f3e876b59214b89a16eaf140ef175bfd090b6420a808ff095a385d7d792`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b6168d649c8cd42a6cd59b90b0da9f35a12e25c6834b36f10b2e06292c428`  
		Last Modified: Fri, 18 Jun 2021 00:52:57 GMT  
		Size: 84.0 MB (83988817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9324009e782ea65db1057a9534d407c4d034db9363bfbc499a06f692b1a5f7`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff93debfa336b5bbd05bb6f7b7258d1641d98cec22f79d3c4fb4bf0e0aa59a6b`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.19-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:035fdb0985179258cf6ae3247adc34a12bc89b0a66aa6ee484739e087c21ed77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135481343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8bd03e2d29053b80e7dcedc73c45e00955985f67b88bf22a83f357ebb36945`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:45:54 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 02:45:57 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 02:46:11 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:49:29 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:49:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:49:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:49:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 02:50:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:50:29 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:50:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c09b410705b361a1012b80dc8cb4d9eea7ced4c34fb58046d2392d7bd09359`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e4987aed889e4d1fddeaae728c2eb6fa7b97385f24b1df1c693a6e4f61bfa`  
		Last Modified: Fri, 18 Jun 2021 03:04:52 GMT  
		Size: 89.2 MB (89229232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c4800093cbe177437c888c875bd23e38189d25fa2e39a0dc08b450170d5dac`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263f3a75f4b837a5a4d163a33b550a944b7167672b80488124aa03a6fb58ef9c`  
		Last Modified: Fri, 18 Jun 2021 03:04:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:be1b339b181ba9f4f95d3aebed9c88ada73273f9474f8413e3fcd1d11e64cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:ca4b2789ac74d0e7c1f9fe32c66a100115ab77d50298158e81fb7e55451a016e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126882173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d89055e5ca272ed7d5da8019d5f92dab1ca588704ffb069829ff723b1fcd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 04:57:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:50 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:50 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb173802fc8683da7adc0f470fbc24dbd74bd845bc7cab75baa6895934e8ae`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2f79f6e6e7563887ee568524407a5c92cee94c22ec47bf46378218ab0be25d`  
		Last Modified: Fri, 18 Jun 2021 05:02:09 GMT  
		Size: 86.9 MB (86939363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2faf917bfb21b3be0ab8246736bca42c357831b873cf405c4f10e153e35c90`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a245b8604e5653edd82713f107d13fc9aef08210c51f5575682997dbedcb384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137576307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62822aca60556dacde47fa40c413245c5cfe3cd9fa3e586a6c6fa65d401d0389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:41:08 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 02:41:14 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 02:41:21 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:44:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:45:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:45:12 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:45:24 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:45:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e4a51f683a867a9b9940cab2319fe7761520236e4d3bb7d8bff8c3e6b2b31b`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17466f0a629dce0359714b749814b8513747e81dbcb854c3cb7d730f638b294b`  
		Last Modified: Fri, 18 Jun 2021 03:04:08 GMT  
		Size: 91.3 MB (91324318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f253cd53c36c6ac73a52fc3a015c8307a251d301d69070270ddd98197941e`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:be1b339b181ba9f4f95d3aebed9c88ada73273f9474f8413e3fcd1d11e64cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:ca4b2789ac74d0e7c1f9fe32c66a100115ab77d50298158e81fb7e55451a016e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126882173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d89055e5ca272ed7d5da8019d5f92dab1ca588704ffb069829ff723b1fcd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 04:57:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:50 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:50 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb173802fc8683da7adc0f470fbc24dbd74bd845bc7cab75baa6895934e8ae`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2f79f6e6e7563887ee568524407a5c92cee94c22ec47bf46378218ab0be25d`  
		Last Modified: Fri, 18 Jun 2021 05:02:09 GMT  
		Size: 86.9 MB (86939363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2faf917bfb21b3be0ab8246736bca42c357831b873cf405c4f10e153e35c90`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a245b8604e5653edd82713f107d13fc9aef08210c51f5575682997dbedcb384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137576307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62822aca60556dacde47fa40c413245c5cfe3cd9fa3e586a6c6fa65d401d0389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:41:08 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 02:41:14 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 02:41:21 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:44:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:45:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:45:12 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:45:24 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:45:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e4a51f683a867a9b9940cab2319fe7761520236e4d3bb7d8bff8c3e6b2b31b`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17466f0a629dce0359714b749814b8513747e81dbcb854c3cb7d730f638b294b`  
		Last Modified: Fri, 18 Jun 2021 03:04:08 GMT  
		Size: 91.3 MB (91324318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f253cd53c36c6ac73a52fc3a015c8307a251d301d69070270ddd98197941e`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.10`

```console
$ docker pull mariadb@sha256:be1b339b181ba9f4f95d3aebed9c88ada73273f9474f8413e3fcd1d11e64cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.10` - linux; amd64

```console
$ docker pull mariadb@sha256:ca4b2789ac74d0e7c1f9fe32c66a100115ab77d50298158e81fb7e55451a016e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126882173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d89055e5ca272ed7d5da8019d5f92dab1ca588704ffb069829ff723b1fcd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 04:57:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:50 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:50 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb173802fc8683da7adc0f470fbc24dbd74bd845bc7cab75baa6895934e8ae`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2f79f6e6e7563887ee568524407a5c92cee94c22ec47bf46378218ab0be25d`  
		Last Modified: Fri, 18 Jun 2021 05:02:09 GMT  
		Size: 86.9 MB (86939363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2faf917bfb21b3be0ab8246736bca42c357831b873cf405c4f10e153e35c90`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a245b8604e5653edd82713f107d13fc9aef08210c51f5575682997dbedcb384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137576307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62822aca60556dacde47fa40c413245c5cfe3cd9fa3e586a6c6fa65d401d0389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:41:08 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 02:41:14 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 02:41:21 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:44:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:45:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:45:12 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:45:24 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:45:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e4a51f683a867a9b9940cab2319fe7761520236e4d3bb7d8bff8c3e6b2b31b`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17466f0a629dce0359714b749814b8513747e81dbcb854c3cb7d730f638b294b`  
		Last Modified: Fri, 18 Jun 2021 03:04:08 GMT  
		Size: 91.3 MB (91324318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f253cd53c36c6ac73a52fc3a015c8307a251d301d69070270ddd98197941e`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.10-focal`

```console
$ docker pull mariadb@sha256:be1b339b181ba9f4f95d3aebed9c88ada73273f9474f8413e3fcd1d11e64cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:ca4b2789ac74d0e7c1f9fe32c66a100115ab77d50298158e81fb7e55451a016e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126882173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d89055e5ca272ed7d5da8019d5f92dab1ca588704ffb069829ff723b1fcd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 04:57:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:50 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:50 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb173802fc8683da7adc0f470fbc24dbd74bd845bc7cab75baa6895934e8ae`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2f79f6e6e7563887ee568524407a5c92cee94c22ec47bf46378218ab0be25d`  
		Last Modified: Fri, 18 Jun 2021 05:02:09 GMT  
		Size: 86.9 MB (86939363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2faf917bfb21b3be0ab8246736bca42c357831b873cf405c4f10e153e35c90`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a245b8604e5653edd82713f107d13fc9aef08210c51f5575682997dbedcb384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137576307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62822aca60556dacde47fa40c413245c5cfe3cd9fa3e586a6c6fa65d401d0389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:41:08 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 02:41:14 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 02:41:21 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:44:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:45:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:45:12 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:45:24 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:45:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e4a51f683a867a9b9940cab2319fe7761520236e4d3bb7d8bff8c3e6b2b31b`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17466f0a629dce0359714b749814b8513747e81dbcb854c3cb7d730f638b294b`  
		Last Modified: Fri, 18 Jun 2021 03:04:08 GMT  
		Size: 91.3 MB (91324318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f253cd53c36c6ac73a52fc3a015c8307a251d301d69070270ddd98197941e`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:b2ba2c4dcaf9a946241f7e368637d351a74010b58f7c5e50002b9735c95c6326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:766b517299edbc055c085103bde25153b5ec031f5836073a0056c2ee679949a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127053806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a2df183cfa924af58e6dd41dd26bc877f9c4777a8fa3eaa5437d0d8b2990f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 04:56:46 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:24 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:25 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b7f963087cef9b50ec84dcf3f0cc460b6ce8d3807b27fd3c8d28a94ae08b0`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a588b78c8ec60b195a74de96104e78c31a20a9aa3ec73ae5d27a4248cb9a9`  
		Last Modified: Fri, 18 Jun 2021 05:01:34 GMT  
		Size: 87.1 MB (87110993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcbe748934e3005e7fbd83de01a1baded6c9e68d55f1f9b54bbc7818008f439`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:863af06507823eb8daf2de20fa54eb9a290be7dbc115c5a42f9c5fc33d39c3cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137563117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92136103a3c859b4b2b14bfb047c3cfb75171b06a7a97e158fd4af9cce951aa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:36:43 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 02:36:47 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 02:36:57 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:40:28 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:40:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:40:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:40:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:40:52 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99ade562883aeff5f1d5c11bd331c708c465d4cef67019719fcc5b990dc37b2`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41958c60ca03214cb1d2ba6315a7d8b4bc2d7ae33927ad905bf058be67e1b9d`  
		Last Modified: Fri, 18 Jun 2021 03:03:28 GMT  
		Size: 91.3 MB (91311128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc4d1e5947e520c9ad100ef65088bd3d3e5f2c29467f156585190f68170c3a`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:b2ba2c4dcaf9a946241f7e368637d351a74010b58f7c5e50002b9735c95c6326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:766b517299edbc055c085103bde25153b5ec031f5836073a0056c2ee679949a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127053806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a2df183cfa924af58e6dd41dd26bc877f9c4777a8fa3eaa5437d0d8b2990f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 04:56:46 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:24 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:25 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b7f963087cef9b50ec84dcf3f0cc460b6ce8d3807b27fd3c8d28a94ae08b0`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a588b78c8ec60b195a74de96104e78c31a20a9aa3ec73ae5d27a4248cb9a9`  
		Last Modified: Fri, 18 Jun 2021 05:01:34 GMT  
		Size: 87.1 MB (87110993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcbe748934e3005e7fbd83de01a1baded6c9e68d55f1f9b54bbc7818008f439`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:863af06507823eb8daf2de20fa54eb9a290be7dbc115c5a42f9c5fc33d39c3cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137563117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92136103a3c859b4b2b14bfb047c3cfb75171b06a7a97e158fd4af9cce951aa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:36:43 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 02:36:47 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 02:36:57 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:40:28 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:40:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:40:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:40:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:40:52 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99ade562883aeff5f1d5c11bd331c708c465d4cef67019719fcc5b990dc37b2`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41958c60ca03214cb1d2ba6315a7d8b4bc2d7ae33927ad905bf058be67e1b9d`  
		Last Modified: Fri, 18 Jun 2021 03:03:28 GMT  
		Size: 91.3 MB (91311128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc4d1e5947e520c9ad100ef65088bd3d3e5f2c29467f156585190f68170c3a`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.1`

```console
$ docker pull mariadb@sha256:b2ba2c4dcaf9a946241f7e368637d351a74010b58f7c5e50002b9735c95c6326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.1` - linux; amd64

```console
$ docker pull mariadb@sha256:766b517299edbc055c085103bde25153b5ec031f5836073a0056c2ee679949a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127053806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a2df183cfa924af58e6dd41dd26bc877f9c4777a8fa3eaa5437d0d8b2990f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 04:56:46 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:24 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:25 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b7f963087cef9b50ec84dcf3f0cc460b6ce8d3807b27fd3c8d28a94ae08b0`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a588b78c8ec60b195a74de96104e78c31a20a9aa3ec73ae5d27a4248cb9a9`  
		Last Modified: Fri, 18 Jun 2021 05:01:34 GMT  
		Size: 87.1 MB (87110993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcbe748934e3005e7fbd83de01a1baded6c9e68d55f1f9b54bbc7818008f439`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:863af06507823eb8daf2de20fa54eb9a290be7dbc115c5a42f9c5fc33d39c3cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137563117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92136103a3c859b4b2b14bfb047c3cfb75171b06a7a97e158fd4af9cce951aa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:36:43 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 02:36:47 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 02:36:57 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:40:28 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:40:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:40:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:40:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:40:52 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99ade562883aeff5f1d5c11bd331c708c465d4cef67019719fcc5b990dc37b2`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41958c60ca03214cb1d2ba6315a7d8b4bc2d7ae33927ad905bf058be67e1b9d`  
		Last Modified: Fri, 18 Jun 2021 03:03:28 GMT  
		Size: 91.3 MB (91311128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc4d1e5947e520c9ad100ef65088bd3d3e5f2c29467f156585190f68170c3a`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.1-focal`

```console
$ docker pull mariadb@sha256:b2ba2c4dcaf9a946241f7e368637d351a74010b58f7c5e50002b9735c95c6326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.1-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:766b517299edbc055c085103bde25153b5ec031f5836073a0056c2ee679949a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127053806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a2df183cfa924af58e6dd41dd26bc877f9c4777a8fa3eaa5437d0d8b2990f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 04:56:46 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:24 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:25 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b7f963087cef9b50ec84dcf3f0cc460b6ce8d3807b27fd3c8d28a94ae08b0`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a588b78c8ec60b195a74de96104e78c31a20a9aa3ec73ae5d27a4248cb9a9`  
		Last Modified: Fri, 18 Jun 2021 05:01:34 GMT  
		Size: 87.1 MB (87110993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcbe748934e3005e7fbd83de01a1baded6c9e68d55f1f9b54bbc7818008f439`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.1-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.1-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:863af06507823eb8daf2de20fa54eb9a290be7dbc115c5a42f9c5fc33d39c3cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137563117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92136103a3c859b4b2b14bfb047c3cfb75171b06a7a97e158fd4af9cce951aa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:36:43 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 02:36:47 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 02:36:57 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:40:28 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:40:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:40:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:40:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:40:52 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99ade562883aeff5f1d5c11bd331c708c465d4cef67019719fcc5b990dc37b2`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41958c60ca03214cb1d2ba6315a7d8b4bc2d7ae33927ad905bf058be67e1b9d`  
		Last Modified: Fri, 18 Jun 2021 03:03:28 GMT  
		Size: 91.3 MB (91311128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc4d1e5947e520c9ad100ef65088bd3d3e5f2c29467f156585190f68170c3a`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:beta`

```console
$ docker pull mariadb@sha256:b2ba2c4dcaf9a946241f7e368637d351a74010b58f7c5e50002b9735c95c6326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:beta` - linux; amd64

```console
$ docker pull mariadb@sha256:766b517299edbc055c085103bde25153b5ec031f5836073a0056c2ee679949a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127053806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a2df183cfa924af58e6dd41dd26bc877f9c4777a8fa3eaa5437d0d8b2990f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 04:56:46 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:24 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:25 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b7f963087cef9b50ec84dcf3f0cc460b6ce8d3807b27fd3c8d28a94ae08b0`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a588b78c8ec60b195a74de96104e78c31a20a9aa3ec73ae5d27a4248cb9a9`  
		Last Modified: Fri, 18 Jun 2021 05:01:34 GMT  
		Size: 87.1 MB (87110993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcbe748934e3005e7fbd83de01a1baded6c9e68d55f1f9b54bbc7818008f439`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta` - linux; ppc64le

```console
$ docker pull mariadb@sha256:863af06507823eb8daf2de20fa54eb9a290be7dbc115c5a42f9c5fc33d39c3cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137563117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92136103a3c859b4b2b14bfb047c3cfb75171b06a7a97e158fd4af9cce951aa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:36:43 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 02:36:47 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 02:36:57 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:40:28 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:40:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:40:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:40:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:40:52 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99ade562883aeff5f1d5c11bd331c708c465d4cef67019719fcc5b990dc37b2`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41958c60ca03214cb1d2ba6315a7d8b4bc2d7ae33927ad905bf058be67e1b9d`  
		Last Modified: Fri, 18 Jun 2021 03:03:28 GMT  
		Size: 91.3 MB (91311128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc4d1e5947e520c9ad100ef65088bd3d3e5f2c29467f156585190f68170c3a`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:beta-focal`

```console
$ docker pull mariadb@sha256:b2ba2c4dcaf9a946241f7e368637d351a74010b58f7c5e50002b9735c95c6326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:beta-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:766b517299edbc055c085103bde25153b5ec031f5836073a0056c2ee679949a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127053806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a2df183cfa924af58e6dd41dd26bc877f9c4777a8fa3eaa5437d0d8b2990f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 04:56:45 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 04:56:46 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:23 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:24 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:25 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b7f963087cef9b50ec84dcf3f0cc460b6ce8d3807b27fd3c8d28a94ae08b0`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a588b78c8ec60b195a74de96104e78c31a20a9aa3ec73ae5d27a4248cb9a9`  
		Last Modified: Fri, 18 Jun 2021 05:01:34 GMT  
		Size: 87.1 MB (87110993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcbe748934e3005e7fbd83de01a1baded6c9e68d55f1f9b54bbc7818008f439`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:863af06507823eb8daf2de20fa54eb9a290be7dbc115c5a42f9c5fc33d39c3cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137563117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92136103a3c859b4b2b14bfb047c3cfb75171b06a7a97e158fd4af9cce951aa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:36:43 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 02:36:47 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 02:36:57 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:40:28 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:40:43 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:40:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:40:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:40:52 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99ade562883aeff5f1d5c11bd331c708c465d4cef67019719fcc5b990dc37b2`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41958c60ca03214cb1d2ba6315a7d8b4bc2d7ae33927ad905bf058be67e1b9d`  
		Last Modified: Fri, 18 Jun 2021 03:03:28 GMT  
		Size: 91.3 MB (91311128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc4d1e5947e520c9ad100ef65088bd3d3e5f2c29467f156585190f68170c3a`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:be1b339b181ba9f4f95d3aebed9c88ada73273f9474f8413e3fcd1d11e64cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:ca4b2789ac74d0e7c1f9fe32c66a100115ab77d50298158e81fb7e55451a016e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126882173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d89055e5ca272ed7d5da8019d5f92dab1ca588704ffb069829ff723b1fcd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 04:57:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:50 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:50 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb173802fc8683da7adc0f470fbc24dbd74bd845bc7cab75baa6895934e8ae`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2f79f6e6e7563887ee568524407a5c92cee94c22ec47bf46378218ab0be25d`  
		Last Modified: Fri, 18 Jun 2021 05:02:09 GMT  
		Size: 86.9 MB (86939363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2faf917bfb21b3be0ab8246736bca42c357831b873cf405c4f10e153e35c90`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a245b8604e5653edd82713f107d13fc9aef08210c51f5575682997dbedcb384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137576307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62822aca60556dacde47fa40c413245c5cfe3cd9fa3e586a6c6fa65d401d0389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:41:08 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 02:41:14 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 02:41:21 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:44:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:45:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:45:12 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:45:24 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:45:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e4a51f683a867a9b9940cab2319fe7761520236e4d3bb7d8bff8c3e6b2b31b`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17466f0a629dce0359714b749814b8513747e81dbcb854c3cb7d730f638b294b`  
		Last Modified: Fri, 18 Jun 2021 03:04:08 GMT  
		Size: 91.3 MB (91324318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f253cd53c36c6ac73a52fc3a015c8307a251d301d69070270ddd98197941e`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:be1b339b181ba9f4f95d3aebed9c88ada73273f9474f8413e3fcd1d11e64cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:ca4b2789ac74d0e7c1f9fe32c66a100115ab77d50298158e81fb7e55451a016e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126882173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d89055e5ca272ed7d5da8019d5f92dab1ca588704ffb069829ff723b1fcd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:56:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 04:56:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 04:56:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 04:56:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 04:56:43 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:56:44 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 04:56:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 04:57:29 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 04:57:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 04:57:49 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 04:57:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 04:57:50 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 04:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 04:57:50 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 04:57:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea6552a46225f37637d406d551ee8fc04ad670606749bf77583984e305763f`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329b1f41043f334fc046ee77daca5b1f2da2680818c346eac07cd10135c85bec`  
		Last Modified: Fri, 18 Jun 2021 05:01:24 GMT  
		Size: 5.5 MB (5488775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d09317d80bcdbde01a7d4984a0d06edfc3b8284f2bb9a81401f0dd7b4f3be`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 3.6 MB (3615926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc055a5511da95c2f42bf255ff0275c86b2e09ad80b7360a2bb717683fe5ce6`  
		Last Modified: Fri, 18 Jun 2021 05:01:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea9e85bedf0cfddaad4d893fa286f85befbc4917147a327b9f8385fa540dd2`  
		Last Modified: Fri, 18 Jun 2021 05:01:21 GMT  
		Size: 2.3 MB (2274155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca0fb8256c072186f30885b966a2279241d86c4b9b252b5cd8e804537d4940`  
		Last Modified: Fri, 18 Jun 2021 05:01:20 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb173802fc8683da7adc0f470fbc24dbd74bd845bc7cab75baa6895934e8ae`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2f79f6e6e7563887ee568524407a5c92cee94c22ec47bf46378218ab0be25d`  
		Last Modified: Fri, 18 Jun 2021 05:02:09 GMT  
		Size: 86.9 MB (86939363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2faf917bfb21b3be0ab8246736bca42c357831b873cf405c4f10e153e35c90`  
		Last Modified: Fri, 18 Jun 2021 05:01:56 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8a245b8604e5653edd82713f107d13fc9aef08210c51f5575682997dbedcb384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137576307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62822aca60556dacde47fa40c413245c5cfe3cd9fa3e586a6c6fa65d401d0389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:33:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 02:35:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:35:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 02:35:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 02:35:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 02:36:25 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:36:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 02:36:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 02:41:08 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 02:41:14 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 02:41:21 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 02:44:55 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 02:45:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 02:45:12 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 02:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 02:45:24 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 02:45:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892130860a067fec368c20f64f2f559deb8e9247d04a6b64ce46b0a114063e50`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c39b896efee4493ae5781757a9d5284e14a7a25ca343ff220681cde01cbf42a`  
		Last Modified: Fri, 18 Jun 2021 03:03:15 GMT  
		Size: 6.7 MB (6667940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd80d1608d833d5aea73f684fecec978d139c0929ec3d1c69c92a4ee5db0b1f`  
		Last Modified: Fri, 18 Jun 2021 03:03:14 GMT  
		Size: 3.7 MB (3725668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8437f7227b0b42d011a9e3e8cd2e8a8bbdd7593d4c491adca03444c024021`  
		Last Modified: Fri, 18 Jun 2021 03:03:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcbdb7b7a24b6f05ca048cb658c315275fa2aa36ab7143635f4d4285cef020e`  
		Last Modified: Fri, 18 Jun 2021 03:03:10 GMT  
		Size: 2.6 MB (2569861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a302fb3c488f1e06de8685360e165c3fdba690a73d3361ed66211c4f1db9764`  
		Last Modified: Fri, 18 Jun 2021 03:03:09 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e4a51f683a867a9b9940cab2319fe7761520236e4d3bb7d8bff8c3e6b2b31b`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17466f0a629dce0359714b749814b8513747e81dbcb854c3cb7d730f638b294b`  
		Last Modified: Fri, 18 Jun 2021 03:04:08 GMT  
		Size: 91.3 MB (91324318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f253cd53c36c6ac73a52fc3a015c8307a251d301d69070270ddd98197941e`  
		Last Modified: Fri, 18 Jun 2021 03:03:49 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
