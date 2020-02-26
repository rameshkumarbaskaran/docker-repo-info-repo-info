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
$ docker pull mysql@sha256:77f6e10afdf66b58c677af6ac756279826f3c32c30e1a7e642e971fbbc11a061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:f37357e01d188c3b335b42277730816ed6efcac66c455e77ebf7d8db9fa09e94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151989543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1bf91a2e39fa905cac5760f848bca9a6b36b1b76f59267480ea9b7682fa0b8`
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
# Wed, 26 Feb 2020 14:19:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:19:52 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 26 Feb 2020 14:20:27 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 26 Feb 2020 14:20:27 GMT
ENV MYSQL_VERSION=5.7.29-1debian9
# Wed, 26 Feb 2020 14:20:28 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 26 Feb 2020 14:21:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 26 Feb 2020 14:21:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Feb 2020 14:21:05 GMT
COPY file:3f9ea5eebe1c6044ae56c9bb1b511da3bde64f7672f438d25bb8440e5a878d15 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:21:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 26 Feb 2020 14:21:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:21:07 GMT
EXPOSE 3306 33060
# Wed, 26 Feb 2020 14:21:07 GMT
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
	-	`sha256:05c10e6ccca51c7a7e82361b995c60d7adc6d819f13982f11a8a0d337f0a266f`  
		Last Modified: Wed, 26 Feb 2020 14:22:07 GMT  
		Size: 12.2 MB (12163858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0306b13322cefe7d680da8e1dad7ec16ade7a59d5f52e6eba854b68fe4f573`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e2caa5b6cf657c381113eb88cac6154034ec72da4fc18aa3bff90197797aba`  
		Last Modified: Wed, 26 Feb 2020 14:22:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d3c3421b5ff93de483eff389acccc826c59633b9f17b139dc7aee822c5d90b`  
		Last Modified: Wed, 26 Feb 2020 14:22:48 GMT  
		Size: 111.5 MB (111505166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca269db077e6ea5a6a2815c75b410b238c2cf8ca9b17c2a50739e54ed50f5b`  
		Last Modified: Wed, 26 Feb 2020 14:22:29 GMT  
		Size: 5.0 KB (5040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f3d38986a2c1b37b455d3f9273224026217b97aae157d377c3b4481b38b41`  
		Last Modified: Wed, 26 Feb 2020 14:22:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:8e3ddf4452daffc1b60fa7045141e2f58bc3b3ad835c7cd702629638839224ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:795cc3b6dec331340b075afd158c7474d124162b26511e309d8162e60cd370ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102733483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d82167a7ab3ad00155450577e9dc16f16d1cdc7ccb37690ceb32c59ed852014`
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
# Wed, 26 Feb 2020 14:21:47 GMT
COPY file:3f9ea5eebe1c6044ae56c9bb1b511da3bde64f7672f438d25bb8440e5a878d15 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:21:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 26 Feb 2020 14:21:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:21:48 GMT
EXPOSE 3306
# Wed, 26 Feb 2020 14:21:48 GMT
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
	-	`sha256:c8bb37c8601fc0731dd6c4291ffd2a624813d19b3bf50c262f669b5b0d463b9f`  
		Last Modified: Wed, 26 Feb 2020 14:22:56 GMT  
		Size: 5.0 KB (5044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da1c02c5951b04812c675e4a6a2c86cbcb3802f05bc535c21ab1d18bfc1dc17`  
		Last Modified: Wed, 26 Feb 2020 14:22:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.47`

```console
$ docker pull mysql@sha256:8e3ddf4452daffc1b60fa7045141e2f58bc3b3ad835c7cd702629638839224ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.47` - linux; amd64

```console
$ docker pull mysql@sha256:795cc3b6dec331340b075afd158c7474d124162b26511e309d8162e60cd370ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102733483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d82167a7ab3ad00155450577e9dc16f16d1cdc7ccb37690ceb32c59ed852014`
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
# Wed, 26 Feb 2020 14:21:47 GMT
COPY file:3f9ea5eebe1c6044ae56c9bb1b511da3bde64f7672f438d25bb8440e5a878d15 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:21:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 26 Feb 2020 14:21:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:21:48 GMT
EXPOSE 3306
# Wed, 26 Feb 2020 14:21:48 GMT
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
	-	`sha256:c8bb37c8601fc0731dd6c4291ffd2a624813d19b3bf50c262f669b5b0d463b9f`  
		Last Modified: Wed, 26 Feb 2020 14:22:56 GMT  
		Size: 5.0 KB (5044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da1c02c5951b04812c675e4a6a2c86cbcb3802f05bc535c21ab1d18bfc1dc17`  
		Last Modified: Wed, 26 Feb 2020 14:22:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:77f6e10afdf66b58c677af6ac756279826f3c32c30e1a7e642e971fbbc11a061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:f37357e01d188c3b335b42277730816ed6efcac66c455e77ebf7d8db9fa09e94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151989543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1bf91a2e39fa905cac5760f848bca9a6b36b1b76f59267480ea9b7682fa0b8`
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
# Wed, 26 Feb 2020 14:19:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:19:52 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 26 Feb 2020 14:20:27 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 26 Feb 2020 14:20:27 GMT
ENV MYSQL_VERSION=5.7.29-1debian9
# Wed, 26 Feb 2020 14:20:28 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 26 Feb 2020 14:21:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 26 Feb 2020 14:21:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Feb 2020 14:21:05 GMT
COPY file:3f9ea5eebe1c6044ae56c9bb1b511da3bde64f7672f438d25bb8440e5a878d15 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:21:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 26 Feb 2020 14:21:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:21:07 GMT
EXPOSE 3306 33060
# Wed, 26 Feb 2020 14:21:07 GMT
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
	-	`sha256:05c10e6ccca51c7a7e82361b995c60d7adc6d819f13982f11a8a0d337f0a266f`  
		Last Modified: Wed, 26 Feb 2020 14:22:07 GMT  
		Size: 12.2 MB (12163858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0306b13322cefe7d680da8e1dad7ec16ade7a59d5f52e6eba854b68fe4f573`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e2caa5b6cf657c381113eb88cac6154034ec72da4fc18aa3bff90197797aba`  
		Last Modified: Wed, 26 Feb 2020 14:22:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d3c3421b5ff93de483eff389acccc826c59633b9f17b139dc7aee822c5d90b`  
		Last Modified: Wed, 26 Feb 2020 14:22:48 GMT  
		Size: 111.5 MB (111505166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca269db077e6ea5a6a2815c75b410b238c2cf8ca9b17c2a50739e54ed50f5b`  
		Last Modified: Wed, 26 Feb 2020 14:22:29 GMT  
		Size: 5.0 KB (5040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f3d38986a2c1b37b455d3f9273224026217b97aae157d377c3b4481b38b41`  
		Last Modified: Wed, 26 Feb 2020 14:22:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.29`

```console
$ docker pull mysql@sha256:77f6e10afdf66b58c677af6ac756279826f3c32c30e1a7e642e971fbbc11a061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.29` - linux; amd64

```console
$ docker pull mysql@sha256:f37357e01d188c3b335b42277730816ed6efcac66c455e77ebf7d8db9fa09e94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151989543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1bf91a2e39fa905cac5760f848bca9a6b36b1b76f59267480ea9b7682fa0b8`
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
# Wed, 26 Feb 2020 14:19:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:19:52 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 26 Feb 2020 14:20:27 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 26 Feb 2020 14:20:27 GMT
ENV MYSQL_VERSION=5.7.29-1debian9
# Wed, 26 Feb 2020 14:20:28 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 26 Feb 2020 14:21:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 26 Feb 2020 14:21:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Feb 2020 14:21:05 GMT
COPY file:3f9ea5eebe1c6044ae56c9bb1b511da3bde64f7672f438d25bb8440e5a878d15 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:21:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 26 Feb 2020 14:21:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:21:07 GMT
EXPOSE 3306 33060
# Wed, 26 Feb 2020 14:21:07 GMT
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
	-	`sha256:05c10e6ccca51c7a7e82361b995c60d7adc6d819f13982f11a8a0d337f0a266f`  
		Last Modified: Wed, 26 Feb 2020 14:22:07 GMT  
		Size: 12.2 MB (12163858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0306b13322cefe7d680da8e1dad7ec16ade7a59d5f52e6eba854b68fe4f573`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e2caa5b6cf657c381113eb88cac6154034ec72da4fc18aa3bff90197797aba`  
		Last Modified: Wed, 26 Feb 2020 14:22:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d3c3421b5ff93de483eff389acccc826c59633b9f17b139dc7aee822c5d90b`  
		Last Modified: Wed, 26 Feb 2020 14:22:48 GMT  
		Size: 111.5 MB (111505166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca269db077e6ea5a6a2815c75b410b238c2cf8ca9b17c2a50739e54ed50f5b`  
		Last Modified: Wed, 26 Feb 2020 14:22:29 GMT  
		Size: 5.0 KB (5040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9f3d38986a2c1b37b455d3f9273224026217b97aae157d377c3b4481b38b41`  
		Last Modified: Wed, 26 Feb 2020 14:22:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:f91e704ffa9f19b9a267d9321550a0772a1b64902226d739d3527fd6edbe3dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:a592539c5a616b6642bb48822688b6917b373a1293638f9268e8da33e5e9dd1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136723147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ad2be69a220e93826a6308458627b8d5624dc981050fabf950e5de5a7a08a8`
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
# Wed, 26 Feb 2020 14:19:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:19:52 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 26 Feb 2020 14:19:53 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 26 Feb 2020 14:19:53 GMT
ENV MYSQL_VERSION=8.0.19-1debian9
# Wed, 26 Feb 2020 14:19:54 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 26 Feb 2020 14:20:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 26 Feb 2020 14:20:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Feb 2020 14:20:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Wed, 26 Feb 2020 14:20:16 GMT
COPY file:3f9ea5eebe1c6044ae56c9bb1b511da3bde64f7672f438d25bb8440e5a878d15 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 26 Feb 2020 14:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:20:19 GMT
EXPOSE 3306 33060
# Wed, 26 Feb 2020 14:20:19 GMT
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
	-	`sha256:05c10e6ccca51c7a7e82361b995c60d7adc6d819f13982f11a8a0d337f0a266f`  
		Last Modified: Wed, 26 Feb 2020 14:22:07 GMT  
		Size: 12.2 MB (12163858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0306b13322cefe7d680da8e1dad7ec16ade7a59d5f52e6eba854b68fe4f573`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900b113c001e0bde194744e9b2289fc71a3283505e6a26fc11f6f12449877de7`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cd07c30bf4233d640c53be2b3b2adda648e6c40d894f52841da2486586af22`  
		Last Modified: Wed, 26 Feb 2020 14:22:23 GMT  
		Size: 96.2 MB (96237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0d65aee5aaf4cee7e0fb5b9c09fdd487153fcbbcb86e1da0029c2a68847b10`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eeb6e0335c1b4467e871e0f7514fb12d11585014232cbf6b5fb59e3dc744ef`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 5.0 KB (5041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf8f9563e97be04cbe8ea1643ad5d37585597e50dfda005462aa5038357a3e2`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:f91e704ffa9f19b9a267d9321550a0772a1b64902226d739d3527fd6edbe3dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:a592539c5a616b6642bb48822688b6917b373a1293638f9268e8da33e5e9dd1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136723147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ad2be69a220e93826a6308458627b8d5624dc981050fabf950e5de5a7a08a8`
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
# Wed, 26 Feb 2020 14:19:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:19:52 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 26 Feb 2020 14:19:53 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 26 Feb 2020 14:19:53 GMT
ENV MYSQL_VERSION=8.0.19-1debian9
# Wed, 26 Feb 2020 14:19:54 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 26 Feb 2020 14:20:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 26 Feb 2020 14:20:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Feb 2020 14:20:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Wed, 26 Feb 2020 14:20:16 GMT
COPY file:3f9ea5eebe1c6044ae56c9bb1b511da3bde64f7672f438d25bb8440e5a878d15 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 26 Feb 2020 14:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:20:19 GMT
EXPOSE 3306 33060
# Wed, 26 Feb 2020 14:20:19 GMT
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
	-	`sha256:05c10e6ccca51c7a7e82361b995c60d7adc6d819f13982f11a8a0d337f0a266f`  
		Last Modified: Wed, 26 Feb 2020 14:22:07 GMT  
		Size: 12.2 MB (12163858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0306b13322cefe7d680da8e1dad7ec16ade7a59d5f52e6eba854b68fe4f573`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900b113c001e0bde194744e9b2289fc71a3283505e6a26fc11f6f12449877de7`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cd07c30bf4233d640c53be2b3b2adda648e6c40d894f52841da2486586af22`  
		Last Modified: Wed, 26 Feb 2020 14:22:23 GMT  
		Size: 96.2 MB (96237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0d65aee5aaf4cee7e0fb5b9c09fdd487153fcbbcb86e1da0029c2a68847b10`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eeb6e0335c1b4467e871e0f7514fb12d11585014232cbf6b5fb59e3dc744ef`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 5.0 KB (5041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf8f9563e97be04cbe8ea1643ad5d37585597e50dfda005462aa5038357a3e2`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.19`

```console
$ docker pull mysql@sha256:f91e704ffa9f19b9a267d9321550a0772a1b64902226d739d3527fd6edbe3dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.19` - linux; amd64

```console
$ docker pull mysql@sha256:a592539c5a616b6642bb48822688b6917b373a1293638f9268e8da33e5e9dd1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136723147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ad2be69a220e93826a6308458627b8d5624dc981050fabf950e5de5a7a08a8`
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
# Wed, 26 Feb 2020 14:19:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:19:52 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 26 Feb 2020 14:19:53 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 26 Feb 2020 14:19:53 GMT
ENV MYSQL_VERSION=8.0.19-1debian9
# Wed, 26 Feb 2020 14:19:54 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 26 Feb 2020 14:20:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 26 Feb 2020 14:20:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Feb 2020 14:20:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Wed, 26 Feb 2020 14:20:16 GMT
COPY file:3f9ea5eebe1c6044ae56c9bb1b511da3bde64f7672f438d25bb8440e5a878d15 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 26 Feb 2020 14:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:20:19 GMT
EXPOSE 3306 33060
# Wed, 26 Feb 2020 14:20:19 GMT
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
	-	`sha256:05c10e6ccca51c7a7e82361b995c60d7adc6d819f13982f11a8a0d337f0a266f`  
		Last Modified: Wed, 26 Feb 2020 14:22:07 GMT  
		Size: 12.2 MB (12163858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0306b13322cefe7d680da8e1dad7ec16ade7a59d5f52e6eba854b68fe4f573`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900b113c001e0bde194744e9b2289fc71a3283505e6a26fc11f6f12449877de7`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cd07c30bf4233d640c53be2b3b2adda648e6c40d894f52841da2486586af22`  
		Last Modified: Wed, 26 Feb 2020 14:22:23 GMT  
		Size: 96.2 MB (96237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0d65aee5aaf4cee7e0fb5b9c09fdd487153fcbbcb86e1da0029c2a68847b10`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eeb6e0335c1b4467e871e0f7514fb12d11585014232cbf6b5fb59e3dc744ef`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 5.0 KB (5041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf8f9563e97be04cbe8ea1643ad5d37585597e50dfda005462aa5038357a3e2`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:f91e704ffa9f19b9a267d9321550a0772a1b64902226d739d3527fd6edbe3dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:a592539c5a616b6642bb48822688b6917b373a1293638f9268e8da33e5e9dd1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136723147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ad2be69a220e93826a6308458627b8d5624dc981050fabf950e5de5a7a08a8`
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
# Wed, 26 Feb 2020 14:19:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:19:52 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 26 Feb 2020 14:19:53 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 26 Feb 2020 14:19:53 GMT
ENV MYSQL_VERSION=8.0.19-1debian9
# Wed, 26 Feb 2020 14:19:54 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 26 Feb 2020 14:20:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 26 Feb 2020 14:20:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Feb 2020 14:20:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Wed, 26 Feb 2020 14:20:16 GMT
COPY file:3f9ea5eebe1c6044ae56c9bb1b511da3bde64f7672f438d25bb8440e5a878d15 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:20:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 26 Feb 2020 14:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2020 14:20:19 GMT
EXPOSE 3306 33060
# Wed, 26 Feb 2020 14:20:19 GMT
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
	-	`sha256:05c10e6ccca51c7a7e82361b995c60d7adc6d819f13982f11a8a0d337f0a266f`  
		Last Modified: Wed, 26 Feb 2020 14:22:07 GMT  
		Size: 12.2 MB (12163858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0306b13322cefe7d680da8e1dad7ec16ade7a59d5f52e6eba854b68fe4f573`  
		Last Modified: Wed, 26 Feb 2020 14:22:04 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900b113c001e0bde194744e9b2289fc71a3283505e6a26fc11f6f12449877de7`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cd07c30bf4233d640c53be2b3b2adda648e6c40d894f52841da2486586af22`  
		Last Modified: Wed, 26 Feb 2020 14:22:23 GMT  
		Size: 96.2 MB (96237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0d65aee5aaf4cee7e0fb5b9c09fdd487153fcbbcb86e1da0029c2a68847b10`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eeb6e0335c1b4467e871e0f7514fb12d11585014232cbf6b5fb59e3dc744ef`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 5.0 KB (5041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf8f9563e97be04cbe8ea1643ad5d37585597e50dfda005462aa5038357a3e2`  
		Last Modified: Wed, 26 Feb 2020 14:22:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
