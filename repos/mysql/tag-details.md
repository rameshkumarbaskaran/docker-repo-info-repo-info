<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.50`](#mysql5650)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.32`](#mysql5732)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.22`](#mysql8022)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:c3a567d3e3ad8b05dfce401ed08f0f6bf3f3b64cc17694979d5f2e5d78e10173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:360d1924d86cbf416f2c84687c2037e153080fed932798a73c5c6b4ceb7399e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154499935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07dfa83b5283f486f1fa1628cb8b4a18a4d071a486708acc5c06243ca7f592a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:04:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Dec 2020 17:04:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:04:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 11 Dec 2020 17:04:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Dec 2020 17:04:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Dec 2020 17:04:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:01 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 11 Dec 2020 17:05:31 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 11 Dec 2020 17:05:31 GMT
ENV MYSQL_VERSION=5.7.32-1debian10
# Fri, 11 Dec 2020 17:05:32 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 11 Dec 2020 17:05:55 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 11 Dec 2020 17:05:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 21 Dec 2020 20:34:42 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Mon, 21 Dec 2020 20:34:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 21 Dec 2020 20:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Dec 2020 20:34:43 GMT
EXPOSE 3306 33060
# Mon, 21 Dec 2020 20:34:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd960d34819b836a86d505ec5d22361c43a4a6df2c8763f2b96ba9f39e8a9d`  
		Last Modified: Fri, 11 Dec 2020 17:07:18 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab947313861c1a794864761bac953e6280da23bca3515156f7159aaa2b62ce1`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 4.2 MB (4178330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f92f19e63856fe7746b7f86dbc0aa50aecd52a43c26421e005493bdd14a12a`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 1.4 MB (1419183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e80b17bff96a7c7a8ceff95e27c30ca6c0c3211ec8c6c3532b0f83bdd8b407f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e976799f91c10d5acc4d9e71a3ddbdc9e2ba0efe1f9251ece7823a09bdf8c`  
		Last Modified: Fri, 11 Dec 2020 17:07:20 GMT  
		Size: 13.4 MB (13447254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ae84fee1b32077b44663fa381bf450c81d17722b0b7c7531744eb3a810385f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1da2a18e2e2b5f6ca1f752e656f5c88186d6f41e7745f7752f2aed32cdf899`  
		Last Modified: Fri, 11 Dec 2020 17:07:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301a28b700b92c71e7cbbaecb97bfac30cb7537bdc187c90b7934787522e0364`  
		Last Modified: Fri, 11 Dec 2020 17:08:01 GMT  
		Size: 108.3 MB (108346148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529dc8dbeaf3452bf9024df02320ad730c5e75a03a74ffb9960fab664dc62522`  
		Last Modified: Mon, 21 Dec 2020 20:35:14 GMT  
		Size: 5.1 KB (5138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9d021dc13f517a205ba5ccf944162d652b64d7ac09c23c81e6a4ef86096360`  
		Last Modified: Mon, 21 Dec 2020 20:35:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:51d59639d9a864ec302008c81d6909c532eff8b946993ef6448c086ba7917e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:574b626bb89112cc406c23471ab968de7be5e598eecb5ecc3eecaaf0610d8050
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102938346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebb5600241dfc6e6ca91931d0d0b3583b0a2619692c5fab8663bd7b4a16dd54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:06:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Dec 2020 17:06:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:06:12 GMT
ENV GOSU_VERSION=1.12
# Fri, 11 Dec 2020 17:06:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Dec 2020 17:06:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Dec 2020 17:06:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:06:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 11 Dec 2020 17:06:35 GMT
ENV MYSQL_MAJOR=5.6
# Fri, 11 Dec 2020 17:06:35 GMT
ENV MYSQL_VERSION=5.6.50-1debian9
# Fri, 11 Dec 2020 17:06:36 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Fri, 11 Dec 2020 17:06:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 11 Dec 2020 17:06:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 21 Dec 2020 20:34:48 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Mon, 21 Dec 2020 20:34:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 21 Dec 2020 20:34:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Dec 2020 20:34:49 GMT
EXPOSE 3306
# Mon, 21 Dec 2020 20:34:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94069ccb85355452b348b7947588bbad5f88291dad228efb4a7030f8629a72a2`  
		Last Modified: Fri, 11 Dec 2020 17:08:11 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1ed35f7ae103655ee9c62465d4bfdb82e859c7cd5f161564d4f6929f9139da`  
		Last Modified: Fri, 11 Dec 2020 17:08:11 GMT  
		Size: 4.5 MB (4502052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d6304f5ee040b9b0dc518a66d55ee1c12ca144601f895a2379260beab45261`  
		Last Modified: Fri, 11 Dec 2020 17:08:09 GMT  
		Size: 1.4 MB (1412081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df200debe65e1cec01e136d46b7b96774427e0bbdd36ae35de1dbf64e238848`  
		Last Modified: Fri, 11 Dec 2020 17:08:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c86983a5f50ce56f703821e9e389c58ce42e7981b9407db71bf5254b156d19b`  
		Last Modified: Fri, 11 Dec 2020 17:08:14 GMT  
		Size: 10.2 MB (10225281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c8ecf8cbd3cc4b3b9b82069eadb5c888927c7daec17643017accdaa15b3da6`  
		Last Modified: Fri, 11 Dec 2020 17:08:07 GMT  
		Size: 29.0 KB (28956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa953f1f767ae0fb52f6c61a428068fbd01192e5a1ad5bac1cb8fc37936052`  
		Last Modified: Fri, 11 Dec 2020 17:08:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49eac7c4004cff97e314fe992b846398f3f777f51a5d89005239d3764d4c6d6`  
		Last Modified: Fri, 11 Dec 2020 17:08:19 GMT  
		Size: 64.2 MB (64234756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0ede2893841a736bb9431d6ea8435a2c6f1d8d95560def0e86db26da5c30d8`  
		Last Modified: Mon, 21 Dec 2020 20:35:19 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1351cc5fcdfb56bbf24f3a7402a9c67b2c3e1ae1522fbd667f9293bdee2c12`  
		Last Modified: Mon, 21 Dec 2020 20:35:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.50`

```console
$ docker pull mysql@sha256:51d59639d9a864ec302008c81d6909c532eff8b946993ef6448c086ba7917e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.50` - linux; amd64

```console
$ docker pull mysql@sha256:574b626bb89112cc406c23471ab968de7be5e598eecb5ecc3eecaaf0610d8050
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102938346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebb5600241dfc6e6ca91931d0d0b3583b0a2619692c5fab8663bd7b4a16dd54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:06:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Dec 2020 17:06:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:06:12 GMT
ENV GOSU_VERSION=1.12
# Fri, 11 Dec 2020 17:06:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Dec 2020 17:06:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Dec 2020 17:06:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:06:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 11 Dec 2020 17:06:35 GMT
ENV MYSQL_MAJOR=5.6
# Fri, 11 Dec 2020 17:06:35 GMT
ENV MYSQL_VERSION=5.6.50-1debian9
# Fri, 11 Dec 2020 17:06:36 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Fri, 11 Dec 2020 17:06:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 11 Dec 2020 17:06:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 21 Dec 2020 20:34:48 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Mon, 21 Dec 2020 20:34:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 21 Dec 2020 20:34:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Dec 2020 20:34:49 GMT
EXPOSE 3306
# Mon, 21 Dec 2020 20:34:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94069ccb85355452b348b7947588bbad5f88291dad228efb4a7030f8629a72a2`  
		Last Modified: Fri, 11 Dec 2020 17:08:11 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1ed35f7ae103655ee9c62465d4bfdb82e859c7cd5f161564d4f6929f9139da`  
		Last Modified: Fri, 11 Dec 2020 17:08:11 GMT  
		Size: 4.5 MB (4502052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d6304f5ee040b9b0dc518a66d55ee1c12ca144601f895a2379260beab45261`  
		Last Modified: Fri, 11 Dec 2020 17:08:09 GMT  
		Size: 1.4 MB (1412081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df200debe65e1cec01e136d46b7b96774427e0bbdd36ae35de1dbf64e238848`  
		Last Modified: Fri, 11 Dec 2020 17:08:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c86983a5f50ce56f703821e9e389c58ce42e7981b9407db71bf5254b156d19b`  
		Last Modified: Fri, 11 Dec 2020 17:08:14 GMT  
		Size: 10.2 MB (10225281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c8ecf8cbd3cc4b3b9b82069eadb5c888927c7daec17643017accdaa15b3da6`  
		Last Modified: Fri, 11 Dec 2020 17:08:07 GMT  
		Size: 29.0 KB (28956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa953f1f767ae0fb52f6c61a428068fbd01192e5a1ad5bac1cb8fc37936052`  
		Last Modified: Fri, 11 Dec 2020 17:08:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49eac7c4004cff97e314fe992b846398f3f777f51a5d89005239d3764d4c6d6`  
		Last Modified: Fri, 11 Dec 2020 17:08:19 GMT  
		Size: 64.2 MB (64234756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0ede2893841a736bb9431d6ea8435a2c6f1d8d95560def0e86db26da5c30d8`  
		Last Modified: Mon, 21 Dec 2020 20:35:19 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1351cc5fcdfb56bbf24f3a7402a9c67b2c3e1ae1522fbd667f9293bdee2c12`  
		Last Modified: Mon, 21 Dec 2020 20:35:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:c3a567d3e3ad8b05dfce401ed08f0f6bf3f3b64cc17694979d5f2e5d78e10173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:360d1924d86cbf416f2c84687c2037e153080fed932798a73c5c6b4ceb7399e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154499935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07dfa83b5283f486f1fa1628cb8b4a18a4d071a486708acc5c06243ca7f592a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:04:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Dec 2020 17:04:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:04:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 11 Dec 2020 17:04:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Dec 2020 17:04:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Dec 2020 17:04:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:01 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 11 Dec 2020 17:05:31 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 11 Dec 2020 17:05:31 GMT
ENV MYSQL_VERSION=5.7.32-1debian10
# Fri, 11 Dec 2020 17:05:32 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 11 Dec 2020 17:05:55 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 11 Dec 2020 17:05:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 21 Dec 2020 20:34:42 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Mon, 21 Dec 2020 20:34:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 21 Dec 2020 20:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Dec 2020 20:34:43 GMT
EXPOSE 3306 33060
# Mon, 21 Dec 2020 20:34:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd960d34819b836a86d505ec5d22361c43a4a6df2c8763f2b96ba9f39e8a9d`  
		Last Modified: Fri, 11 Dec 2020 17:07:18 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab947313861c1a794864761bac953e6280da23bca3515156f7159aaa2b62ce1`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 4.2 MB (4178330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f92f19e63856fe7746b7f86dbc0aa50aecd52a43c26421e005493bdd14a12a`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 1.4 MB (1419183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e80b17bff96a7c7a8ceff95e27c30ca6c0c3211ec8c6c3532b0f83bdd8b407f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e976799f91c10d5acc4d9e71a3ddbdc9e2ba0efe1f9251ece7823a09bdf8c`  
		Last Modified: Fri, 11 Dec 2020 17:07:20 GMT  
		Size: 13.4 MB (13447254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ae84fee1b32077b44663fa381bf450c81d17722b0b7c7531744eb3a810385f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1da2a18e2e2b5f6ca1f752e656f5c88186d6f41e7745f7752f2aed32cdf899`  
		Last Modified: Fri, 11 Dec 2020 17:07:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301a28b700b92c71e7cbbaecb97bfac30cb7537bdc187c90b7934787522e0364`  
		Last Modified: Fri, 11 Dec 2020 17:08:01 GMT  
		Size: 108.3 MB (108346148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529dc8dbeaf3452bf9024df02320ad730c5e75a03a74ffb9960fab664dc62522`  
		Last Modified: Mon, 21 Dec 2020 20:35:14 GMT  
		Size: 5.1 KB (5138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9d021dc13f517a205ba5ccf944162d652b64d7ac09c23c81e6a4ef86096360`  
		Last Modified: Mon, 21 Dec 2020 20:35:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.32`

```console
$ docker pull mysql@sha256:c3a567d3e3ad8b05dfce401ed08f0f6bf3f3b64cc17694979d5f2e5d78e10173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.32` - linux; amd64

```console
$ docker pull mysql@sha256:360d1924d86cbf416f2c84687c2037e153080fed932798a73c5c6b4ceb7399e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154499935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07dfa83b5283f486f1fa1628cb8b4a18a4d071a486708acc5c06243ca7f592a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:04:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Dec 2020 17:04:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:04:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 11 Dec 2020 17:04:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Dec 2020 17:04:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Dec 2020 17:04:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:01 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 11 Dec 2020 17:05:31 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 11 Dec 2020 17:05:31 GMT
ENV MYSQL_VERSION=5.7.32-1debian10
# Fri, 11 Dec 2020 17:05:32 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 11 Dec 2020 17:05:55 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 11 Dec 2020 17:05:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 21 Dec 2020 20:34:42 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Mon, 21 Dec 2020 20:34:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 21 Dec 2020 20:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Dec 2020 20:34:43 GMT
EXPOSE 3306 33060
# Mon, 21 Dec 2020 20:34:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd960d34819b836a86d505ec5d22361c43a4a6df2c8763f2b96ba9f39e8a9d`  
		Last Modified: Fri, 11 Dec 2020 17:07:18 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab947313861c1a794864761bac953e6280da23bca3515156f7159aaa2b62ce1`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 4.2 MB (4178330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f92f19e63856fe7746b7f86dbc0aa50aecd52a43c26421e005493bdd14a12a`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 1.4 MB (1419183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e80b17bff96a7c7a8ceff95e27c30ca6c0c3211ec8c6c3532b0f83bdd8b407f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e976799f91c10d5acc4d9e71a3ddbdc9e2ba0efe1f9251ece7823a09bdf8c`  
		Last Modified: Fri, 11 Dec 2020 17:07:20 GMT  
		Size: 13.4 MB (13447254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ae84fee1b32077b44663fa381bf450c81d17722b0b7c7531744eb3a810385f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1da2a18e2e2b5f6ca1f752e656f5c88186d6f41e7745f7752f2aed32cdf899`  
		Last Modified: Fri, 11 Dec 2020 17:07:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301a28b700b92c71e7cbbaecb97bfac30cb7537bdc187c90b7934787522e0364`  
		Last Modified: Fri, 11 Dec 2020 17:08:01 GMT  
		Size: 108.3 MB (108346148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529dc8dbeaf3452bf9024df02320ad730c5e75a03a74ffb9960fab664dc62522`  
		Last Modified: Mon, 21 Dec 2020 20:35:14 GMT  
		Size: 5.1 KB (5138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9d021dc13f517a205ba5ccf944162d652b64d7ac09c23c81e6a4ef86096360`  
		Last Modified: Mon, 21 Dec 2020 20:35:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:78800e6d3f1b230e35275145e657b82c3fb02a27b2d8e76aac2f5e90c1c30873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:dce31fcdd15aaedb5591aa89f19ec37cb79981af46511781fa41287d88ed0abd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158954275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a347a59280467629ae4d70ce555e3f96faca8ff2ff8c57cacc8184bebb681f66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:04:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Dec 2020 17:04:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:04:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 11 Dec 2020 17:04:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Dec 2020 17:04:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Dec 2020 17:04:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:01 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 11 Dec 2020 17:05:01 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Dec 2020 17:05:01 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Fri, 11 Dec 2020 17:05:02 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 11 Dec 2020 17:05:18 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 11 Dec 2020 17:05:18 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Dec 2020 17:05:18 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Mon, 21 Dec 2020 20:34:36 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Mon, 21 Dec 2020 20:34:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 21 Dec 2020 20:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Dec 2020 20:34:37 GMT
EXPOSE 3306 33060
# Mon, 21 Dec 2020 20:34:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd960d34819b836a86d505ec5d22361c43a4a6df2c8763f2b96ba9f39e8a9d`  
		Last Modified: Fri, 11 Dec 2020 17:07:18 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab947313861c1a794864761bac953e6280da23bca3515156f7159aaa2b62ce1`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 4.2 MB (4178330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f92f19e63856fe7746b7f86dbc0aa50aecd52a43c26421e005493bdd14a12a`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 1.4 MB (1419183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e80b17bff96a7c7a8ceff95e27c30ca6c0c3211ec8c6c3532b0f83bdd8b407f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e976799f91c10d5acc4d9e71a3ddbdc9e2ba0efe1f9251ece7823a09bdf8c`  
		Last Modified: Fri, 11 Dec 2020 17:07:20 GMT  
		Size: 13.4 MB (13447254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ae84fee1b32077b44663fa381bf450c81d17722b0b7c7531744eb3a810385f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe10de703eacbbaa29d6ff64c747a8e1f5d3aa8f1157ea4c241fc80e90e9f99`  
		Last Modified: Fri, 11 Dec 2020 17:07:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657af6d90c8389128c5a128e2f5f203e5fb6b98f2c9ff11adb794fc72abcf74c`  
		Last Modified: Fri, 11 Dec 2020 17:07:35 GMT  
		Size: 112.8 MB (112799640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bfb480322c562416481bdaf12b4d64ee5725e257ec6cbee1dae15ac0d54e5f`  
		Last Modified: Fri, 11 Dec 2020 17:07:14 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa3859c478957376cafdcee5fb31795bb80d2cabf5286b75befa2f3ffd33a4c`  
		Last Modified: Mon, 21 Dec 2020 20:35:04 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed875d851ef8f2e38ba3613a07e307054344fbab82b41fdcfa200b18c7d567e`  
		Last Modified: Mon, 21 Dec 2020 20:35:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:78800e6d3f1b230e35275145e657b82c3fb02a27b2d8e76aac2f5e90c1c30873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:dce31fcdd15aaedb5591aa89f19ec37cb79981af46511781fa41287d88ed0abd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158954275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a347a59280467629ae4d70ce555e3f96faca8ff2ff8c57cacc8184bebb681f66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:04:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Dec 2020 17:04:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:04:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 11 Dec 2020 17:04:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Dec 2020 17:04:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Dec 2020 17:04:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:01 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 11 Dec 2020 17:05:01 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Dec 2020 17:05:01 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Fri, 11 Dec 2020 17:05:02 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 11 Dec 2020 17:05:18 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 11 Dec 2020 17:05:18 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Dec 2020 17:05:18 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Mon, 21 Dec 2020 20:34:36 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Mon, 21 Dec 2020 20:34:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 21 Dec 2020 20:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Dec 2020 20:34:37 GMT
EXPOSE 3306 33060
# Mon, 21 Dec 2020 20:34:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd960d34819b836a86d505ec5d22361c43a4a6df2c8763f2b96ba9f39e8a9d`  
		Last Modified: Fri, 11 Dec 2020 17:07:18 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab947313861c1a794864761bac953e6280da23bca3515156f7159aaa2b62ce1`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 4.2 MB (4178330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f92f19e63856fe7746b7f86dbc0aa50aecd52a43c26421e005493bdd14a12a`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 1.4 MB (1419183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e80b17bff96a7c7a8ceff95e27c30ca6c0c3211ec8c6c3532b0f83bdd8b407f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e976799f91c10d5acc4d9e71a3ddbdc9e2ba0efe1f9251ece7823a09bdf8c`  
		Last Modified: Fri, 11 Dec 2020 17:07:20 GMT  
		Size: 13.4 MB (13447254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ae84fee1b32077b44663fa381bf450c81d17722b0b7c7531744eb3a810385f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe10de703eacbbaa29d6ff64c747a8e1f5d3aa8f1157ea4c241fc80e90e9f99`  
		Last Modified: Fri, 11 Dec 2020 17:07:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657af6d90c8389128c5a128e2f5f203e5fb6b98f2c9ff11adb794fc72abcf74c`  
		Last Modified: Fri, 11 Dec 2020 17:07:35 GMT  
		Size: 112.8 MB (112799640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bfb480322c562416481bdaf12b4d64ee5725e257ec6cbee1dae15ac0d54e5f`  
		Last Modified: Fri, 11 Dec 2020 17:07:14 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa3859c478957376cafdcee5fb31795bb80d2cabf5286b75befa2f3ffd33a4c`  
		Last Modified: Mon, 21 Dec 2020 20:35:04 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed875d851ef8f2e38ba3613a07e307054344fbab82b41fdcfa200b18c7d567e`  
		Last Modified: Mon, 21 Dec 2020 20:35:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.22`

```console
$ docker pull mysql@sha256:78800e6d3f1b230e35275145e657b82c3fb02a27b2d8e76aac2f5e90c1c30873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.22` - linux; amd64

```console
$ docker pull mysql@sha256:dce31fcdd15aaedb5591aa89f19ec37cb79981af46511781fa41287d88ed0abd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158954275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a347a59280467629ae4d70ce555e3f96faca8ff2ff8c57cacc8184bebb681f66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:04:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Dec 2020 17:04:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:04:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 11 Dec 2020 17:04:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Dec 2020 17:04:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Dec 2020 17:04:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:01 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 11 Dec 2020 17:05:01 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Dec 2020 17:05:01 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Fri, 11 Dec 2020 17:05:02 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 11 Dec 2020 17:05:18 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 11 Dec 2020 17:05:18 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Dec 2020 17:05:18 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Mon, 21 Dec 2020 20:34:36 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Mon, 21 Dec 2020 20:34:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 21 Dec 2020 20:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Dec 2020 20:34:37 GMT
EXPOSE 3306 33060
# Mon, 21 Dec 2020 20:34:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd960d34819b836a86d505ec5d22361c43a4a6df2c8763f2b96ba9f39e8a9d`  
		Last Modified: Fri, 11 Dec 2020 17:07:18 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab947313861c1a794864761bac953e6280da23bca3515156f7159aaa2b62ce1`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 4.2 MB (4178330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f92f19e63856fe7746b7f86dbc0aa50aecd52a43c26421e005493bdd14a12a`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 1.4 MB (1419183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e80b17bff96a7c7a8ceff95e27c30ca6c0c3211ec8c6c3532b0f83bdd8b407f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e976799f91c10d5acc4d9e71a3ddbdc9e2ba0efe1f9251ece7823a09bdf8c`  
		Last Modified: Fri, 11 Dec 2020 17:07:20 GMT  
		Size: 13.4 MB (13447254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ae84fee1b32077b44663fa381bf450c81d17722b0b7c7531744eb3a810385f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe10de703eacbbaa29d6ff64c747a8e1f5d3aa8f1157ea4c241fc80e90e9f99`  
		Last Modified: Fri, 11 Dec 2020 17:07:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657af6d90c8389128c5a128e2f5f203e5fb6b98f2c9ff11adb794fc72abcf74c`  
		Last Modified: Fri, 11 Dec 2020 17:07:35 GMT  
		Size: 112.8 MB (112799640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bfb480322c562416481bdaf12b4d64ee5725e257ec6cbee1dae15ac0d54e5f`  
		Last Modified: Fri, 11 Dec 2020 17:07:14 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa3859c478957376cafdcee5fb31795bb80d2cabf5286b75befa2f3ffd33a4c`  
		Last Modified: Mon, 21 Dec 2020 20:35:04 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed875d851ef8f2e38ba3613a07e307054344fbab82b41fdcfa200b18c7d567e`  
		Last Modified: Mon, 21 Dec 2020 20:35:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:78800e6d3f1b230e35275145e657b82c3fb02a27b2d8e76aac2f5e90c1c30873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:dce31fcdd15aaedb5591aa89f19ec37cb79981af46511781fa41287d88ed0abd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158954275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a347a59280467629ae4d70ce555e3f96faca8ff2ff8c57cacc8184bebb681f66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:04:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Dec 2020 17:04:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:04:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 11 Dec 2020 17:04:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Dec 2020 17:04:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Dec 2020 17:04:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:01 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 11 Dec 2020 17:05:01 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Dec 2020 17:05:01 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Fri, 11 Dec 2020 17:05:02 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 11 Dec 2020 17:05:18 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 11 Dec 2020 17:05:18 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Dec 2020 17:05:18 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Mon, 21 Dec 2020 20:34:36 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Mon, 21 Dec 2020 20:34:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 21 Dec 2020 20:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Dec 2020 20:34:37 GMT
EXPOSE 3306 33060
# Mon, 21 Dec 2020 20:34:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd960d34819b836a86d505ec5d22361c43a4a6df2c8763f2b96ba9f39e8a9d`  
		Last Modified: Fri, 11 Dec 2020 17:07:18 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab947313861c1a794864761bac953e6280da23bca3515156f7159aaa2b62ce1`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 4.2 MB (4178330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f92f19e63856fe7746b7f86dbc0aa50aecd52a43c26421e005493bdd14a12a`  
		Last Modified: Fri, 11 Dec 2020 17:07:17 GMT  
		Size: 1.4 MB (1419183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e80b17bff96a7c7a8ceff95e27c30ca6c0c3211ec8c6c3532b0f83bdd8b407f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e976799f91c10d5acc4d9e71a3ddbdc9e2ba0efe1f9251ece7823a09bdf8c`  
		Last Modified: Fri, 11 Dec 2020 17:07:20 GMT  
		Size: 13.4 MB (13447254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ae84fee1b32077b44663fa381bf450c81d17722b0b7c7531744eb3a810385f`  
		Last Modified: Fri, 11 Dec 2020 17:07:16 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe10de703eacbbaa29d6ff64c747a8e1f5d3aa8f1157ea4c241fc80e90e9f99`  
		Last Modified: Fri, 11 Dec 2020 17:07:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657af6d90c8389128c5a128e2f5f203e5fb6b98f2c9ff11adb794fc72abcf74c`  
		Last Modified: Fri, 11 Dec 2020 17:07:35 GMT  
		Size: 112.8 MB (112799640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bfb480322c562416481bdaf12b4d64ee5725e257ec6cbee1dae15ac0d54e5f`  
		Last Modified: Fri, 11 Dec 2020 17:07:14 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa3859c478957376cafdcee5fb31795bb80d2cabf5286b75befa2f3ffd33a4c`  
		Last Modified: Mon, 21 Dec 2020 20:35:04 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed875d851ef8f2e38ba3613a07e307054344fbab82b41fdcfa200b18c7d567e`  
		Last Modified: Mon, 21 Dec 2020 20:35:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
