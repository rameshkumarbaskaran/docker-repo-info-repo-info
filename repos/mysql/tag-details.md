<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.49`](#mysql5649)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.31`](#mysql5731)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.21`](#mysql8021)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:14fd47ec8724954b63d1a236d2299b8da25c9bbb8eacc739bb88038d82da4919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:9e902247f80eca2e0fc4179f48a91afbe3b2a61122dd5e7575b5f0549aab97d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154474458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef08065b0a302111b56966aa92c89fa0bacdfc537741cbca88a15b10f14332ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:53:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 10 Sep 2020 06:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Sep 2020 06:53:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Sep 2020 06:53:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Sep 2020 06:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:38 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 10 Sep 2020 06:54:07 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 10 Sep 2020 06:54:07 GMT
ENV MYSQL_VERSION=5.7.31-1debian10
# Thu, 10 Sep 2020 06:54:08 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 10 Sep 2020 06:54:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 10 Sep 2020 06:54:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 10 Sep 2020 06:54:32 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 10 Sep 2020 06:54:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 06:54:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Sep 2020 06:54:33 GMT
EXPOSE 3306 33060
# Thu, 10 Sep 2020 06:54:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cebc0b46913f0ab62528142684580ec1e3559f7c3571b2d53eccb656fbf308`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1862755a0b378cf709262d121db21ca934437463f647c7eeb1dd328869df9743`  
		Last Modified: Thu, 10 Sep 2020 06:56:11 GMT  
		Size: 4.2 MB (4178114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489b44f3dbb4c3b4fb955823e880352f6acfe001b1f41c8dcc81fac58622ee29`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.4 MB (1419211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690874f836dbbd1fc19486ed7d1d09084fc88cb8a1a873228ff987700314d91c`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa8be383ffb08bae1621a739dffb09ef152a476bdf23fa43ab902a5a330b7f2`  
		Last Modified: Thu, 10 Sep 2020 06:56:16 GMT  
		Size: 13.4 MB (13447130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55356608b4ac46e974b166adeb8207e78938059004277e38257ae1e0b5e517aa`  
		Last Modified: Thu, 10 Sep 2020 06:56:09 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277d8f888368515d82ac9233d5b396a2c5d4f8719a2d13d100cc18490a217483`  
		Last Modified: Thu, 10 Sep 2020 06:56:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f2da6feb6711dcfdb19aa6d95949f3a2531abfc0d0324b227760d50d4874e1`  
		Last Modified: Thu, 10 Sep 2020 06:57:06 GMT  
		Size: 108.3 MB (108328100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c98f818bcb915b3d9d17b2054c79f05090ae0a5e1aa442eadeb62054a7d201b`  
		Last Modified: Thu, 10 Sep 2020 06:56:47 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031b0a770162c53689705fe09d25791ad2732a6ca29067c74831c0a7ccfe361d`  
		Last Modified: Thu, 10 Sep 2020 06:56:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:149e4fcf1c8e63117d0548d4f98b0b62c16fc4061f7b26e4281744189063cf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:bfcef110bc3892d329ea483fd3e69fc5162a36f1b9089275c7f8bf64717787c0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102930359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44241dbd4d38e96362789edfe0743d6cd2cb81322cd788fd448fcad37d652fec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:54:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 10 Sep 2020 06:54:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:54:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Sep 2020 06:55:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Sep 2020 06:55:04 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Sep 2020 06:55:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:55:19 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 10 Sep 2020 06:55:20 GMT
ENV MYSQL_MAJOR=5.6
# Thu, 10 Sep 2020 06:55:20 GMT
ENV MYSQL_VERSION=5.6.49-1debian9
# Thu, 10 Sep 2020 06:55:21 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 10 Sep 2020 06:55:45 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 10 Sep 2020 06:55:45 GMT
VOLUME [/var/lib/mysql]
# Thu, 10 Sep 2020 06:55:46 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 10 Sep 2020 06:55:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 06:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Sep 2020 06:55:48 GMT
EXPOSE 3306
# Thu, 10 Sep 2020 06:55:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c63fd0e6a8d461ca9ff99347f4b63ad3613e451de0e7b598f59bbad6efb222f`  
		Last Modified: Thu, 10 Sep 2020 06:57:14 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d0dd6b202f94d33c01b2fd73d5107e42c4bf98d2f31762d9031580793f3b0`  
		Last Modified: Thu, 10 Sep 2020 06:57:15 GMT  
		Size: 4.5 MB (4502003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c2a492ee4c990b3a686e5def9e1af45b151a7a8fff2e9a410f671e3ee3fc84`  
		Last Modified: Thu, 10 Sep 2020 06:57:13 GMT  
		Size: 1.4 MB (1412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af4bf164c41d636b60f6ff915cee2d0629205a9f8fba839d108faf9593e52a`  
		Last Modified: Thu, 10 Sep 2020 06:57:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca7652d449e48d03673a104bd36a02525394a555cfc172485dcfd5f72e8e723`  
		Last Modified: Thu, 10 Sep 2020 06:57:18 GMT  
		Size: 10.2 MB (10224996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c4cf5588992fa83730cbb5a8323a5d788b8443a9c95754390560b0245689e7`  
		Last Modified: Thu, 10 Sep 2020 06:57:11 GMT  
		Size: 28.7 KB (28652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e913f976f3603bc02cf3f09db3263a410e9c22bf0a65968a61ab2076aec77e7`  
		Last Modified: Thu, 10 Sep 2020 06:57:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fa36a96f170425b396a6f07135e84ae1ba747994549bc36639eb64fc4ee097`  
		Last Modified: Thu, 10 Sep 2020 06:57:30 GMT  
		Size: 64.2 MB (64233000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea732f57b53ae0059abd0c476c729d52cd4359fa963927b1bff3a268718c48c2`  
		Last Modified: Thu, 10 Sep 2020 06:57:12 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe3789c9297baf7439a809b8065596a57825779968d06da6bbba4811dcfa53a`  
		Last Modified: Thu, 10 Sep 2020 06:57:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.49`

```console
$ docker pull mysql@sha256:149e4fcf1c8e63117d0548d4f98b0b62c16fc4061f7b26e4281744189063cf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.49` - linux; amd64

```console
$ docker pull mysql@sha256:bfcef110bc3892d329ea483fd3e69fc5162a36f1b9089275c7f8bf64717787c0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102930359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44241dbd4d38e96362789edfe0743d6cd2cb81322cd788fd448fcad37d652fec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:54:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 10 Sep 2020 06:54:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:54:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Sep 2020 06:55:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Sep 2020 06:55:04 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Sep 2020 06:55:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:55:19 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 10 Sep 2020 06:55:20 GMT
ENV MYSQL_MAJOR=5.6
# Thu, 10 Sep 2020 06:55:20 GMT
ENV MYSQL_VERSION=5.6.49-1debian9
# Thu, 10 Sep 2020 06:55:21 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 10 Sep 2020 06:55:45 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 10 Sep 2020 06:55:45 GMT
VOLUME [/var/lib/mysql]
# Thu, 10 Sep 2020 06:55:46 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 10 Sep 2020 06:55:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 06:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Sep 2020 06:55:48 GMT
EXPOSE 3306
# Thu, 10 Sep 2020 06:55:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c63fd0e6a8d461ca9ff99347f4b63ad3613e451de0e7b598f59bbad6efb222f`  
		Last Modified: Thu, 10 Sep 2020 06:57:14 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d0dd6b202f94d33c01b2fd73d5107e42c4bf98d2f31762d9031580793f3b0`  
		Last Modified: Thu, 10 Sep 2020 06:57:15 GMT  
		Size: 4.5 MB (4502003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c2a492ee4c990b3a686e5def9e1af45b151a7a8fff2e9a410f671e3ee3fc84`  
		Last Modified: Thu, 10 Sep 2020 06:57:13 GMT  
		Size: 1.4 MB (1412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af4bf164c41d636b60f6ff915cee2d0629205a9f8fba839d108faf9593e52a`  
		Last Modified: Thu, 10 Sep 2020 06:57:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca7652d449e48d03673a104bd36a02525394a555cfc172485dcfd5f72e8e723`  
		Last Modified: Thu, 10 Sep 2020 06:57:18 GMT  
		Size: 10.2 MB (10224996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c4cf5588992fa83730cbb5a8323a5d788b8443a9c95754390560b0245689e7`  
		Last Modified: Thu, 10 Sep 2020 06:57:11 GMT  
		Size: 28.7 KB (28652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e913f976f3603bc02cf3f09db3263a410e9c22bf0a65968a61ab2076aec77e7`  
		Last Modified: Thu, 10 Sep 2020 06:57:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fa36a96f170425b396a6f07135e84ae1ba747994549bc36639eb64fc4ee097`  
		Last Modified: Thu, 10 Sep 2020 06:57:30 GMT  
		Size: 64.2 MB (64233000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea732f57b53ae0059abd0c476c729d52cd4359fa963927b1bff3a268718c48c2`  
		Last Modified: Thu, 10 Sep 2020 06:57:12 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe3789c9297baf7439a809b8065596a57825779968d06da6bbba4811dcfa53a`  
		Last Modified: Thu, 10 Sep 2020 06:57:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:14fd47ec8724954b63d1a236d2299b8da25c9bbb8eacc739bb88038d82da4919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:9e902247f80eca2e0fc4179f48a91afbe3b2a61122dd5e7575b5f0549aab97d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154474458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef08065b0a302111b56966aa92c89fa0bacdfc537741cbca88a15b10f14332ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:53:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 10 Sep 2020 06:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Sep 2020 06:53:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Sep 2020 06:53:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Sep 2020 06:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:38 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 10 Sep 2020 06:54:07 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 10 Sep 2020 06:54:07 GMT
ENV MYSQL_VERSION=5.7.31-1debian10
# Thu, 10 Sep 2020 06:54:08 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 10 Sep 2020 06:54:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 10 Sep 2020 06:54:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 10 Sep 2020 06:54:32 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 10 Sep 2020 06:54:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 06:54:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Sep 2020 06:54:33 GMT
EXPOSE 3306 33060
# Thu, 10 Sep 2020 06:54:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cebc0b46913f0ab62528142684580ec1e3559f7c3571b2d53eccb656fbf308`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1862755a0b378cf709262d121db21ca934437463f647c7eeb1dd328869df9743`  
		Last Modified: Thu, 10 Sep 2020 06:56:11 GMT  
		Size: 4.2 MB (4178114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489b44f3dbb4c3b4fb955823e880352f6acfe001b1f41c8dcc81fac58622ee29`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.4 MB (1419211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690874f836dbbd1fc19486ed7d1d09084fc88cb8a1a873228ff987700314d91c`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa8be383ffb08bae1621a739dffb09ef152a476bdf23fa43ab902a5a330b7f2`  
		Last Modified: Thu, 10 Sep 2020 06:56:16 GMT  
		Size: 13.4 MB (13447130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55356608b4ac46e974b166adeb8207e78938059004277e38257ae1e0b5e517aa`  
		Last Modified: Thu, 10 Sep 2020 06:56:09 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277d8f888368515d82ac9233d5b396a2c5d4f8719a2d13d100cc18490a217483`  
		Last Modified: Thu, 10 Sep 2020 06:56:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f2da6feb6711dcfdb19aa6d95949f3a2531abfc0d0324b227760d50d4874e1`  
		Last Modified: Thu, 10 Sep 2020 06:57:06 GMT  
		Size: 108.3 MB (108328100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c98f818bcb915b3d9d17b2054c79f05090ae0a5e1aa442eadeb62054a7d201b`  
		Last Modified: Thu, 10 Sep 2020 06:56:47 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031b0a770162c53689705fe09d25791ad2732a6ca29067c74831c0a7ccfe361d`  
		Last Modified: Thu, 10 Sep 2020 06:56:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.31`

```console
$ docker pull mysql@sha256:14fd47ec8724954b63d1a236d2299b8da25c9bbb8eacc739bb88038d82da4919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.31` - linux; amd64

```console
$ docker pull mysql@sha256:9e902247f80eca2e0fc4179f48a91afbe3b2a61122dd5e7575b5f0549aab97d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154474458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef08065b0a302111b56966aa92c89fa0bacdfc537741cbca88a15b10f14332ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:53:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 10 Sep 2020 06:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Sep 2020 06:53:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Sep 2020 06:53:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Sep 2020 06:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:38 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 10 Sep 2020 06:54:07 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 10 Sep 2020 06:54:07 GMT
ENV MYSQL_VERSION=5.7.31-1debian10
# Thu, 10 Sep 2020 06:54:08 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 10 Sep 2020 06:54:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Thu, 10 Sep 2020 06:54:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 10 Sep 2020 06:54:32 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 10 Sep 2020 06:54:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 06:54:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Sep 2020 06:54:33 GMT
EXPOSE 3306 33060
# Thu, 10 Sep 2020 06:54:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cebc0b46913f0ab62528142684580ec1e3559f7c3571b2d53eccb656fbf308`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1862755a0b378cf709262d121db21ca934437463f647c7eeb1dd328869df9743`  
		Last Modified: Thu, 10 Sep 2020 06:56:11 GMT  
		Size: 4.2 MB (4178114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489b44f3dbb4c3b4fb955823e880352f6acfe001b1f41c8dcc81fac58622ee29`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.4 MB (1419211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690874f836dbbd1fc19486ed7d1d09084fc88cb8a1a873228ff987700314d91c`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa8be383ffb08bae1621a739dffb09ef152a476bdf23fa43ab902a5a330b7f2`  
		Last Modified: Thu, 10 Sep 2020 06:56:16 GMT  
		Size: 13.4 MB (13447130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55356608b4ac46e974b166adeb8207e78938059004277e38257ae1e0b5e517aa`  
		Last Modified: Thu, 10 Sep 2020 06:56:09 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277d8f888368515d82ac9233d5b396a2c5d4f8719a2d13d100cc18490a217483`  
		Last Modified: Thu, 10 Sep 2020 06:56:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f2da6feb6711dcfdb19aa6d95949f3a2531abfc0d0324b227760d50d4874e1`  
		Last Modified: Thu, 10 Sep 2020 06:57:06 GMT  
		Size: 108.3 MB (108328100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c98f818bcb915b3d9d17b2054c79f05090ae0a5e1aa442eadeb62054a7d201b`  
		Last Modified: Thu, 10 Sep 2020 06:56:47 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031b0a770162c53689705fe09d25791ad2732a6ca29067c74831c0a7ccfe361d`  
		Last Modified: Thu, 10 Sep 2020 06:56:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:e1bfe11693ed2052cb3b4e5fa356c65381129e87e38551c6cd6ec532ebe0e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:b589f11ab39a852fd13090aeb56314978c73a16d615e28ec148306889b67889f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158633433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d7dc9731daa2c79858307d65ef35f543daf97457b9c11b681f78bb86f7a158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:53:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 10 Sep 2020 06:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Sep 2020 06:53:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Sep 2020 06:53:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Sep 2020 06:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:38 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 10 Sep 2020 06:53:38 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 10 Sep 2020 06:53:39 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Thu, 10 Sep 2020 06:53:39 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 10 Sep 2020 06:53:55 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 10 Sep 2020 06:53:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 10 Sep 2020 06:53:56 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 10 Sep 2020 06:53:56 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 10 Sep 2020 06:53:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 06:53:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Sep 2020 06:53:57 GMT
EXPOSE 3306 33060
# Thu, 10 Sep 2020 06:53:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cebc0b46913f0ab62528142684580ec1e3559f7c3571b2d53eccb656fbf308`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1862755a0b378cf709262d121db21ca934437463f647c7eeb1dd328869df9743`  
		Last Modified: Thu, 10 Sep 2020 06:56:11 GMT  
		Size: 4.2 MB (4178114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489b44f3dbb4c3b4fb955823e880352f6acfe001b1f41c8dcc81fac58622ee29`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.4 MB (1419211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690874f836dbbd1fc19486ed7d1d09084fc88cb8a1a873228ff987700314d91c`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa8be383ffb08bae1621a739dffb09ef152a476bdf23fa43ab902a5a330b7f2`  
		Last Modified: Thu, 10 Sep 2020 06:56:16 GMT  
		Size: 13.4 MB (13447130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55356608b4ac46e974b166adeb8207e78938059004277e38257ae1e0b5e517aa`  
		Last Modified: Thu, 10 Sep 2020 06:56:09 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd35ceccb6ebb923fead362e892aecdf0c78e9bf9871236edd37b939e9aa42b7`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429b35712b19f180a3b54050b0e06f2aba4604a93595a4e84aecbef5ae965756`  
		Last Modified: Thu, 10 Sep 2020 06:56:41 GMT  
		Size: 112.5 MB (112486232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162d8291095c7d95de5978bed455880ca417b35062409ccca428620a0e12e2d0`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e500ef7181b04f57c863f6a874500d2f1963976f66833ddba3238b3c0ca5949`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7528e958b6dbe6f2348a1a2035f2ba4b57f4742156f0d5cd0f2e763150d3c4`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:e1bfe11693ed2052cb3b4e5fa356c65381129e87e38551c6cd6ec532ebe0e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:b589f11ab39a852fd13090aeb56314978c73a16d615e28ec148306889b67889f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158633433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d7dc9731daa2c79858307d65ef35f543daf97457b9c11b681f78bb86f7a158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:53:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 10 Sep 2020 06:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Sep 2020 06:53:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Sep 2020 06:53:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Sep 2020 06:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:38 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 10 Sep 2020 06:53:38 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 10 Sep 2020 06:53:39 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Thu, 10 Sep 2020 06:53:39 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 10 Sep 2020 06:53:55 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 10 Sep 2020 06:53:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 10 Sep 2020 06:53:56 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 10 Sep 2020 06:53:56 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 10 Sep 2020 06:53:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 06:53:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Sep 2020 06:53:57 GMT
EXPOSE 3306 33060
# Thu, 10 Sep 2020 06:53:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cebc0b46913f0ab62528142684580ec1e3559f7c3571b2d53eccb656fbf308`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1862755a0b378cf709262d121db21ca934437463f647c7eeb1dd328869df9743`  
		Last Modified: Thu, 10 Sep 2020 06:56:11 GMT  
		Size: 4.2 MB (4178114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489b44f3dbb4c3b4fb955823e880352f6acfe001b1f41c8dcc81fac58622ee29`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.4 MB (1419211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690874f836dbbd1fc19486ed7d1d09084fc88cb8a1a873228ff987700314d91c`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa8be383ffb08bae1621a739dffb09ef152a476bdf23fa43ab902a5a330b7f2`  
		Last Modified: Thu, 10 Sep 2020 06:56:16 GMT  
		Size: 13.4 MB (13447130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55356608b4ac46e974b166adeb8207e78938059004277e38257ae1e0b5e517aa`  
		Last Modified: Thu, 10 Sep 2020 06:56:09 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd35ceccb6ebb923fead362e892aecdf0c78e9bf9871236edd37b939e9aa42b7`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429b35712b19f180a3b54050b0e06f2aba4604a93595a4e84aecbef5ae965756`  
		Last Modified: Thu, 10 Sep 2020 06:56:41 GMT  
		Size: 112.5 MB (112486232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162d8291095c7d95de5978bed455880ca417b35062409ccca428620a0e12e2d0`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e500ef7181b04f57c863f6a874500d2f1963976f66833ddba3238b3c0ca5949`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7528e958b6dbe6f2348a1a2035f2ba4b57f4742156f0d5cd0f2e763150d3c4`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.21`

```console
$ docker pull mysql@sha256:e1bfe11693ed2052cb3b4e5fa356c65381129e87e38551c6cd6ec532ebe0e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.21` - linux; amd64

```console
$ docker pull mysql@sha256:b589f11ab39a852fd13090aeb56314978c73a16d615e28ec148306889b67889f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158633433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d7dc9731daa2c79858307d65ef35f543daf97457b9c11b681f78bb86f7a158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:53:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 10 Sep 2020 06:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Sep 2020 06:53:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Sep 2020 06:53:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Sep 2020 06:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:38 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 10 Sep 2020 06:53:38 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 10 Sep 2020 06:53:39 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Thu, 10 Sep 2020 06:53:39 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 10 Sep 2020 06:53:55 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 10 Sep 2020 06:53:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 10 Sep 2020 06:53:56 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 10 Sep 2020 06:53:56 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 10 Sep 2020 06:53:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 06:53:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Sep 2020 06:53:57 GMT
EXPOSE 3306 33060
# Thu, 10 Sep 2020 06:53:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cebc0b46913f0ab62528142684580ec1e3559f7c3571b2d53eccb656fbf308`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1862755a0b378cf709262d121db21ca934437463f647c7eeb1dd328869df9743`  
		Last Modified: Thu, 10 Sep 2020 06:56:11 GMT  
		Size: 4.2 MB (4178114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489b44f3dbb4c3b4fb955823e880352f6acfe001b1f41c8dcc81fac58622ee29`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.4 MB (1419211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690874f836dbbd1fc19486ed7d1d09084fc88cb8a1a873228ff987700314d91c`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa8be383ffb08bae1621a739dffb09ef152a476bdf23fa43ab902a5a330b7f2`  
		Last Modified: Thu, 10 Sep 2020 06:56:16 GMT  
		Size: 13.4 MB (13447130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55356608b4ac46e974b166adeb8207e78938059004277e38257ae1e0b5e517aa`  
		Last Modified: Thu, 10 Sep 2020 06:56:09 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd35ceccb6ebb923fead362e892aecdf0c78e9bf9871236edd37b939e9aa42b7`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429b35712b19f180a3b54050b0e06f2aba4604a93595a4e84aecbef5ae965756`  
		Last Modified: Thu, 10 Sep 2020 06:56:41 GMT  
		Size: 112.5 MB (112486232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162d8291095c7d95de5978bed455880ca417b35062409ccca428620a0e12e2d0`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e500ef7181b04f57c863f6a874500d2f1963976f66833ddba3238b3c0ca5949`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7528e958b6dbe6f2348a1a2035f2ba4b57f4742156f0d5cd0f2e763150d3c4`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:e1bfe11693ed2052cb3b4e5fa356c65381129e87e38551c6cd6ec532ebe0e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:b589f11ab39a852fd13090aeb56314978c73a16d615e28ec148306889b67889f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158633433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d7dc9731daa2c79858307d65ef35f543daf97457b9c11b681f78bb86f7a158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:53:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 10 Sep 2020 06:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Sep 2020 06:53:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Sep 2020 06:53:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Sep 2020 06:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:53:38 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 10 Sep 2020 06:53:38 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 10 Sep 2020 06:53:39 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Thu, 10 Sep 2020 06:53:39 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Thu, 10 Sep 2020 06:53:55 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 10 Sep 2020 06:53:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 10 Sep 2020 06:53:56 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 10 Sep 2020 06:53:56 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 10 Sep 2020 06:53:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 06:53:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Sep 2020 06:53:57 GMT
EXPOSE 3306 33060
# Thu, 10 Sep 2020 06:53:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cebc0b46913f0ab62528142684580ec1e3559f7c3571b2d53eccb656fbf308`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1862755a0b378cf709262d121db21ca934437463f647c7eeb1dd328869df9743`  
		Last Modified: Thu, 10 Sep 2020 06:56:11 GMT  
		Size: 4.2 MB (4178114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489b44f3dbb4c3b4fb955823e880352f6acfe001b1f41c8dcc81fac58622ee29`  
		Last Modified: Thu, 10 Sep 2020 06:56:10 GMT  
		Size: 1.4 MB (1419211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690874f836dbbd1fc19486ed7d1d09084fc88cb8a1a873228ff987700314d91c`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa8be383ffb08bae1621a739dffb09ef152a476bdf23fa43ab902a5a330b7f2`  
		Last Modified: Thu, 10 Sep 2020 06:56:16 GMT  
		Size: 13.4 MB (13447130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55356608b4ac46e974b166adeb8207e78938059004277e38257ae1e0b5e517aa`  
		Last Modified: Thu, 10 Sep 2020 06:56:09 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd35ceccb6ebb923fead362e892aecdf0c78e9bf9871236edd37b939e9aa42b7`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429b35712b19f180a3b54050b0e06f2aba4604a93595a4e84aecbef5ae965756`  
		Last Modified: Thu, 10 Sep 2020 06:56:41 GMT  
		Size: 112.5 MB (112486232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162d8291095c7d95de5978bed455880ca417b35062409ccca428620a0e12e2d0`  
		Last Modified: Thu, 10 Sep 2020 06:56:08 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e500ef7181b04f57c863f6a874500d2f1963976f66833ddba3238b3c0ca5949`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7528e958b6dbe6f2348a1a2035f2ba4b57f4742156f0d5cd0f2e763150d3c4`  
		Last Modified: Thu, 10 Sep 2020 06:56:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
