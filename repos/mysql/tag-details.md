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
$ docker pull mysql@sha256:8e2004f9fe43df06c3030090f593021a5f283d028b5ed5765cc24236c2c4d88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:ec6742af6625f76f98162b17fd62d22e1824d13fd80f214ab9184c7b6b50bad5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154505674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0658fdbad5fb1c9413c998d8a573eeb5d16713463992005029c591e6400d02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:15:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:01 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:16:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:16:50 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 18 Nov 2020 08:16:50 GMT
ENV MYSQL_VERSION=5.7.32-1debian10
# Sat, 21 Nov 2020 01:22:45 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:23:05 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:23:06 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:23:06 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:23:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:23:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:23:10 GMT
EXPOSE 3306 33060
# Sat, 21 Nov 2020 01:23:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29969ddb0ffb0ed3db2ce1f7fa289fb85495125b9e3469057b10f556ef65b8bb`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f41a44c48e6051d436face965bdfc38392fa9c75959c5cbe93cf50e7151ba`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd802543a34a27d237d3aff4faf5875692d521fe92d3accfee437343755da6`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.4 MB (1419210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79b040de953d321965acb3b6f4564f8332dc90b096fef3fefb5513f3658fcab`  
		Last Modified: Wed, 18 Nov 2020 08:19:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c641199690039d482f076e9279d29bfac6b76331b4cfa974f86af8b14d076`  
		Last Modified: Wed, 18 Nov 2020 08:19:23 GMT  
		Size: 13.4 MB (13447061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7689ec51a0d96ba9a32db995a755b690fa76546c97e8ccc3c17a42968a49b363`  
		Last Modified: Wed, 18 Nov 2020 08:19:16 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bd6224d58feb8d7a53c88cec3fbaa7bb64226db33c55a478596549d478b41a`  
		Last Modified: Sat, 21 Nov 2020 01:24:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab9d3fa4c8c706291c288cc6b350e59a515152341b4c8be3b1bf7303c0b4c4c`  
		Last Modified: Sat, 21 Nov 2020 01:24:56 GMT  
		Size: 108.3 MB (108346091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b741e1c47de1b82b799cb9fe6b810167d8f4de15242bce34026ac4de2da168d`  
		Last Modified: Sat, 21 Nov 2020 01:24:39 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac9d11987ac8bae024896c62b1bda4b029cb2dea86904d346eef21d952aafd2`  
		Last Modified: Sat, 21 Nov 2020 01:24:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:489a24e1c73a4bd3922b16eac848bca9f68c62f9b69c65fd049ceaa2aa556480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:9045727e2a5b8a5428f2f36b17d37da3e284b612205a787d1e37708c1ce937ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102937623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b3da40572bbe0575e0ed7e160fa7e6c886d7e23e937522594116f085f45a04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:29 GMT
ADD file:02294bc9e72a3f3314955f0b5e0e728cd75321e88a1fae9bfbac77c76bfaf05d in / 
# Tue, 17 Nov 2020 20:24:29 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:17:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:17:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:17:50 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:18:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:18:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:18:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:18:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:18:25 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 18 Nov 2020 08:18:25 GMT
ENV MYSQL_VERSION=5.6.50-1debian9
# Sat, 21 Nov 2020 01:23:19 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:23:37 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:23:38 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:23:39 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:23:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:23:40 GMT
EXPOSE 3306
# Sat, 21 Nov 2020 01:23:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4297e02295585beb3f148a5740b644ce87e059455f8d98a5adb7bf95105e011c`  
		Last Modified: Tue, 17 Nov 2020 20:30:42 GMT  
		Size: 22.5 MB (22527663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4202dbafac4ac63b2e6248aa2f1d4337b3d6bd25cd7956d388a46fdcf33d24`  
		Last Modified: Wed, 18 Nov 2020 08:20:35 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaf1f3f851838317d1a75435a3100f7ed932fa4895956b9992c9860173c632b`  
		Last Modified: Wed, 18 Nov 2020 08:20:34 GMT  
		Size: 4.5 MB (4502039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52e4fa803c93e9201b7146447133a9b570780f263a241357937d653403a1a90`  
		Last Modified: Wed, 18 Nov 2020 08:20:33 GMT  
		Size: 1.4 MB (1412141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8912e5072cec20dd745e178d9dd2a0f3fa7470380662d40ce59d8c43a8eedf08`  
		Last Modified: Wed, 18 Nov 2020 08:20:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f1ff5625cc97ec1a27521a556f693199f37876ffc89fb1d2825b6443567c3a`  
		Last Modified: Wed, 18 Nov 2020 08:20:37 GMT  
		Size: 10.2 MB (10224757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824a8567e87bec6f827dc0ce6ed340bd4456ba7d72d8ec91b39e033c767ef2a2`  
		Last Modified: Wed, 18 Nov 2020 08:20:31 GMT  
		Size: 29.0 KB (28956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a38f4d61331d2b259c5fe8967b12a54bb32cbd4e8cf26187aade743f1ce5ce`  
		Last Modified: Sat, 21 Nov 2020 01:25:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba8760c46ecc021a984d6812e0ad5f19430c2a1c7ff5640f54e6a5abd407420`  
		Last Modified: Sat, 21 Nov 2020 01:25:13 GMT  
		Size: 64.2 MB (64234708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7da86861cbd36d56d72ce52871b3a99418672e8511a345692484dea0fb8df4`  
		Last Modified: Sat, 21 Nov 2020 01:25:02 GMT  
		Size: 5.2 KB (5150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e1336d2fe9a718befc18001b0cda0c7f57bcd95326e8f40b8fe59a3cdcf5d2`  
		Last Modified: Sat, 21 Nov 2020 01:25:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.50`

```console
$ docker pull mysql@sha256:489a24e1c73a4bd3922b16eac848bca9f68c62f9b69c65fd049ceaa2aa556480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.50` - linux; amd64

```console
$ docker pull mysql@sha256:9045727e2a5b8a5428f2f36b17d37da3e284b612205a787d1e37708c1ce937ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102937623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b3da40572bbe0575e0ed7e160fa7e6c886d7e23e937522594116f085f45a04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:29 GMT
ADD file:02294bc9e72a3f3314955f0b5e0e728cd75321e88a1fae9bfbac77c76bfaf05d in / 
# Tue, 17 Nov 2020 20:24:29 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:17:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:17:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:17:50 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:18:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:18:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:18:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:18:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:18:25 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 18 Nov 2020 08:18:25 GMT
ENV MYSQL_VERSION=5.6.50-1debian9
# Sat, 21 Nov 2020 01:23:19 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:23:37 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:23:38 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:23:39 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:23:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:23:40 GMT
EXPOSE 3306
# Sat, 21 Nov 2020 01:23:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4297e02295585beb3f148a5740b644ce87e059455f8d98a5adb7bf95105e011c`  
		Last Modified: Tue, 17 Nov 2020 20:30:42 GMT  
		Size: 22.5 MB (22527663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4202dbafac4ac63b2e6248aa2f1d4337b3d6bd25cd7956d388a46fdcf33d24`  
		Last Modified: Wed, 18 Nov 2020 08:20:35 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaf1f3f851838317d1a75435a3100f7ed932fa4895956b9992c9860173c632b`  
		Last Modified: Wed, 18 Nov 2020 08:20:34 GMT  
		Size: 4.5 MB (4502039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52e4fa803c93e9201b7146447133a9b570780f263a241357937d653403a1a90`  
		Last Modified: Wed, 18 Nov 2020 08:20:33 GMT  
		Size: 1.4 MB (1412141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8912e5072cec20dd745e178d9dd2a0f3fa7470380662d40ce59d8c43a8eedf08`  
		Last Modified: Wed, 18 Nov 2020 08:20:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f1ff5625cc97ec1a27521a556f693199f37876ffc89fb1d2825b6443567c3a`  
		Last Modified: Wed, 18 Nov 2020 08:20:37 GMT  
		Size: 10.2 MB (10224757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824a8567e87bec6f827dc0ce6ed340bd4456ba7d72d8ec91b39e033c767ef2a2`  
		Last Modified: Wed, 18 Nov 2020 08:20:31 GMT  
		Size: 29.0 KB (28956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a38f4d61331d2b259c5fe8967b12a54bb32cbd4e8cf26187aade743f1ce5ce`  
		Last Modified: Sat, 21 Nov 2020 01:25:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba8760c46ecc021a984d6812e0ad5f19430c2a1c7ff5640f54e6a5abd407420`  
		Last Modified: Sat, 21 Nov 2020 01:25:13 GMT  
		Size: 64.2 MB (64234708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7da86861cbd36d56d72ce52871b3a99418672e8511a345692484dea0fb8df4`  
		Last Modified: Sat, 21 Nov 2020 01:25:02 GMT  
		Size: 5.2 KB (5150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e1336d2fe9a718befc18001b0cda0c7f57bcd95326e8f40b8fe59a3cdcf5d2`  
		Last Modified: Sat, 21 Nov 2020 01:25:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:8e2004f9fe43df06c3030090f593021a5f283d028b5ed5765cc24236c2c4d88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:ec6742af6625f76f98162b17fd62d22e1824d13fd80f214ab9184c7b6b50bad5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154505674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0658fdbad5fb1c9413c998d8a573eeb5d16713463992005029c591e6400d02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:15:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:01 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:16:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:16:50 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 18 Nov 2020 08:16:50 GMT
ENV MYSQL_VERSION=5.7.32-1debian10
# Sat, 21 Nov 2020 01:22:45 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:23:05 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:23:06 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:23:06 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:23:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:23:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:23:10 GMT
EXPOSE 3306 33060
# Sat, 21 Nov 2020 01:23:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29969ddb0ffb0ed3db2ce1f7fa289fb85495125b9e3469057b10f556ef65b8bb`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f41a44c48e6051d436face965bdfc38392fa9c75959c5cbe93cf50e7151ba`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd802543a34a27d237d3aff4faf5875692d521fe92d3accfee437343755da6`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.4 MB (1419210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79b040de953d321965acb3b6f4564f8332dc90b096fef3fefb5513f3658fcab`  
		Last Modified: Wed, 18 Nov 2020 08:19:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c641199690039d482f076e9279d29bfac6b76331b4cfa974f86af8b14d076`  
		Last Modified: Wed, 18 Nov 2020 08:19:23 GMT  
		Size: 13.4 MB (13447061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7689ec51a0d96ba9a32db995a755b690fa76546c97e8ccc3c17a42968a49b363`  
		Last Modified: Wed, 18 Nov 2020 08:19:16 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bd6224d58feb8d7a53c88cec3fbaa7bb64226db33c55a478596549d478b41a`  
		Last Modified: Sat, 21 Nov 2020 01:24:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab9d3fa4c8c706291c288cc6b350e59a515152341b4c8be3b1bf7303c0b4c4c`  
		Last Modified: Sat, 21 Nov 2020 01:24:56 GMT  
		Size: 108.3 MB (108346091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b741e1c47de1b82b799cb9fe6b810167d8f4de15242bce34026ac4de2da168d`  
		Last Modified: Sat, 21 Nov 2020 01:24:39 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac9d11987ac8bae024896c62b1bda4b029cb2dea86904d346eef21d952aafd2`  
		Last Modified: Sat, 21 Nov 2020 01:24:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.32`

```console
$ docker pull mysql@sha256:8e2004f9fe43df06c3030090f593021a5f283d028b5ed5765cc24236c2c4d88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.32` - linux; amd64

```console
$ docker pull mysql@sha256:ec6742af6625f76f98162b17fd62d22e1824d13fd80f214ab9184c7b6b50bad5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154505674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0658fdbad5fb1c9413c998d8a573eeb5d16713463992005029c591e6400d02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:15:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:01 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:16:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:16:50 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 18 Nov 2020 08:16:50 GMT
ENV MYSQL_VERSION=5.7.32-1debian10
# Sat, 21 Nov 2020 01:22:45 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:23:05 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:23:06 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:23:06 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:23:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:23:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:23:10 GMT
EXPOSE 3306 33060
# Sat, 21 Nov 2020 01:23:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29969ddb0ffb0ed3db2ce1f7fa289fb85495125b9e3469057b10f556ef65b8bb`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f41a44c48e6051d436face965bdfc38392fa9c75959c5cbe93cf50e7151ba`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd802543a34a27d237d3aff4faf5875692d521fe92d3accfee437343755da6`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.4 MB (1419210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79b040de953d321965acb3b6f4564f8332dc90b096fef3fefb5513f3658fcab`  
		Last Modified: Wed, 18 Nov 2020 08:19:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c641199690039d482f076e9279d29bfac6b76331b4cfa974f86af8b14d076`  
		Last Modified: Wed, 18 Nov 2020 08:19:23 GMT  
		Size: 13.4 MB (13447061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7689ec51a0d96ba9a32db995a755b690fa76546c97e8ccc3c17a42968a49b363`  
		Last Modified: Wed, 18 Nov 2020 08:19:16 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bd6224d58feb8d7a53c88cec3fbaa7bb64226db33c55a478596549d478b41a`  
		Last Modified: Sat, 21 Nov 2020 01:24:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab9d3fa4c8c706291c288cc6b350e59a515152341b4c8be3b1bf7303c0b4c4c`  
		Last Modified: Sat, 21 Nov 2020 01:24:56 GMT  
		Size: 108.3 MB (108346091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b741e1c47de1b82b799cb9fe6b810167d8f4de15242bce34026ac4de2da168d`  
		Last Modified: Sat, 21 Nov 2020 01:24:39 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac9d11987ac8bae024896c62b1bda4b029cb2dea86904d346eef21d952aafd2`  
		Last Modified: Sat, 21 Nov 2020 01:24:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:4bb2e81a40e9d0d59bd8e3dc2ba5e1f2197696f6de39a91e90798dd27299b093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:c8414a9528a0fff5dd44d7c9260e570258dc09c2548766400cd5cfc4dd384991
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158960115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7265748b5dc3211208fb9aa232cef8d3fefd5d9a2a80d87407b8ea649e571c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:15:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:01 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:16:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Sat, 21 Nov 2020 01:22:20 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:22:35 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:22:36 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:22:36 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 21 Nov 2020 01:22:36 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:22:38 GMT
EXPOSE 3306 33060
# Sat, 21 Nov 2020 01:22:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29969ddb0ffb0ed3db2ce1f7fa289fb85495125b9e3469057b10f556ef65b8bb`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f41a44c48e6051d436face965bdfc38392fa9c75959c5cbe93cf50e7151ba`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd802543a34a27d237d3aff4faf5875692d521fe92d3accfee437343755da6`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.4 MB (1419210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79b040de953d321965acb3b6f4564f8332dc90b096fef3fefb5513f3658fcab`  
		Last Modified: Wed, 18 Nov 2020 08:19:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c641199690039d482f076e9279d29bfac6b76331b4cfa974f86af8b14d076`  
		Last Modified: Wed, 18 Nov 2020 08:19:23 GMT  
		Size: 13.4 MB (13447061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7689ec51a0d96ba9a32db995a755b690fa76546c97e8ccc3c17a42968a49b363`  
		Last Modified: Wed, 18 Nov 2020 08:19:16 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a880ba7c411fa76cff7c85338d6ec8a2595ba8b9eab771a826011e9a8a517b58`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984f656ec6cade78263fa8887ad717d89ac8479de3826249ea8b679bcdcd5ca3`  
		Last Modified: Sat, 21 Nov 2020 01:24:32 GMT  
		Size: 112.8 MB (112799692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f497bce458aeb6b738fe4d5763b444231390efa450c28361a91fe8c337c5b89`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f97694b93ca77fab22010d3d964c1909cedeab8750a60942c2a5c38f4a1`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f069358dc963e6a16b7891e1002c991fe4f9653997ef005f1b570dac4921d9a`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:4bb2e81a40e9d0d59bd8e3dc2ba5e1f2197696f6de39a91e90798dd27299b093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:c8414a9528a0fff5dd44d7c9260e570258dc09c2548766400cd5cfc4dd384991
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158960115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7265748b5dc3211208fb9aa232cef8d3fefd5d9a2a80d87407b8ea649e571c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:15:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:01 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:16:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Sat, 21 Nov 2020 01:22:20 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:22:35 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:22:36 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:22:36 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 21 Nov 2020 01:22:36 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:22:38 GMT
EXPOSE 3306 33060
# Sat, 21 Nov 2020 01:22:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29969ddb0ffb0ed3db2ce1f7fa289fb85495125b9e3469057b10f556ef65b8bb`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f41a44c48e6051d436face965bdfc38392fa9c75959c5cbe93cf50e7151ba`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd802543a34a27d237d3aff4faf5875692d521fe92d3accfee437343755da6`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.4 MB (1419210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79b040de953d321965acb3b6f4564f8332dc90b096fef3fefb5513f3658fcab`  
		Last Modified: Wed, 18 Nov 2020 08:19:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c641199690039d482f076e9279d29bfac6b76331b4cfa974f86af8b14d076`  
		Last Modified: Wed, 18 Nov 2020 08:19:23 GMT  
		Size: 13.4 MB (13447061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7689ec51a0d96ba9a32db995a755b690fa76546c97e8ccc3c17a42968a49b363`  
		Last Modified: Wed, 18 Nov 2020 08:19:16 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a880ba7c411fa76cff7c85338d6ec8a2595ba8b9eab771a826011e9a8a517b58`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984f656ec6cade78263fa8887ad717d89ac8479de3826249ea8b679bcdcd5ca3`  
		Last Modified: Sat, 21 Nov 2020 01:24:32 GMT  
		Size: 112.8 MB (112799692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f497bce458aeb6b738fe4d5763b444231390efa450c28361a91fe8c337c5b89`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f97694b93ca77fab22010d3d964c1909cedeab8750a60942c2a5c38f4a1`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f069358dc963e6a16b7891e1002c991fe4f9653997ef005f1b570dac4921d9a`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.22`

```console
$ docker pull mysql@sha256:4bb2e81a40e9d0d59bd8e3dc2ba5e1f2197696f6de39a91e90798dd27299b093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.22` - linux; amd64

```console
$ docker pull mysql@sha256:c8414a9528a0fff5dd44d7c9260e570258dc09c2548766400cd5cfc4dd384991
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158960115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7265748b5dc3211208fb9aa232cef8d3fefd5d9a2a80d87407b8ea649e571c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:15:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:01 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:16:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Sat, 21 Nov 2020 01:22:20 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:22:35 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:22:36 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:22:36 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 21 Nov 2020 01:22:36 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:22:38 GMT
EXPOSE 3306 33060
# Sat, 21 Nov 2020 01:22:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29969ddb0ffb0ed3db2ce1f7fa289fb85495125b9e3469057b10f556ef65b8bb`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f41a44c48e6051d436face965bdfc38392fa9c75959c5cbe93cf50e7151ba`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd802543a34a27d237d3aff4faf5875692d521fe92d3accfee437343755da6`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.4 MB (1419210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79b040de953d321965acb3b6f4564f8332dc90b096fef3fefb5513f3658fcab`  
		Last Modified: Wed, 18 Nov 2020 08:19:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c641199690039d482f076e9279d29bfac6b76331b4cfa974f86af8b14d076`  
		Last Modified: Wed, 18 Nov 2020 08:19:23 GMT  
		Size: 13.4 MB (13447061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7689ec51a0d96ba9a32db995a755b690fa76546c97e8ccc3c17a42968a49b363`  
		Last Modified: Wed, 18 Nov 2020 08:19:16 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a880ba7c411fa76cff7c85338d6ec8a2595ba8b9eab771a826011e9a8a517b58`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984f656ec6cade78263fa8887ad717d89ac8479de3826249ea8b679bcdcd5ca3`  
		Last Modified: Sat, 21 Nov 2020 01:24:32 GMT  
		Size: 112.8 MB (112799692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f497bce458aeb6b738fe4d5763b444231390efa450c28361a91fe8c337c5b89`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f97694b93ca77fab22010d3d964c1909cedeab8750a60942c2a5c38f4a1`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f069358dc963e6a16b7891e1002c991fe4f9653997ef005f1b570dac4921d9a`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:4bb2e81a40e9d0d59bd8e3dc2ba5e1f2197696f6de39a91e90798dd27299b093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:c8414a9528a0fff5dd44d7c9260e570258dc09c2548766400cd5cfc4dd384991
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158960115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7265748b5dc3211208fb9aa232cef8d3fefd5d9a2a80d87407b8ea649e571c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:15:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:01 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:16:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Sat, 21 Nov 2020 01:22:20 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:22:35 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:22:36 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:22:36 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 21 Nov 2020 01:22:36 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:22:38 GMT
EXPOSE 3306 33060
# Sat, 21 Nov 2020 01:22:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29969ddb0ffb0ed3db2ce1f7fa289fb85495125b9e3469057b10f556ef65b8bb`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f41a44c48e6051d436face965bdfc38392fa9c75959c5cbe93cf50e7151ba`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd802543a34a27d237d3aff4faf5875692d521fe92d3accfee437343755da6`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.4 MB (1419210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79b040de953d321965acb3b6f4564f8332dc90b096fef3fefb5513f3658fcab`  
		Last Modified: Wed, 18 Nov 2020 08:19:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c641199690039d482f076e9279d29bfac6b76331b4cfa974f86af8b14d076`  
		Last Modified: Wed, 18 Nov 2020 08:19:23 GMT  
		Size: 13.4 MB (13447061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7689ec51a0d96ba9a32db995a755b690fa76546c97e8ccc3c17a42968a49b363`  
		Last Modified: Wed, 18 Nov 2020 08:19:16 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a880ba7c411fa76cff7c85338d6ec8a2595ba8b9eab771a826011e9a8a517b58`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984f656ec6cade78263fa8887ad717d89ac8479de3826249ea8b679bcdcd5ca3`  
		Last Modified: Sat, 21 Nov 2020 01:24:32 GMT  
		Size: 112.8 MB (112799692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f497bce458aeb6b738fe4d5763b444231390efa450c28361a91fe8c337c5b89`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f97694b93ca77fab22010d3d964c1909cedeab8750a60942c2a5c38f4a1`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f069358dc963e6a16b7891e1002c991fe4f9653997ef005f1b570dac4921d9a`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
