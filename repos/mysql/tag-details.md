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
$ docker pull mysql@sha256:97869b42772dac5b767f4e4692434fbd5e6b86bcb8695d4feafb52b59fe9ae24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:a175aaebe819a4f0beb626ae99ff771ab885a44f2ba9c104a58ff6665d73e33f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154476840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8679ced16d206961b35686895b06cfafefde87ef02b518dfc2133081ebf47cda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:14:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:14:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:14:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:15:26 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 22 Jul 2020 20:15:26 GMT
ENV MYSQL_VERSION=5.7.31-1debian10
# Wed, 22 Jul 2020 20:15:27 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:15:57 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 22 Jul 2020 20:15:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:15:58 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:15:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:16:00 GMT
EXPOSE 3306 33060
# Wed, 22 Jul 2020 20:16:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e5de89054c0184901d7b361aa53939eb417f6b02b94490952e7493af5b856`  
		Last Modified: Wed, 22 Jul 2020 20:17:34 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ccb86eb40398cc3c7f679c1b60a0587089c03c940e03fdeb1b8b3415f8441`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ee78841235274ca62885510d6aebeee2cb8e28df2fe98e9b08972b8c4ad005`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 1.4 MB (1419246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd86ccee5651597918eceb86d6ddffab7218f346d3de86b7f2278cff761c04`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bea0594a440e1fdbb7284c54cbf62a79c066e430b8c52ec7d1c97c81427de8`  
		Last Modified: Wed, 22 Jul 2020 20:17:39 GMT  
		Size: 13.4 MB (13443184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f529ae895c9062642dd43724d2e001dfd8fc5401e852e407da7b314e71cf`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54a8bcf566c30e1f08915d5f0bc2068a5c8d6c37dfaa5f4b125a07c6bebb3f`  
		Last Modified: Wed, 22 Jul 2020 20:18:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c21ba6527b8c367dc78b227d96f0112c6a6bdcc8169077e3fd0abf5b1089da`  
		Last Modified: Wed, 22 Jul 2020 20:18:34 GMT  
		Size: 108.3 MB (108328029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e74bb27b39c5dd922b0894107551517c837da54518ae0a90792f4ce8dccd5a`  
		Last Modified: Wed, 22 Jul 2020 20:18:11 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f13eadfe747bf44d817e5cea0096bb3be6893e827facf7c2fd0ab5d04b143fd`  
		Last Modified: Wed, 22 Jul 2020 20:18:10 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:213f489cb42497635fa98189734837a0c210e01c473c78c2ad77a81acac3ac22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:055ccf66464b1bea6226601f3ce836a188d9e7cff836e7702380c50edf071631
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102923274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a599e29874aa0b52e0349f928e78ed835e46da4dede9a435bf19a2c2c6fdb0df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:16:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:16:15 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:16:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:16:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:16:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:16:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:16:47 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 22 Jul 2020 20:16:47 GMT
ENV MYSQL_VERSION=5.6.49-1debian9
# Wed, 22 Jul 2020 20:16:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:17:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 22 Jul 2020 20:17:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:17:12 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:17:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:17:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:17:14 GMT
EXPOSE 3306
# Wed, 22 Jul 2020 20:17:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70349e9e9a81f2700f5f64e349eff174ac8506f2fe61f686576203bc5f7459e6`  
		Last Modified: Wed, 22 Jul 2020 20:18:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a33a99d92de1f28dd48bbe01f3d8ffa2eeab1b49da0c4bf5c83690d097db2`  
		Last Modified: Wed, 22 Jul 2020 20:18:43 GMT  
		Size: 4.5 MB (4501998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd80d3b52aa8bb2066b125ff3e00f0de5186c69a01c13293bacaf4f38d4a406`  
		Last Modified: Wed, 22 Jul 2020 20:18:42 GMT  
		Size: 1.4 MB (1412086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05148f09775a807c7d97e939b61a1646fd4b2e08ee2335c73b63f0d051f73e2b`  
		Last Modified: Wed, 22 Jul 2020 20:18:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7540e79efb137cd984b8f43b9a417c0f9ad8d40771ac73664ef299caf97fb696`  
		Last Modified: Wed, 22 Jul 2020 20:18:46 GMT  
		Size: 10.2 MB (10224888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a189f9d0a19096badde4664f29f8991a535c098c9636dbb65e7ac32f2434a220`  
		Last Modified: Wed, 22 Jul 2020 20:18:40 GMT  
		Size: 28.3 KB (28326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4444b3d7ee9ec309b8cca76a30d2057a262ee70549737b38657cb5c84046ed9c`  
		Last Modified: Wed, 22 Jul 2020 20:18:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8560fc9c5ba854bb49cc5ceb7c8fe30ef27f983cf7b264f35316d0168dff70f`  
		Last Modified: Wed, 22 Jul 2020 20:18:58 GMT  
		Size: 64.2 MB (64232978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7986c73e30e639a62bee19dc601b5b8a80b92e31ef385e908c20563dcf43ed`  
		Last Modified: Wed, 22 Jul 2020 20:18:40 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a2ddaf5fa9c371d178b5af909b943bba07d26b0657450d2dbc482ebf5b5fa`  
		Last Modified: Wed, 22 Jul 2020 20:18:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.49`

```console
$ docker pull mysql@sha256:213f489cb42497635fa98189734837a0c210e01c473c78c2ad77a81acac3ac22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.49` - linux; amd64

```console
$ docker pull mysql@sha256:055ccf66464b1bea6226601f3ce836a188d9e7cff836e7702380c50edf071631
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102923274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a599e29874aa0b52e0349f928e78ed835e46da4dede9a435bf19a2c2c6fdb0df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:16:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:16:15 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:16:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:16:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:16:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:16:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:16:47 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 22 Jul 2020 20:16:47 GMT
ENV MYSQL_VERSION=5.6.49-1debian9
# Wed, 22 Jul 2020 20:16:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:17:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 22 Jul 2020 20:17:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:17:12 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:17:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:17:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:17:14 GMT
EXPOSE 3306
# Wed, 22 Jul 2020 20:17:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70349e9e9a81f2700f5f64e349eff174ac8506f2fe61f686576203bc5f7459e6`  
		Last Modified: Wed, 22 Jul 2020 20:18:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a33a99d92de1f28dd48bbe01f3d8ffa2eeab1b49da0c4bf5c83690d097db2`  
		Last Modified: Wed, 22 Jul 2020 20:18:43 GMT  
		Size: 4.5 MB (4501998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd80d3b52aa8bb2066b125ff3e00f0de5186c69a01c13293bacaf4f38d4a406`  
		Last Modified: Wed, 22 Jul 2020 20:18:42 GMT  
		Size: 1.4 MB (1412086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05148f09775a807c7d97e939b61a1646fd4b2e08ee2335c73b63f0d051f73e2b`  
		Last Modified: Wed, 22 Jul 2020 20:18:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7540e79efb137cd984b8f43b9a417c0f9ad8d40771ac73664ef299caf97fb696`  
		Last Modified: Wed, 22 Jul 2020 20:18:46 GMT  
		Size: 10.2 MB (10224888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a189f9d0a19096badde4664f29f8991a535c098c9636dbb65e7ac32f2434a220`  
		Last Modified: Wed, 22 Jul 2020 20:18:40 GMT  
		Size: 28.3 KB (28326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4444b3d7ee9ec309b8cca76a30d2057a262ee70549737b38657cb5c84046ed9c`  
		Last Modified: Wed, 22 Jul 2020 20:18:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8560fc9c5ba854bb49cc5ceb7c8fe30ef27f983cf7b264f35316d0168dff70f`  
		Last Modified: Wed, 22 Jul 2020 20:18:58 GMT  
		Size: 64.2 MB (64232978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7986c73e30e639a62bee19dc601b5b8a80b92e31ef385e908c20563dcf43ed`  
		Last Modified: Wed, 22 Jul 2020 20:18:40 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a2ddaf5fa9c371d178b5af909b943bba07d26b0657450d2dbc482ebf5b5fa`  
		Last Modified: Wed, 22 Jul 2020 20:18:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:97869b42772dac5b767f4e4692434fbd5e6b86bcb8695d4feafb52b59fe9ae24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:a175aaebe819a4f0beb626ae99ff771ab885a44f2ba9c104a58ff6665d73e33f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154476840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8679ced16d206961b35686895b06cfafefde87ef02b518dfc2133081ebf47cda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:14:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:14:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:14:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:15:26 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 22 Jul 2020 20:15:26 GMT
ENV MYSQL_VERSION=5.7.31-1debian10
# Wed, 22 Jul 2020 20:15:27 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:15:57 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 22 Jul 2020 20:15:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:15:58 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:15:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:16:00 GMT
EXPOSE 3306 33060
# Wed, 22 Jul 2020 20:16:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e5de89054c0184901d7b361aa53939eb417f6b02b94490952e7493af5b856`  
		Last Modified: Wed, 22 Jul 2020 20:17:34 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ccb86eb40398cc3c7f679c1b60a0587089c03c940e03fdeb1b8b3415f8441`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ee78841235274ca62885510d6aebeee2cb8e28df2fe98e9b08972b8c4ad005`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 1.4 MB (1419246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd86ccee5651597918eceb86d6ddffab7218f346d3de86b7f2278cff761c04`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bea0594a440e1fdbb7284c54cbf62a79c066e430b8c52ec7d1c97c81427de8`  
		Last Modified: Wed, 22 Jul 2020 20:17:39 GMT  
		Size: 13.4 MB (13443184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f529ae895c9062642dd43724d2e001dfd8fc5401e852e407da7b314e71cf`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54a8bcf566c30e1f08915d5f0bc2068a5c8d6c37dfaa5f4b125a07c6bebb3f`  
		Last Modified: Wed, 22 Jul 2020 20:18:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c21ba6527b8c367dc78b227d96f0112c6a6bdcc8169077e3fd0abf5b1089da`  
		Last Modified: Wed, 22 Jul 2020 20:18:34 GMT  
		Size: 108.3 MB (108328029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e74bb27b39c5dd922b0894107551517c837da54518ae0a90792f4ce8dccd5a`  
		Last Modified: Wed, 22 Jul 2020 20:18:11 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f13eadfe747bf44d817e5cea0096bb3be6893e827facf7c2fd0ab5d04b143fd`  
		Last Modified: Wed, 22 Jul 2020 20:18:10 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.31`

```console
$ docker pull mysql@sha256:97869b42772dac5b767f4e4692434fbd5e6b86bcb8695d4feafb52b59fe9ae24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.31` - linux; amd64

```console
$ docker pull mysql@sha256:a175aaebe819a4f0beb626ae99ff771ab885a44f2ba9c104a58ff6665d73e33f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154476840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8679ced16d206961b35686895b06cfafefde87ef02b518dfc2133081ebf47cda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:14:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:14:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:14:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:15:26 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 22 Jul 2020 20:15:26 GMT
ENV MYSQL_VERSION=5.7.31-1debian10
# Wed, 22 Jul 2020 20:15:27 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:15:57 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 22 Jul 2020 20:15:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:15:58 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:15:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:16:00 GMT
EXPOSE 3306 33060
# Wed, 22 Jul 2020 20:16:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e5de89054c0184901d7b361aa53939eb417f6b02b94490952e7493af5b856`  
		Last Modified: Wed, 22 Jul 2020 20:17:34 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ccb86eb40398cc3c7f679c1b60a0587089c03c940e03fdeb1b8b3415f8441`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ee78841235274ca62885510d6aebeee2cb8e28df2fe98e9b08972b8c4ad005`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 1.4 MB (1419246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd86ccee5651597918eceb86d6ddffab7218f346d3de86b7f2278cff761c04`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bea0594a440e1fdbb7284c54cbf62a79c066e430b8c52ec7d1c97c81427de8`  
		Last Modified: Wed, 22 Jul 2020 20:17:39 GMT  
		Size: 13.4 MB (13443184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f529ae895c9062642dd43724d2e001dfd8fc5401e852e407da7b314e71cf`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54a8bcf566c30e1f08915d5f0bc2068a5c8d6c37dfaa5f4b125a07c6bebb3f`  
		Last Modified: Wed, 22 Jul 2020 20:18:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c21ba6527b8c367dc78b227d96f0112c6a6bdcc8169077e3fd0abf5b1089da`  
		Last Modified: Wed, 22 Jul 2020 20:18:34 GMT  
		Size: 108.3 MB (108328029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e74bb27b39c5dd922b0894107551517c837da54518ae0a90792f4ce8dccd5a`  
		Last Modified: Wed, 22 Jul 2020 20:18:11 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f13eadfe747bf44d817e5cea0096bb3be6893e827facf7c2fd0ab5d04b143fd`  
		Last Modified: Wed, 22 Jul 2020 20:18:10 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:fb6a6a26111ba75f9e8487db639bc5721d4431beba4cd668a4e922b8f8b14acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:f1f10a8a6014bda907889c2f649d7b832398432b6eb4849331818f01533db293
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158635718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fcc9e1cc046c92cfcea0d66cdb00fcb7747e87dde96dfc958bd80be37af117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:14:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:14:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:14:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Wed, 22 Jul 2020 20:14:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 22 Jul 2020 20:15:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:15:14 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 22 Jul 2020 20:15:14 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:15:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:15:16 GMT
EXPOSE 3306 33060
# Wed, 22 Jul 2020 20:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e5de89054c0184901d7b361aa53939eb417f6b02b94490952e7493af5b856`  
		Last Modified: Wed, 22 Jul 2020 20:17:34 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ccb86eb40398cc3c7f679c1b60a0587089c03c940e03fdeb1b8b3415f8441`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ee78841235274ca62885510d6aebeee2cb8e28df2fe98e9b08972b8c4ad005`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 1.4 MB (1419246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd86ccee5651597918eceb86d6ddffab7218f346d3de86b7f2278cff761c04`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bea0594a440e1fdbb7284c54cbf62a79c066e430b8c52ec7d1c97c81427de8`  
		Last Modified: Wed, 22 Jul 2020 20:17:39 GMT  
		Size: 13.4 MB (13443184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f529ae895c9062642dd43724d2e001dfd8fc5401e852e407da7b314e71cf`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0fc09f046d2387586aaef133cd264733e33597645aa48407b88f090e01e3cb`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccd5b05a8f634497cebc0350e74799d0ca0e046361bb280bcf787ac382fd01e`  
		Last Modified: Wed, 22 Jul 2020 20:18:04 GMT  
		Size: 112.5 MB (112486062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d29d8de5d4bfcd07f7157f4f3b47c3c7400e250fd09c7c43064533c0f2a88f`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8077a91f5d16cf6c6a03a1a5e7ae43d1c5b8d059374b2ca2ec2e447d08a04959`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922753e827ecc1cb20cbd2d608d772223378eac55724852d23d3d1473da185a4`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:fb6a6a26111ba75f9e8487db639bc5721d4431beba4cd668a4e922b8f8b14acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:f1f10a8a6014bda907889c2f649d7b832398432b6eb4849331818f01533db293
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158635718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fcc9e1cc046c92cfcea0d66cdb00fcb7747e87dde96dfc958bd80be37af117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:14:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:14:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:14:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Wed, 22 Jul 2020 20:14:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 22 Jul 2020 20:15:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:15:14 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 22 Jul 2020 20:15:14 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:15:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:15:16 GMT
EXPOSE 3306 33060
# Wed, 22 Jul 2020 20:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e5de89054c0184901d7b361aa53939eb417f6b02b94490952e7493af5b856`  
		Last Modified: Wed, 22 Jul 2020 20:17:34 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ccb86eb40398cc3c7f679c1b60a0587089c03c940e03fdeb1b8b3415f8441`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ee78841235274ca62885510d6aebeee2cb8e28df2fe98e9b08972b8c4ad005`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 1.4 MB (1419246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd86ccee5651597918eceb86d6ddffab7218f346d3de86b7f2278cff761c04`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bea0594a440e1fdbb7284c54cbf62a79c066e430b8c52ec7d1c97c81427de8`  
		Last Modified: Wed, 22 Jul 2020 20:17:39 GMT  
		Size: 13.4 MB (13443184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f529ae895c9062642dd43724d2e001dfd8fc5401e852e407da7b314e71cf`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0fc09f046d2387586aaef133cd264733e33597645aa48407b88f090e01e3cb`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccd5b05a8f634497cebc0350e74799d0ca0e046361bb280bcf787ac382fd01e`  
		Last Modified: Wed, 22 Jul 2020 20:18:04 GMT  
		Size: 112.5 MB (112486062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d29d8de5d4bfcd07f7157f4f3b47c3c7400e250fd09c7c43064533c0f2a88f`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8077a91f5d16cf6c6a03a1a5e7ae43d1c5b8d059374b2ca2ec2e447d08a04959`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922753e827ecc1cb20cbd2d608d772223378eac55724852d23d3d1473da185a4`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.21`

```console
$ docker pull mysql@sha256:fb6a6a26111ba75f9e8487db639bc5721d4431beba4cd668a4e922b8f8b14acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.21` - linux; amd64

```console
$ docker pull mysql@sha256:f1f10a8a6014bda907889c2f649d7b832398432b6eb4849331818f01533db293
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158635718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fcc9e1cc046c92cfcea0d66cdb00fcb7747e87dde96dfc958bd80be37af117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:14:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:14:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:14:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Wed, 22 Jul 2020 20:14:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 22 Jul 2020 20:15:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:15:14 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 22 Jul 2020 20:15:14 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:15:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:15:16 GMT
EXPOSE 3306 33060
# Wed, 22 Jul 2020 20:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e5de89054c0184901d7b361aa53939eb417f6b02b94490952e7493af5b856`  
		Last Modified: Wed, 22 Jul 2020 20:17:34 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ccb86eb40398cc3c7f679c1b60a0587089c03c940e03fdeb1b8b3415f8441`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ee78841235274ca62885510d6aebeee2cb8e28df2fe98e9b08972b8c4ad005`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 1.4 MB (1419246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd86ccee5651597918eceb86d6ddffab7218f346d3de86b7f2278cff761c04`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bea0594a440e1fdbb7284c54cbf62a79c066e430b8c52ec7d1c97c81427de8`  
		Last Modified: Wed, 22 Jul 2020 20:17:39 GMT  
		Size: 13.4 MB (13443184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f529ae895c9062642dd43724d2e001dfd8fc5401e852e407da7b314e71cf`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0fc09f046d2387586aaef133cd264733e33597645aa48407b88f090e01e3cb`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccd5b05a8f634497cebc0350e74799d0ca0e046361bb280bcf787ac382fd01e`  
		Last Modified: Wed, 22 Jul 2020 20:18:04 GMT  
		Size: 112.5 MB (112486062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d29d8de5d4bfcd07f7157f4f3b47c3c7400e250fd09c7c43064533c0f2a88f`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8077a91f5d16cf6c6a03a1a5e7ae43d1c5b8d059374b2ca2ec2e447d08a04959`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922753e827ecc1cb20cbd2d608d772223378eac55724852d23d3d1473da185a4`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:fb6a6a26111ba75f9e8487db639bc5721d4431beba4cd668a4e922b8f8b14acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:f1f10a8a6014bda907889c2f649d7b832398432b6eb4849331818f01533db293
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158635718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fcc9e1cc046c92cfcea0d66cdb00fcb7747e87dde96dfc958bd80be37af117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:14:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:14:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:14:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Wed, 22 Jul 2020 20:14:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 22 Jul 2020 20:15:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:15:14 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 22 Jul 2020 20:15:14 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:15:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:15:16 GMT
EXPOSE 3306 33060
# Wed, 22 Jul 2020 20:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e5de89054c0184901d7b361aa53939eb417f6b02b94490952e7493af5b856`  
		Last Modified: Wed, 22 Jul 2020 20:17:34 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ccb86eb40398cc3c7f679c1b60a0587089c03c940e03fdeb1b8b3415f8441`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ee78841235274ca62885510d6aebeee2cb8e28df2fe98e9b08972b8c4ad005`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 1.4 MB (1419246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd86ccee5651597918eceb86d6ddffab7218f346d3de86b7f2278cff761c04`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bea0594a440e1fdbb7284c54cbf62a79c066e430b8c52ec7d1c97c81427de8`  
		Last Modified: Wed, 22 Jul 2020 20:17:39 GMT  
		Size: 13.4 MB (13443184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f529ae895c9062642dd43724d2e001dfd8fc5401e852e407da7b314e71cf`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0fc09f046d2387586aaef133cd264733e33597645aa48407b88f090e01e3cb`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccd5b05a8f634497cebc0350e74799d0ca0e046361bb280bcf787ac382fd01e`  
		Last Modified: Wed, 22 Jul 2020 20:18:04 GMT  
		Size: 112.5 MB (112486062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d29d8de5d4bfcd07f7157f4f3b47c3c7400e250fd09c7c43064533c0f2a88f`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8077a91f5d16cf6c6a03a1a5e7ae43d1c5b8d059374b2ca2ec2e447d08a04959`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922753e827ecc1cb20cbd2d608d772223378eac55724852d23d3d1473da185a4`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
