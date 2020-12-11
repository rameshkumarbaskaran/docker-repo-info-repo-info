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
$ docker pull mysql@sha256:d4ca82cee68dce98aa72a1c48b5ef5ce9f1538265831132187871b78e768aed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:b3b2703de646600b008cbb2de36b70b21e51e7e93a7fca450d2b08151658b2dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154499933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697daaecf703e82e8755034e816282fc3e912151b7818c85af8647fdcdcee517`
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
# Fri, 11 Dec 2020 17:05:56 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Fri, 11 Dec 2020 17:05:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 17:05:57 GMT
EXPOSE 3306 33060
# Fri, 11 Dec 2020 17:05:57 GMT
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
	-	`sha256:979b389fc71f58fc71b1cd07d3500e9873e45d7064217e492f6fd51de43c96f9`  
		Last Modified: Fri, 11 Dec 2020 17:07:43 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403f729b1bad4c2514a641029adf21f81d9dcb418201444d55df88a43e4551e1`  
		Last Modified: Fri, 11 Dec 2020 17:07:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:5cb02288931d4d9f3ac9a837cb84bf1b1b40542fb714f5bfa9d6f07cc9e976d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:d8e4032005f53a774f2361281ebf61fa3d7635d5dacf9c58bc54e823ddcf9f1d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102938341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61c95a9851455112a52f8eb1aab6616569e32e6b8e087b1e3330ea50005508f`
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
# Fri, 11 Dec 2020 17:06:53 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Fri, 11 Dec 2020 17:06:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 17:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 17:06:55 GMT
EXPOSE 3306
# Fri, 11 Dec 2020 17:06:55 GMT
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
	-	`sha256:fb5fe413de46fa14078d778c3c868791d4f03a2058b6f125751f95f448fc3d6c`  
		Last Modified: Fri, 11 Dec 2020 17:08:08 GMT  
		Size: 5.2 KB (5151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a75b492613dc7b97fa038e386cdc12b6e24d5a71e21a508d058788bf72428fe`  
		Last Modified: Fri, 11 Dec 2020 17:08:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.50`

```console
$ docker pull mysql@sha256:5cb02288931d4d9f3ac9a837cb84bf1b1b40542fb714f5bfa9d6f07cc9e976d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.50` - linux; amd64

```console
$ docker pull mysql@sha256:d8e4032005f53a774f2361281ebf61fa3d7635d5dacf9c58bc54e823ddcf9f1d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102938341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61c95a9851455112a52f8eb1aab6616569e32e6b8e087b1e3330ea50005508f`
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
# Fri, 11 Dec 2020 17:06:53 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Fri, 11 Dec 2020 17:06:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 17:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 17:06:55 GMT
EXPOSE 3306
# Fri, 11 Dec 2020 17:06:55 GMT
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
	-	`sha256:fb5fe413de46fa14078d778c3c868791d4f03a2058b6f125751f95f448fc3d6c`  
		Last Modified: Fri, 11 Dec 2020 17:08:08 GMT  
		Size: 5.2 KB (5151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a75b492613dc7b97fa038e386cdc12b6e24d5a71e21a508d058788bf72428fe`  
		Last Modified: Fri, 11 Dec 2020 17:08:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:d4ca82cee68dce98aa72a1c48b5ef5ce9f1538265831132187871b78e768aed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:b3b2703de646600b008cbb2de36b70b21e51e7e93a7fca450d2b08151658b2dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154499933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697daaecf703e82e8755034e816282fc3e912151b7818c85af8647fdcdcee517`
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
# Fri, 11 Dec 2020 17:05:56 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Fri, 11 Dec 2020 17:05:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 17:05:57 GMT
EXPOSE 3306 33060
# Fri, 11 Dec 2020 17:05:57 GMT
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
	-	`sha256:979b389fc71f58fc71b1cd07d3500e9873e45d7064217e492f6fd51de43c96f9`  
		Last Modified: Fri, 11 Dec 2020 17:07:43 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403f729b1bad4c2514a641029adf21f81d9dcb418201444d55df88a43e4551e1`  
		Last Modified: Fri, 11 Dec 2020 17:07:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.32`

```console
$ docker pull mysql@sha256:d4ca82cee68dce98aa72a1c48b5ef5ce9f1538265831132187871b78e768aed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.32` - linux; amd64

```console
$ docker pull mysql@sha256:b3b2703de646600b008cbb2de36b70b21e51e7e93a7fca450d2b08151658b2dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154499933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697daaecf703e82e8755034e816282fc3e912151b7818c85af8647fdcdcee517`
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
# Fri, 11 Dec 2020 17:05:56 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Fri, 11 Dec 2020 17:05:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 17:05:57 GMT
EXPOSE 3306 33060
# Fri, 11 Dec 2020 17:05:57 GMT
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
	-	`sha256:979b389fc71f58fc71b1cd07d3500e9873e45d7064217e492f6fd51de43c96f9`  
		Last Modified: Fri, 11 Dec 2020 17:07:43 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403f729b1bad4c2514a641029adf21f81d9dcb418201444d55df88a43e4551e1`  
		Last Modified: Fri, 11 Dec 2020 17:07:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:365e891b22abd3336d65baefc475b4a9a1e29a01a7b6b5be04367fcc9f373bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:9ea5b1010711123ab241f86b9aafeee0e4c425942a651a0ea3c2817e369c086a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158954270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2f358b86124c477cc1f91066d42ca15fb2da58f029aa3c4312de5b3ca02018`
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
# Fri, 11 Dec 2020 17:05:18 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Fri, 11 Dec 2020 17:05:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 17:05:20 GMT
EXPOSE 3306 33060
# Fri, 11 Dec 2020 17:05:20 GMT
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
	-	`sha256:9f2c4202ac29b8cd1ab34cea7c64f0ea6a15358fc9afcba83144085cb9018ab5`  
		Last Modified: Fri, 11 Dec 2020 17:07:14 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a369b92bfc99a7fc1d2324942f41c4fcb1e5d3d74e60d2573c7ed18f9b529050`  
		Last Modified: Fri, 11 Dec 2020 17:07:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:365e891b22abd3336d65baefc475b4a9a1e29a01a7b6b5be04367fcc9f373bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:9ea5b1010711123ab241f86b9aafeee0e4c425942a651a0ea3c2817e369c086a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158954270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2f358b86124c477cc1f91066d42ca15fb2da58f029aa3c4312de5b3ca02018`
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
# Fri, 11 Dec 2020 17:05:18 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Fri, 11 Dec 2020 17:05:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 17:05:20 GMT
EXPOSE 3306 33060
# Fri, 11 Dec 2020 17:05:20 GMT
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
	-	`sha256:9f2c4202ac29b8cd1ab34cea7c64f0ea6a15358fc9afcba83144085cb9018ab5`  
		Last Modified: Fri, 11 Dec 2020 17:07:14 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a369b92bfc99a7fc1d2324942f41c4fcb1e5d3d74e60d2573c7ed18f9b529050`  
		Last Modified: Fri, 11 Dec 2020 17:07:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.22`

```console
$ docker pull mysql@sha256:365e891b22abd3336d65baefc475b4a9a1e29a01a7b6b5be04367fcc9f373bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.22` - linux; amd64

```console
$ docker pull mysql@sha256:9ea5b1010711123ab241f86b9aafeee0e4c425942a651a0ea3c2817e369c086a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158954270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2f358b86124c477cc1f91066d42ca15fb2da58f029aa3c4312de5b3ca02018`
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
# Fri, 11 Dec 2020 17:05:18 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Fri, 11 Dec 2020 17:05:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 17:05:20 GMT
EXPOSE 3306 33060
# Fri, 11 Dec 2020 17:05:20 GMT
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
	-	`sha256:9f2c4202ac29b8cd1ab34cea7c64f0ea6a15358fc9afcba83144085cb9018ab5`  
		Last Modified: Fri, 11 Dec 2020 17:07:14 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a369b92bfc99a7fc1d2324942f41c4fcb1e5d3d74e60d2573c7ed18f9b529050`  
		Last Modified: Fri, 11 Dec 2020 17:07:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:365e891b22abd3336d65baefc475b4a9a1e29a01a7b6b5be04367fcc9f373bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:9ea5b1010711123ab241f86b9aafeee0e4c425942a651a0ea3c2817e369c086a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158954270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2f358b86124c477cc1f91066d42ca15fb2da58f029aa3c4312de5b3ca02018`
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
# Fri, 11 Dec 2020 17:05:18 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Fri, 11 Dec 2020 17:05:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 17:05:20 GMT
EXPOSE 3306 33060
# Fri, 11 Dec 2020 17:05:20 GMT
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
	-	`sha256:9f2c4202ac29b8cd1ab34cea7c64f0ea6a15358fc9afcba83144085cb9018ab5`  
		Last Modified: Fri, 11 Dec 2020 17:07:14 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a369b92bfc99a7fc1d2324942f41c4fcb1e5d3d74e60d2573c7ed18f9b529050`  
		Last Modified: Fri, 11 Dec 2020 17:07:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
