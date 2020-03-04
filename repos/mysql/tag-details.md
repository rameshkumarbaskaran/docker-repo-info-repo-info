<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.47`](#mysql5647)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.29`](#mysql5729)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.19`](#mysql8019)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:f4a5f5be3d94b4f4d3aef00fbc276ce7c08e62f2e1f28867d930deb73a314c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:b475cf2d99b3209c9fafe7841b6f05cfd862c67ee5b06ff66506216409370b74
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158203061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84164b03fa2ecb33e8b4c1f2636ec3286e90786819faa4d1c103ae147824196a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 04 Mar 2020 17:28:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 04 Mar 2020 17:28:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:28:48 GMT
ENV GOSU_VERSION=1.7
# Wed, 04 Mar 2020 17:28:57 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 04 Mar 2020 17:28:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 04 Mar 2020 17:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:29:05 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 04 Mar 2020 17:29:35 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 04 Mar 2020 17:29:35 GMT
ENV MYSQL_VERSION=5.7.29-1debian10
# Wed, 04 Mar 2020 17:29:36 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 04 Mar 2020 17:30:01 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 04 Mar 2020 17:30:02 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Mar 2020 17:30:02 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:30:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 04 Mar 2020 17:30:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:30:03 GMT
EXPOSE 3306 33060
# Wed, 04 Mar 2020 17:30:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9748e016a5c09d5e1669038c1924dd722b08bebe43298490438fd61eaeaa022`  
		Last Modified: Wed, 04 Mar 2020 17:30:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da54b038fed135fc80d01cc2c1ef143ca69bb418e44261a4f6a62d96cf20a19b`  
		Last Modified: Wed, 04 Mar 2020 17:30:21 GMT  
		Size: 4.2 MB (4178026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6895ec5eb2c0de57232791bdc715eef9753a0ebf379644c4c9d237e77f079509`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 1.3 MB (1277296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ba0647b87721c5700e04da65c5adde40fe7791e8374fd8813e3639636562d`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dce60f2f1a8bab438c8286497a8a11b02965c936f62c5ae2fd5a20f7299284`  
		Last Modified: Wed, 04 Mar 2020 17:30:22 GMT  
		Size: 13.4 MB (13443138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702ec598d0af1ab669d4221882b740a42e5bd99ea5451e7340f32cf0aaf80039`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cca87a5d4dd913a08564698c04fbaaea7c33b9a4e71259976abfe58d0b1fd5`  
		Last Modified: Wed, 04 Mar 2020 17:30:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec05b7b1c5c7542319640df43b9682d58938dbcabecce9c4f8ceea56f0d92c44`  
		Last Modified: Wed, 04 Mar 2020 17:31:10 GMT  
		Size: 112.2 MB (112203117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b1d9f49b053f0713da67fb456618bfa2d682f0236cef99c33fe8099987f0d`  
		Last Modified: Wed, 04 Mar 2020 17:30:53 GMT  
		Size: 5.1 KB (5074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded6a30c87c47884b78ce1cd9dc511a890affc9a503bd234f536192e9aa87ca`  
		Last Modified: Wed, 04 Mar 2020 17:30:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:a72a05bcf3914c902070765a506b1c8c17c06400258e7b574965763099dee9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:8d4c4f7d3a9c2e650757a27bb74c83c4996739e989f2c8bf7f7678faa8c7d772
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102733524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8078e8ab06d8dabd6c30cffb03951fa035d85f75c19a83ace29b01cb3ecd272`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 14:19:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Feb 2020 14:19:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:19:30 GMT
ENV GOSU_VERSION=1.7
# Wed, 26 Feb 2020 14:19:42 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 26 Feb 2020 14:19:43 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Feb 2020 14:21:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:21:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 26 Feb 2020 14:21:24 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 26 Feb 2020 14:21:24 GMT
ENV MYSQL_VERSION=5.6.47-1debian9
# Wed, 26 Feb 2020 14:21:25 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 26 Feb 2020 14:21:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 26 Feb 2020 14:21:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Mar 2020 17:30:08 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:30:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 04 Mar 2020 17:30:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:30:09 GMT
EXPOSE 3306
# Wed, 04 Mar 2020 17:30:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda15103a86a472aecface46a21e4687bf799a7a7562172cefd94f4d64ba14eb`  
		Last Modified: Wed, 26 Feb 2020 14:22:05 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55971d75ab8c7112e84a48e647c8bc9941a32bcb23549a0a9b49ad27f4911c95`  
		Last Modified: Wed, 26 Feb 2020 14:22:06 GMT  
		Size: 4.5 MB (4501215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d4ea32020b3db53b4f86b22403895ca3bf327ec1d83de316d59e284fa5409e`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 1.3 MB (1270374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61420072af9194292e8c4b7a8b10f2c1cb474df6a64971ba6575f11eb03c748f`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30862a48418b4f2cc5b8a8d295a13f55d5f73c0a3d761607288fc12848bc733f`  
		Last Modified: Wed, 26 Feb 2020 14:22:59 GMT  
		Size: 10.2 MB (10222848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c2ee3a9a570a80487ed96d3f4ddb051e644a66b75ae356750476aec9e05473`  
		Last Modified: Wed, 26 Feb 2020 14:22:55 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4efadb31dfa55f888104c07bfa6a3ead9db357bfdbe928eaf442f70028bd5a`  
		Last Modified: Wed, 26 Feb 2020 14:22:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd931017b211104e6782056838a12014c435d3a1e2afa406dfba314792703d4e`  
		Last Modified: Wed, 26 Feb 2020 14:23:08 GMT  
		Size: 64.2 MB (64190112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488a8608307942b4c58f2ff11fa239c42c0a779447fc3c4fd1890993e42755a1`  
		Last Modified: Wed, 04 Mar 2020 17:31:15 GMT  
		Size: 5.1 KB (5085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921d4bdabca263cab06d154630307cd947de5983eb169e8023794373dac1d6c6`  
		Last Modified: Wed, 04 Mar 2020 17:31:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.47`

```console
$ docker pull mysql@sha256:a72a05bcf3914c902070765a506b1c8c17c06400258e7b574965763099dee9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.47` - linux; amd64

```console
$ docker pull mysql@sha256:8d4c4f7d3a9c2e650757a27bb74c83c4996739e989f2c8bf7f7678faa8c7d772
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102733524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8078e8ab06d8dabd6c30cffb03951fa035d85f75c19a83ace29b01cb3ecd272`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 14:19:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Feb 2020 14:19:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:19:30 GMT
ENV GOSU_VERSION=1.7
# Wed, 26 Feb 2020 14:19:42 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 26 Feb 2020 14:19:43 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Feb 2020 14:21:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:21:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 26 Feb 2020 14:21:24 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 26 Feb 2020 14:21:24 GMT
ENV MYSQL_VERSION=5.6.47-1debian9
# Wed, 26 Feb 2020 14:21:25 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 26 Feb 2020 14:21:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 26 Feb 2020 14:21:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Mar 2020 17:30:08 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:30:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 04 Mar 2020 17:30:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:30:09 GMT
EXPOSE 3306
# Wed, 04 Mar 2020 17:30:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda15103a86a472aecface46a21e4687bf799a7a7562172cefd94f4d64ba14eb`  
		Last Modified: Wed, 26 Feb 2020 14:22:05 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55971d75ab8c7112e84a48e647c8bc9941a32bcb23549a0a9b49ad27f4911c95`  
		Last Modified: Wed, 26 Feb 2020 14:22:06 GMT  
		Size: 4.5 MB (4501215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d4ea32020b3db53b4f86b22403895ca3bf327ec1d83de316d59e284fa5409e`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 1.3 MB (1270374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61420072af9194292e8c4b7a8b10f2c1cb474df6a64971ba6575f11eb03c748f`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30862a48418b4f2cc5b8a8d295a13f55d5f73c0a3d761607288fc12848bc733f`  
		Last Modified: Wed, 26 Feb 2020 14:22:59 GMT  
		Size: 10.2 MB (10222848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c2ee3a9a570a80487ed96d3f4ddb051e644a66b75ae356750476aec9e05473`  
		Last Modified: Wed, 26 Feb 2020 14:22:55 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4efadb31dfa55f888104c07bfa6a3ead9db357bfdbe928eaf442f70028bd5a`  
		Last Modified: Wed, 26 Feb 2020 14:22:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd931017b211104e6782056838a12014c435d3a1e2afa406dfba314792703d4e`  
		Last Modified: Wed, 26 Feb 2020 14:23:08 GMT  
		Size: 64.2 MB (64190112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488a8608307942b4c58f2ff11fa239c42c0a779447fc3c4fd1890993e42755a1`  
		Last Modified: Wed, 04 Mar 2020 17:31:15 GMT  
		Size: 5.1 KB (5085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921d4bdabca263cab06d154630307cd947de5983eb169e8023794373dac1d6c6`  
		Last Modified: Wed, 04 Mar 2020 17:31:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:f4a5f5be3d94b4f4d3aef00fbc276ce7c08e62f2e1f28867d930deb73a314c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:b475cf2d99b3209c9fafe7841b6f05cfd862c67ee5b06ff66506216409370b74
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158203061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84164b03fa2ecb33e8b4c1f2636ec3286e90786819faa4d1c103ae147824196a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 04 Mar 2020 17:28:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 04 Mar 2020 17:28:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:28:48 GMT
ENV GOSU_VERSION=1.7
# Wed, 04 Mar 2020 17:28:57 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 04 Mar 2020 17:28:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 04 Mar 2020 17:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:29:05 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 04 Mar 2020 17:29:35 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 04 Mar 2020 17:29:35 GMT
ENV MYSQL_VERSION=5.7.29-1debian10
# Wed, 04 Mar 2020 17:29:36 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 04 Mar 2020 17:30:01 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 04 Mar 2020 17:30:02 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Mar 2020 17:30:02 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:30:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 04 Mar 2020 17:30:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:30:03 GMT
EXPOSE 3306 33060
# Wed, 04 Mar 2020 17:30:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9748e016a5c09d5e1669038c1924dd722b08bebe43298490438fd61eaeaa022`  
		Last Modified: Wed, 04 Mar 2020 17:30:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da54b038fed135fc80d01cc2c1ef143ca69bb418e44261a4f6a62d96cf20a19b`  
		Last Modified: Wed, 04 Mar 2020 17:30:21 GMT  
		Size: 4.2 MB (4178026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6895ec5eb2c0de57232791bdc715eef9753a0ebf379644c4c9d237e77f079509`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 1.3 MB (1277296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ba0647b87721c5700e04da65c5adde40fe7791e8374fd8813e3639636562d`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dce60f2f1a8bab438c8286497a8a11b02965c936f62c5ae2fd5a20f7299284`  
		Last Modified: Wed, 04 Mar 2020 17:30:22 GMT  
		Size: 13.4 MB (13443138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702ec598d0af1ab669d4221882b740a42e5bd99ea5451e7340f32cf0aaf80039`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cca87a5d4dd913a08564698c04fbaaea7c33b9a4e71259976abfe58d0b1fd5`  
		Last Modified: Wed, 04 Mar 2020 17:30:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec05b7b1c5c7542319640df43b9682d58938dbcabecce9c4f8ceea56f0d92c44`  
		Last Modified: Wed, 04 Mar 2020 17:31:10 GMT  
		Size: 112.2 MB (112203117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b1d9f49b053f0713da67fb456618bfa2d682f0236cef99c33fe8099987f0d`  
		Last Modified: Wed, 04 Mar 2020 17:30:53 GMT  
		Size: 5.1 KB (5074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded6a30c87c47884b78ce1cd9dc511a890affc9a503bd234f536192e9aa87ca`  
		Last Modified: Wed, 04 Mar 2020 17:30:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.29`

```console
$ docker pull mysql@sha256:f4a5f5be3d94b4f4d3aef00fbc276ce7c08e62f2e1f28867d930deb73a314c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.29` - linux; amd64

```console
$ docker pull mysql@sha256:b475cf2d99b3209c9fafe7841b6f05cfd862c67ee5b06ff66506216409370b74
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158203061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84164b03fa2ecb33e8b4c1f2636ec3286e90786819faa4d1c103ae147824196a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 04 Mar 2020 17:28:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 04 Mar 2020 17:28:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:28:48 GMT
ENV GOSU_VERSION=1.7
# Wed, 04 Mar 2020 17:28:57 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 04 Mar 2020 17:28:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 04 Mar 2020 17:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:29:05 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 04 Mar 2020 17:29:35 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 04 Mar 2020 17:29:35 GMT
ENV MYSQL_VERSION=5.7.29-1debian10
# Wed, 04 Mar 2020 17:29:36 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 04 Mar 2020 17:30:01 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 04 Mar 2020 17:30:02 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Mar 2020 17:30:02 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:30:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 04 Mar 2020 17:30:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:30:03 GMT
EXPOSE 3306 33060
# Wed, 04 Mar 2020 17:30:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9748e016a5c09d5e1669038c1924dd722b08bebe43298490438fd61eaeaa022`  
		Last Modified: Wed, 04 Mar 2020 17:30:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da54b038fed135fc80d01cc2c1ef143ca69bb418e44261a4f6a62d96cf20a19b`  
		Last Modified: Wed, 04 Mar 2020 17:30:21 GMT  
		Size: 4.2 MB (4178026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6895ec5eb2c0de57232791bdc715eef9753a0ebf379644c4c9d237e77f079509`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 1.3 MB (1277296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ba0647b87721c5700e04da65c5adde40fe7791e8374fd8813e3639636562d`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dce60f2f1a8bab438c8286497a8a11b02965c936f62c5ae2fd5a20f7299284`  
		Last Modified: Wed, 04 Mar 2020 17:30:22 GMT  
		Size: 13.4 MB (13443138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702ec598d0af1ab669d4221882b740a42e5bd99ea5451e7340f32cf0aaf80039`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cca87a5d4dd913a08564698c04fbaaea7c33b9a4e71259976abfe58d0b1fd5`  
		Last Modified: Wed, 04 Mar 2020 17:30:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec05b7b1c5c7542319640df43b9682d58938dbcabecce9c4f8ceea56f0d92c44`  
		Last Modified: Wed, 04 Mar 2020 17:31:10 GMT  
		Size: 112.2 MB (112203117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b1d9f49b053f0713da67fb456618bfa2d682f0236cef99c33fe8099987f0d`  
		Last Modified: Wed, 04 Mar 2020 17:30:53 GMT  
		Size: 5.1 KB (5074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded6a30c87c47884b78ce1cd9dc511a890affc9a503bd234f536192e9aa87ca`  
		Last Modified: Wed, 04 Mar 2020 17:30:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:4a30434ce03d2fa396d0414f075ad9ca9b0b578f14ea5685e24dcbf789450a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:60adb98682fd8b89b3534624d3bce0b15df6a476f92ba102a2f54b2c353a1544
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158956299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b51d9275906910446e03bb86e16a0fe0051d6518ba7ae39c8780fc2323fd637`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 04 Mar 2020 17:28:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 04 Mar 2020 17:28:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:28:48 GMT
ENV GOSU_VERSION=1.7
# Wed, 04 Mar 2020 17:28:57 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 04 Mar 2020 17:28:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 04 Mar 2020 17:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:29:05 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 04 Mar 2020 17:29:05 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 04 Mar 2020 17:29:05 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Wed, 04 Mar 2020 17:29:06 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 04 Mar 2020 17:29:21 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 04 Mar 2020 17:29:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Mar 2020 17:29:22 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Wed, 04 Mar 2020 17:29:22 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:29:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 04 Mar 2020 17:29:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:29:23 GMT
EXPOSE 3306 33060
# Wed, 04 Mar 2020 17:29:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9748e016a5c09d5e1669038c1924dd722b08bebe43298490438fd61eaeaa022`  
		Last Modified: Wed, 04 Mar 2020 17:30:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da54b038fed135fc80d01cc2c1ef143ca69bb418e44261a4f6a62d96cf20a19b`  
		Last Modified: Wed, 04 Mar 2020 17:30:21 GMT  
		Size: 4.2 MB (4178026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6895ec5eb2c0de57232791bdc715eef9753a0ebf379644c4c9d237e77f079509`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 1.3 MB (1277296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ba0647b87721c5700e04da65c5adde40fe7791e8374fd8813e3639636562d`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dce60f2f1a8bab438c8286497a8a11b02965c936f62c5ae2fd5a20f7299284`  
		Last Modified: Wed, 04 Mar 2020 17:30:22 GMT  
		Size: 13.4 MB (13443138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702ec598d0af1ab669d4221882b740a42e5bd99ea5451e7340f32cf0aaf80039`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aba2fcbe8694c47bbee47ac849bce00601c16a3481dcd9079f4b0ee57332564`  
		Last Modified: Wed, 04 Mar 2020 17:30:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26bbbd533e673d78f24dc1f646e223b5361033e19f9a089ad7419e848d9f992`  
		Last Modified: Wed, 04 Mar 2020 17:30:46 GMT  
		Size: 113.0 MB (112955456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd100a66c55ddd0e332db375cecb8e7fd7fc73710156a7aed9f3166a85c38a3`  
		Last Modified: Wed, 04 Mar 2020 17:30:18 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74149336419a5509026f9f950cab5a5c7d9c11f299980058047ab0250bafd370`  
		Last Modified: Wed, 04 Mar 2020 17:30:17 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145ea1f01648ba4cffcf52d7085d76e6fef4b18017d29b462e4c8505b4c251d0`  
		Last Modified: Wed, 04 Mar 2020 17:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:4a30434ce03d2fa396d0414f075ad9ca9b0b578f14ea5685e24dcbf789450a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:60adb98682fd8b89b3534624d3bce0b15df6a476f92ba102a2f54b2c353a1544
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158956299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b51d9275906910446e03bb86e16a0fe0051d6518ba7ae39c8780fc2323fd637`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 04 Mar 2020 17:28:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 04 Mar 2020 17:28:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:28:48 GMT
ENV GOSU_VERSION=1.7
# Wed, 04 Mar 2020 17:28:57 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 04 Mar 2020 17:28:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 04 Mar 2020 17:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:29:05 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 04 Mar 2020 17:29:05 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 04 Mar 2020 17:29:05 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Wed, 04 Mar 2020 17:29:06 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 04 Mar 2020 17:29:21 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 04 Mar 2020 17:29:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Mar 2020 17:29:22 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Wed, 04 Mar 2020 17:29:22 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:29:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 04 Mar 2020 17:29:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:29:23 GMT
EXPOSE 3306 33060
# Wed, 04 Mar 2020 17:29:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9748e016a5c09d5e1669038c1924dd722b08bebe43298490438fd61eaeaa022`  
		Last Modified: Wed, 04 Mar 2020 17:30:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da54b038fed135fc80d01cc2c1ef143ca69bb418e44261a4f6a62d96cf20a19b`  
		Last Modified: Wed, 04 Mar 2020 17:30:21 GMT  
		Size: 4.2 MB (4178026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6895ec5eb2c0de57232791bdc715eef9753a0ebf379644c4c9d237e77f079509`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 1.3 MB (1277296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ba0647b87721c5700e04da65c5adde40fe7791e8374fd8813e3639636562d`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dce60f2f1a8bab438c8286497a8a11b02965c936f62c5ae2fd5a20f7299284`  
		Last Modified: Wed, 04 Mar 2020 17:30:22 GMT  
		Size: 13.4 MB (13443138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702ec598d0af1ab669d4221882b740a42e5bd99ea5451e7340f32cf0aaf80039`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aba2fcbe8694c47bbee47ac849bce00601c16a3481dcd9079f4b0ee57332564`  
		Last Modified: Wed, 04 Mar 2020 17:30:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26bbbd533e673d78f24dc1f646e223b5361033e19f9a089ad7419e848d9f992`  
		Last Modified: Wed, 04 Mar 2020 17:30:46 GMT  
		Size: 113.0 MB (112955456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd100a66c55ddd0e332db375cecb8e7fd7fc73710156a7aed9f3166a85c38a3`  
		Last Modified: Wed, 04 Mar 2020 17:30:18 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74149336419a5509026f9f950cab5a5c7d9c11f299980058047ab0250bafd370`  
		Last Modified: Wed, 04 Mar 2020 17:30:17 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145ea1f01648ba4cffcf52d7085d76e6fef4b18017d29b462e4c8505b4c251d0`  
		Last Modified: Wed, 04 Mar 2020 17:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.19`

```console
$ docker pull mysql@sha256:4a30434ce03d2fa396d0414f075ad9ca9b0b578f14ea5685e24dcbf789450a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.19` - linux; amd64

```console
$ docker pull mysql@sha256:60adb98682fd8b89b3534624d3bce0b15df6a476f92ba102a2f54b2c353a1544
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158956299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b51d9275906910446e03bb86e16a0fe0051d6518ba7ae39c8780fc2323fd637`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 04 Mar 2020 17:28:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 04 Mar 2020 17:28:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:28:48 GMT
ENV GOSU_VERSION=1.7
# Wed, 04 Mar 2020 17:28:57 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 04 Mar 2020 17:28:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 04 Mar 2020 17:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:29:05 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 04 Mar 2020 17:29:05 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 04 Mar 2020 17:29:05 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Wed, 04 Mar 2020 17:29:06 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 04 Mar 2020 17:29:21 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 04 Mar 2020 17:29:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Mar 2020 17:29:22 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Wed, 04 Mar 2020 17:29:22 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:29:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 04 Mar 2020 17:29:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:29:23 GMT
EXPOSE 3306 33060
# Wed, 04 Mar 2020 17:29:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9748e016a5c09d5e1669038c1924dd722b08bebe43298490438fd61eaeaa022`  
		Last Modified: Wed, 04 Mar 2020 17:30:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da54b038fed135fc80d01cc2c1ef143ca69bb418e44261a4f6a62d96cf20a19b`  
		Last Modified: Wed, 04 Mar 2020 17:30:21 GMT  
		Size: 4.2 MB (4178026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6895ec5eb2c0de57232791bdc715eef9753a0ebf379644c4c9d237e77f079509`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 1.3 MB (1277296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ba0647b87721c5700e04da65c5adde40fe7791e8374fd8813e3639636562d`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dce60f2f1a8bab438c8286497a8a11b02965c936f62c5ae2fd5a20f7299284`  
		Last Modified: Wed, 04 Mar 2020 17:30:22 GMT  
		Size: 13.4 MB (13443138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702ec598d0af1ab669d4221882b740a42e5bd99ea5451e7340f32cf0aaf80039`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aba2fcbe8694c47bbee47ac849bce00601c16a3481dcd9079f4b0ee57332564`  
		Last Modified: Wed, 04 Mar 2020 17:30:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26bbbd533e673d78f24dc1f646e223b5361033e19f9a089ad7419e848d9f992`  
		Last Modified: Wed, 04 Mar 2020 17:30:46 GMT  
		Size: 113.0 MB (112955456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd100a66c55ddd0e332db375cecb8e7fd7fc73710156a7aed9f3166a85c38a3`  
		Last Modified: Wed, 04 Mar 2020 17:30:18 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74149336419a5509026f9f950cab5a5c7d9c11f299980058047ab0250bafd370`  
		Last Modified: Wed, 04 Mar 2020 17:30:17 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145ea1f01648ba4cffcf52d7085d76e6fef4b18017d29b462e4c8505b4c251d0`  
		Last Modified: Wed, 04 Mar 2020 17:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:4a30434ce03d2fa396d0414f075ad9ca9b0b578f14ea5685e24dcbf789450a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:60adb98682fd8b89b3534624d3bce0b15df6a476f92ba102a2f54b2c353a1544
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158956299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b51d9275906910446e03bb86e16a0fe0051d6518ba7ae39c8780fc2323fd637`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 04 Mar 2020 17:28:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 04 Mar 2020 17:28:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:28:48 GMT
ENV GOSU_VERSION=1.7
# Wed, 04 Mar 2020 17:28:57 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 04 Mar 2020 17:28:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 04 Mar 2020 17:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 04 Mar 2020 17:29:05 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 04 Mar 2020 17:29:05 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 04 Mar 2020 17:29:05 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Wed, 04 Mar 2020 17:29:06 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 04 Mar 2020 17:29:21 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 04 Mar 2020 17:29:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 04 Mar 2020 17:29:22 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Wed, 04 Mar 2020 17:29:22 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:29:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 04 Mar 2020 17:29:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:29:23 GMT
EXPOSE 3306 33060
# Wed, 04 Mar 2020 17:29:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9748e016a5c09d5e1669038c1924dd722b08bebe43298490438fd61eaeaa022`  
		Last Modified: Wed, 04 Mar 2020 17:30:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da54b038fed135fc80d01cc2c1ef143ca69bb418e44261a4f6a62d96cf20a19b`  
		Last Modified: Wed, 04 Mar 2020 17:30:21 GMT  
		Size: 4.2 MB (4178026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6895ec5eb2c0de57232791bdc715eef9753a0ebf379644c4c9d237e77f079509`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 1.3 MB (1277296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ba0647b87721c5700e04da65c5adde40fe7791e8374fd8813e3639636562d`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dce60f2f1a8bab438c8286497a8a11b02965c936f62c5ae2fd5a20f7299284`  
		Last Modified: Wed, 04 Mar 2020 17:30:22 GMT  
		Size: 13.4 MB (13443138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702ec598d0af1ab669d4221882b740a42e5bd99ea5451e7340f32cf0aaf80039`  
		Last Modified: Wed, 04 Mar 2020 17:30:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aba2fcbe8694c47bbee47ac849bce00601c16a3481dcd9079f4b0ee57332564`  
		Last Modified: Wed, 04 Mar 2020 17:30:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26bbbd533e673d78f24dc1f646e223b5361033e19f9a089ad7419e848d9f992`  
		Last Modified: Wed, 04 Mar 2020 17:30:46 GMT  
		Size: 113.0 MB (112955456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd100a66c55ddd0e332db375cecb8e7fd7fc73710156a7aed9f3166a85c38a3`  
		Last Modified: Wed, 04 Mar 2020 17:30:18 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74149336419a5509026f9f950cab5a5c7d9c11f299980058047ab0250bafd370`  
		Last Modified: Wed, 04 Mar 2020 17:30:17 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145ea1f01648ba4cffcf52d7085d76e6fef4b18017d29b462e4c8505b4c251d0`  
		Last Modified: Wed, 04 Mar 2020 17:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
