<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.51`](#mysql5651)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.34`](#mysql5734)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.25`](#mysql8025)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:a682e3c78fc5bd941e9db080b4796c75f69a28a8cad65677c23f7a9f18ba21fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:92ad1d7e3f8eb7e67d35bf251912fb7cd12676a601dc90b6beb1aece7c1f5073
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154437118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9028880e5814e8923c278d7e2059f9066d56608a21cd3f83a01e3337bacd68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:09:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 May 2021 08:09:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:09:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 08:09:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 08:09:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 08:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:10:04 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 12 May 2021 08:10:37 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 12 May 2021 08:10:38 GMT
ENV MYSQL_VERSION=5.7.34-1debian10
# Wed, 12 May 2021 08:10:40 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 May 2021 08:11:00 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 May 2021 08:11:01 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 May 2021 08:11:01 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Wed, 12 May 2021 08:11:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 May 2021 08:11:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 May 2021 08:11:03 GMT
EXPOSE 3306 33060
# Wed, 12 May 2021 08:11:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1651b0be3df3b7c2b57c16e7932836c239fe5f5f1625e390147b5ea0dac3b3e0`  
		Last Modified: Wed, 12 May 2021 08:12:32 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951da7386bc8b010c95056608b66b1e7431ef0e895a1717528d3a16cda93f341`  
		Last Modified: Wed, 12 May 2021 08:12:33 GMT  
		Size: 4.2 MB (4179301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f86c95aa2427b656dbc0bf01413bb8af354ea168e660887eb93ee816ad360a1`  
		Last Modified: Wed, 12 May 2021 08:12:30 GMT  
		Size: 1.4 MB (1419437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ba2d8bd4fe60e7cd8ba1fe43fec4fde06acd0f4407a3db4b4dea1450f19f99`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278bb05e94d4d1aa8bf5b6db09d8b5d8421b61026ba29c78405521e3aa49eb`  
		Last Modified: Wed, 12 May 2021 08:12:35 GMT  
		Size: 13.4 MB (13447524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497efbd93a3eb09094c94c3a06b0a2fc6b8cc224812b464a8dd4889d5c2af266`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a023ae82eef58ac1a6d2d2161a1c085cdc6e7a19aec33653d3af043c82dc8f29`  
		Last Modified: Wed, 12 May 2021 08:13:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c35f20ee7c3d56102e7a8b7462b0f61e0e457318317bd252ea0c08b9589e2`  
		Last Modified: Wed, 12 May 2021 08:13:40 GMT  
		Size: 108.2 MB (108234777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e887524d2ef90488936c4286860fa24aa6659d115b45f25b8f9486b5013040d1`  
		Last Modified: Wed, 12 May 2021 08:13:19 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb65627e1c3c2c6580de60b241f7d4501b479cd268e3721ab3e9bafd70164fa`  
		Last Modified: Wed, 12 May 2021 08:13:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:1d96ea86f9173607f1534c05041bf18dba691ded86d2ab51f6fd4533377fac39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:0cec2428f4827e0581893af9b8d9fbfa84c3dbf2add6aabc645efa7f773bc00f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102980757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3045d3a6e718a5429041301b0c2b5acfb2768b8bb5a94a1e26d589c1f2f4bd51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:11:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 May 2021 08:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:11:15 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 08:11:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 08:11:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 08:11:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:11:37 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 12 May 2021 08:11:38 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 12 May 2021 08:11:38 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Wed, 12 May 2021 08:11:39 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 May 2021 08:11:58 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 May 2021 08:11:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 May 2021 08:11:59 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Wed, 12 May 2021 08:12:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 May 2021 08:12:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 May 2021 08:12:03 GMT
EXPOSE 3306
# Wed, 12 May 2021 08:12:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385bc110a881dd0a90813fb6ddbfa67fd579e636c4e213252188d732d023fef0`  
		Last Modified: Wed, 12 May 2021 08:14:00 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b576ec9cbcd09883a65b72bb81be7d46b72848523f131290a626a30314ba5060`  
		Last Modified: Wed, 12 May 2021 08:13:59 GMT  
		Size: 4.5 MB (4503299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badcfd010ebe4e389805efd03a5a08327a99e6cfef7d93abbcbaeba0c52f7ead`  
		Last Modified: Wed, 12 May 2021 08:13:58 GMT  
		Size: 1.4 MB (1412264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77aee01abe1ee01b7746c03134f61333bebf4a0b5ff9e19b95d4b5dc005ae4dc`  
		Last Modified: Wed, 12 May 2021 08:13:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2356508746309a5585ee912e236ba72191b675f10489445421a683d18dc459c4`  
		Last Modified: Wed, 12 May 2021 08:14:02 GMT  
		Size: 10.2 MB (10225806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7926d4338e89d3438b2262b387d2403852700ed4039d28908cf2f4b8bccc0`  
		Last Modified: Wed, 12 May 2021 08:13:55 GMT  
		Size: 29.0 KB (28954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c611bff81de75dc67cac44402fe79b6d926d0305afaaa1dc2d3fa9af5d8723b`  
		Last Modified: Wed, 12 May 2021 08:13:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ef93c8315556bbc6e201dfb9930971a5b5ecc12770afed250990a82bfe2e59`  
		Last Modified: Wed, 12 May 2021 08:14:11 GMT  
		Size: 64.3 MB (64274377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d070554f81b744024bc391254d91873ed68639309d0408f1c3238c0bbfdb493e`  
		Last Modified: Wed, 12 May 2021 08:13:55 GMT  
		Size: 5.6 KB (5558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60218a9a3b7f9bc04e0cbc17239817d05da305240d06b5c89ff94babe4dad5a`  
		Last Modified: Wed, 12 May 2021 08:13:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.51`

```console
$ docker pull mysql@sha256:1d96ea86f9173607f1534c05041bf18dba691ded86d2ab51f6fd4533377fac39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.51` - linux; amd64

```console
$ docker pull mysql@sha256:0cec2428f4827e0581893af9b8d9fbfa84c3dbf2add6aabc645efa7f773bc00f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102980757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3045d3a6e718a5429041301b0c2b5acfb2768b8bb5a94a1e26d589c1f2f4bd51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:11:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 May 2021 08:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:11:15 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 08:11:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 08:11:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 08:11:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:11:37 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 12 May 2021 08:11:38 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 12 May 2021 08:11:38 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Wed, 12 May 2021 08:11:39 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 May 2021 08:11:58 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 May 2021 08:11:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 May 2021 08:11:59 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Wed, 12 May 2021 08:12:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 May 2021 08:12:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 May 2021 08:12:03 GMT
EXPOSE 3306
# Wed, 12 May 2021 08:12:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385bc110a881dd0a90813fb6ddbfa67fd579e636c4e213252188d732d023fef0`  
		Last Modified: Wed, 12 May 2021 08:14:00 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b576ec9cbcd09883a65b72bb81be7d46b72848523f131290a626a30314ba5060`  
		Last Modified: Wed, 12 May 2021 08:13:59 GMT  
		Size: 4.5 MB (4503299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badcfd010ebe4e389805efd03a5a08327a99e6cfef7d93abbcbaeba0c52f7ead`  
		Last Modified: Wed, 12 May 2021 08:13:58 GMT  
		Size: 1.4 MB (1412264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77aee01abe1ee01b7746c03134f61333bebf4a0b5ff9e19b95d4b5dc005ae4dc`  
		Last Modified: Wed, 12 May 2021 08:13:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2356508746309a5585ee912e236ba72191b675f10489445421a683d18dc459c4`  
		Last Modified: Wed, 12 May 2021 08:14:02 GMT  
		Size: 10.2 MB (10225806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7926d4338e89d3438b2262b387d2403852700ed4039d28908cf2f4b8bccc0`  
		Last Modified: Wed, 12 May 2021 08:13:55 GMT  
		Size: 29.0 KB (28954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c611bff81de75dc67cac44402fe79b6d926d0305afaaa1dc2d3fa9af5d8723b`  
		Last Modified: Wed, 12 May 2021 08:13:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ef93c8315556bbc6e201dfb9930971a5b5ecc12770afed250990a82bfe2e59`  
		Last Modified: Wed, 12 May 2021 08:14:11 GMT  
		Size: 64.3 MB (64274377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d070554f81b744024bc391254d91873ed68639309d0408f1c3238c0bbfdb493e`  
		Last Modified: Wed, 12 May 2021 08:13:55 GMT  
		Size: 5.6 KB (5558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60218a9a3b7f9bc04e0cbc17239817d05da305240d06b5c89ff94babe4dad5a`  
		Last Modified: Wed, 12 May 2021 08:13:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:a682e3c78fc5bd941e9db080b4796c75f69a28a8cad65677c23f7a9f18ba21fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:92ad1d7e3f8eb7e67d35bf251912fb7cd12676a601dc90b6beb1aece7c1f5073
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154437118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9028880e5814e8923c278d7e2059f9066d56608a21cd3f83a01e3337bacd68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:09:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 May 2021 08:09:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:09:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 08:09:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 08:09:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 08:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:10:04 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 12 May 2021 08:10:37 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 12 May 2021 08:10:38 GMT
ENV MYSQL_VERSION=5.7.34-1debian10
# Wed, 12 May 2021 08:10:40 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 May 2021 08:11:00 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 May 2021 08:11:01 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 May 2021 08:11:01 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Wed, 12 May 2021 08:11:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 May 2021 08:11:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 May 2021 08:11:03 GMT
EXPOSE 3306 33060
# Wed, 12 May 2021 08:11:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1651b0be3df3b7c2b57c16e7932836c239fe5f5f1625e390147b5ea0dac3b3e0`  
		Last Modified: Wed, 12 May 2021 08:12:32 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951da7386bc8b010c95056608b66b1e7431ef0e895a1717528d3a16cda93f341`  
		Last Modified: Wed, 12 May 2021 08:12:33 GMT  
		Size: 4.2 MB (4179301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f86c95aa2427b656dbc0bf01413bb8af354ea168e660887eb93ee816ad360a1`  
		Last Modified: Wed, 12 May 2021 08:12:30 GMT  
		Size: 1.4 MB (1419437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ba2d8bd4fe60e7cd8ba1fe43fec4fde06acd0f4407a3db4b4dea1450f19f99`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278bb05e94d4d1aa8bf5b6db09d8b5d8421b61026ba29c78405521e3aa49eb`  
		Last Modified: Wed, 12 May 2021 08:12:35 GMT  
		Size: 13.4 MB (13447524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497efbd93a3eb09094c94c3a06b0a2fc6b8cc224812b464a8dd4889d5c2af266`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a023ae82eef58ac1a6d2d2161a1c085cdc6e7a19aec33653d3af043c82dc8f29`  
		Last Modified: Wed, 12 May 2021 08:13:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c35f20ee7c3d56102e7a8b7462b0f61e0e457318317bd252ea0c08b9589e2`  
		Last Modified: Wed, 12 May 2021 08:13:40 GMT  
		Size: 108.2 MB (108234777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e887524d2ef90488936c4286860fa24aa6659d115b45f25b8f9486b5013040d1`  
		Last Modified: Wed, 12 May 2021 08:13:19 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb65627e1c3c2c6580de60b241f7d4501b479cd268e3721ab3e9bafd70164fa`  
		Last Modified: Wed, 12 May 2021 08:13:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.34`

```console
$ docker pull mysql@sha256:a682e3c78fc5bd941e9db080b4796c75f69a28a8cad65677c23f7a9f18ba21fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.34` - linux; amd64

```console
$ docker pull mysql@sha256:92ad1d7e3f8eb7e67d35bf251912fb7cd12676a601dc90b6beb1aece7c1f5073
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154437118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9028880e5814e8923c278d7e2059f9066d56608a21cd3f83a01e3337bacd68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:09:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 May 2021 08:09:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:09:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 08:09:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 08:09:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 08:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:10:04 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 12 May 2021 08:10:37 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 12 May 2021 08:10:38 GMT
ENV MYSQL_VERSION=5.7.34-1debian10
# Wed, 12 May 2021 08:10:40 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 May 2021 08:11:00 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 May 2021 08:11:01 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 May 2021 08:11:01 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Wed, 12 May 2021 08:11:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 May 2021 08:11:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 May 2021 08:11:03 GMT
EXPOSE 3306 33060
# Wed, 12 May 2021 08:11:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1651b0be3df3b7c2b57c16e7932836c239fe5f5f1625e390147b5ea0dac3b3e0`  
		Last Modified: Wed, 12 May 2021 08:12:32 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951da7386bc8b010c95056608b66b1e7431ef0e895a1717528d3a16cda93f341`  
		Last Modified: Wed, 12 May 2021 08:12:33 GMT  
		Size: 4.2 MB (4179301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f86c95aa2427b656dbc0bf01413bb8af354ea168e660887eb93ee816ad360a1`  
		Last Modified: Wed, 12 May 2021 08:12:30 GMT  
		Size: 1.4 MB (1419437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ba2d8bd4fe60e7cd8ba1fe43fec4fde06acd0f4407a3db4b4dea1450f19f99`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278bb05e94d4d1aa8bf5b6db09d8b5d8421b61026ba29c78405521e3aa49eb`  
		Last Modified: Wed, 12 May 2021 08:12:35 GMT  
		Size: 13.4 MB (13447524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497efbd93a3eb09094c94c3a06b0a2fc6b8cc224812b464a8dd4889d5c2af266`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a023ae82eef58ac1a6d2d2161a1c085cdc6e7a19aec33653d3af043c82dc8f29`  
		Last Modified: Wed, 12 May 2021 08:13:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c35f20ee7c3d56102e7a8b7462b0f61e0e457318317bd252ea0c08b9589e2`  
		Last Modified: Wed, 12 May 2021 08:13:40 GMT  
		Size: 108.2 MB (108234777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e887524d2ef90488936c4286860fa24aa6659d115b45f25b8f9486b5013040d1`  
		Last Modified: Wed, 12 May 2021 08:13:19 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb65627e1c3c2c6580de60b241f7d4501b479cd268e3721ab3e9bafd70164fa`  
		Last Modified: Wed, 12 May 2021 08:13:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:d50098d7fcb25b1fcb24e2d3247cae3fc55815d64fec640dc395840f8fa80969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:68b207d01891915410db3b5bc1f69963e3dc8f23813fd01e61e6d7e7e3a46680
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162009000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdc95609f1fc1daf2c7cae05ebd6adcf7b5c614b4f424949554a24012e3c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:09:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 May 2021 08:09:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:09:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 08:09:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 08:09:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 08:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:10:04 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 12 May 2021 08:10:04 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 12 May 2021 08:10:04 GMT
ENV MYSQL_VERSION=8.0.25-1debian10
# Wed, 12 May 2021 08:10:06 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 May 2021 08:10:29 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 May 2021 08:10:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 May 2021 08:10:30 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 12 May 2021 08:10:31 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Wed, 12 May 2021 08:10:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 May 2021 08:10:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 May 2021 08:10:32 GMT
EXPOSE 3306 33060
# Wed, 12 May 2021 08:10:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1651b0be3df3b7c2b57c16e7932836c239fe5f5f1625e390147b5ea0dac3b3e0`  
		Last Modified: Wed, 12 May 2021 08:12:32 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951da7386bc8b010c95056608b66b1e7431ef0e895a1717528d3a16cda93f341`  
		Last Modified: Wed, 12 May 2021 08:12:33 GMT  
		Size: 4.2 MB (4179301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f86c95aa2427b656dbc0bf01413bb8af354ea168e660887eb93ee816ad360a1`  
		Last Modified: Wed, 12 May 2021 08:12:30 GMT  
		Size: 1.4 MB (1419437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ba2d8bd4fe60e7cd8ba1fe43fec4fde06acd0f4407a3db4b4dea1450f19f99`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278bb05e94d4d1aa8bf5b6db09d8b5d8421b61026ba29c78405521e3aa49eb`  
		Last Modified: Wed, 12 May 2021 08:12:35 GMT  
		Size: 13.4 MB (13447524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497efbd93a3eb09094c94c3a06b0a2fc6b8cc224812b464a8dd4889d5c2af266`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fddf10c2c2d7643ac60e6e748d418847c6c5b8d2d772d6d777e5bc4cfed299`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16415d159dfb70afbd4d25c43bd44d506c6d3b15d7f7518494331f7001c7d024`  
		Last Modified: Wed, 12 May 2021 08:13:01 GMT  
		Size: 115.8 MB (115805815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e530ffc6b73401d9bb9ecff4a3ec072184ae79f4d858fa37f6373a7b731f483`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a4a1a771782ef8e5e7d4ef8ace68fd47ba9b9cacff585f7b6b619b0eb60ea2`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 5.5 KB (5539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd90f92aa9ef2e393330b60b73d8e18f473a780a7caaa2e97378379d08da920e`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:d50098d7fcb25b1fcb24e2d3247cae3fc55815d64fec640dc395840f8fa80969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:68b207d01891915410db3b5bc1f69963e3dc8f23813fd01e61e6d7e7e3a46680
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162009000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdc95609f1fc1daf2c7cae05ebd6adcf7b5c614b4f424949554a24012e3c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:09:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 May 2021 08:09:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:09:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 08:09:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 08:09:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 08:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:10:04 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 12 May 2021 08:10:04 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 12 May 2021 08:10:04 GMT
ENV MYSQL_VERSION=8.0.25-1debian10
# Wed, 12 May 2021 08:10:06 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 May 2021 08:10:29 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 May 2021 08:10:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 May 2021 08:10:30 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 12 May 2021 08:10:31 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Wed, 12 May 2021 08:10:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 May 2021 08:10:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 May 2021 08:10:32 GMT
EXPOSE 3306 33060
# Wed, 12 May 2021 08:10:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1651b0be3df3b7c2b57c16e7932836c239fe5f5f1625e390147b5ea0dac3b3e0`  
		Last Modified: Wed, 12 May 2021 08:12:32 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951da7386bc8b010c95056608b66b1e7431ef0e895a1717528d3a16cda93f341`  
		Last Modified: Wed, 12 May 2021 08:12:33 GMT  
		Size: 4.2 MB (4179301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f86c95aa2427b656dbc0bf01413bb8af354ea168e660887eb93ee816ad360a1`  
		Last Modified: Wed, 12 May 2021 08:12:30 GMT  
		Size: 1.4 MB (1419437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ba2d8bd4fe60e7cd8ba1fe43fec4fde06acd0f4407a3db4b4dea1450f19f99`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278bb05e94d4d1aa8bf5b6db09d8b5d8421b61026ba29c78405521e3aa49eb`  
		Last Modified: Wed, 12 May 2021 08:12:35 GMT  
		Size: 13.4 MB (13447524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497efbd93a3eb09094c94c3a06b0a2fc6b8cc224812b464a8dd4889d5c2af266`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fddf10c2c2d7643ac60e6e748d418847c6c5b8d2d772d6d777e5bc4cfed299`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16415d159dfb70afbd4d25c43bd44d506c6d3b15d7f7518494331f7001c7d024`  
		Last Modified: Wed, 12 May 2021 08:13:01 GMT  
		Size: 115.8 MB (115805815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e530ffc6b73401d9bb9ecff4a3ec072184ae79f4d858fa37f6373a7b731f483`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a4a1a771782ef8e5e7d4ef8ace68fd47ba9b9cacff585f7b6b619b0eb60ea2`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 5.5 KB (5539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd90f92aa9ef2e393330b60b73d8e18f473a780a7caaa2e97378379d08da920e`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.25`

```console
$ docker pull mysql@sha256:d50098d7fcb25b1fcb24e2d3247cae3fc55815d64fec640dc395840f8fa80969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.25` - linux; amd64

```console
$ docker pull mysql@sha256:68b207d01891915410db3b5bc1f69963e3dc8f23813fd01e61e6d7e7e3a46680
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162009000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdc95609f1fc1daf2c7cae05ebd6adcf7b5c614b4f424949554a24012e3c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:09:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 May 2021 08:09:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:09:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 08:09:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 08:09:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 08:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:10:04 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 12 May 2021 08:10:04 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 12 May 2021 08:10:04 GMT
ENV MYSQL_VERSION=8.0.25-1debian10
# Wed, 12 May 2021 08:10:06 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 May 2021 08:10:29 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 May 2021 08:10:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 May 2021 08:10:30 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 12 May 2021 08:10:31 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Wed, 12 May 2021 08:10:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 May 2021 08:10:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 May 2021 08:10:32 GMT
EXPOSE 3306 33060
# Wed, 12 May 2021 08:10:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1651b0be3df3b7c2b57c16e7932836c239fe5f5f1625e390147b5ea0dac3b3e0`  
		Last Modified: Wed, 12 May 2021 08:12:32 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951da7386bc8b010c95056608b66b1e7431ef0e895a1717528d3a16cda93f341`  
		Last Modified: Wed, 12 May 2021 08:12:33 GMT  
		Size: 4.2 MB (4179301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f86c95aa2427b656dbc0bf01413bb8af354ea168e660887eb93ee816ad360a1`  
		Last Modified: Wed, 12 May 2021 08:12:30 GMT  
		Size: 1.4 MB (1419437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ba2d8bd4fe60e7cd8ba1fe43fec4fde06acd0f4407a3db4b4dea1450f19f99`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278bb05e94d4d1aa8bf5b6db09d8b5d8421b61026ba29c78405521e3aa49eb`  
		Last Modified: Wed, 12 May 2021 08:12:35 GMT  
		Size: 13.4 MB (13447524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497efbd93a3eb09094c94c3a06b0a2fc6b8cc224812b464a8dd4889d5c2af266`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fddf10c2c2d7643ac60e6e748d418847c6c5b8d2d772d6d777e5bc4cfed299`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16415d159dfb70afbd4d25c43bd44d506c6d3b15d7f7518494331f7001c7d024`  
		Last Modified: Wed, 12 May 2021 08:13:01 GMT  
		Size: 115.8 MB (115805815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e530ffc6b73401d9bb9ecff4a3ec072184ae79f4d858fa37f6373a7b731f483`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a4a1a771782ef8e5e7d4ef8ace68fd47ba9b9cacff585f7b6b619b0eb60ea2`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 5.5 KB (5539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd90f92aa9ef2e393330b60b73d8e18f473a780a7caaa2e97378379d08da920e`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:d50098d7fcb25b1fcb24e2d3247cae3fc55815d64fec640dc395840f8fa80969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:68b207d01891915410db3b5bc1f69963e3dc8f23813fd01e61e6d7e7e3a46680
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162009000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdc95609f1fc1daf2c7cae05ebd6adcf7b5c614b4f424949554a24012e3c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:09:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 May 2021 08:09:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:09:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 08:09:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 08:09:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 08:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:10:04 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 12 May 2021 08:10:04 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 12 May 2021 08:10:04 GMT
ENV MYSQL_VERSION=8.0.25-1debian10
# Wed, 12 May 2021 08:10:06 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 May 2021 08:10:29 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 May 2021 08:10:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 May 2021 08:10:30 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 12 May 2021 08:10:31 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Wed, 12 May 2021 08:10:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 May 2021 08:10:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 May 2021 08:10:32 GMT
EXPOSE 3306 33060
# Wed, 12 May 2021 08:10:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1651b0be3df3b7c2b57c16e7932836c239fe5f5f1625e390147b5ea0dac3b3e0`  
		Last Modified: Wed, 12 May 2021 08:12:32 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951da7386bc8b010c95056608b66b1e7431ef0e895a1717528d3a16cda93f341`  
		Last Modified: Wed, 12 May 2021 08:12:33 GMT  
		Size: 4.2 MB (4179301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f86c95aa2427b656dbc0bf01413bb8af354ea168e660887eb93ee816ad360a1`  
		Last Modified: Wed, 12 May 2021 08:12:30 GMT  
		Size: 1.4 MB (1419437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ba2d8bd4fe60e7cd8ba1fe43fec4fde06acd0f4407a3db4b4dea1450f19f99`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278bb05e94d4d1aa8bf5b6db09d8b5d8421b61026ba29c78405521e3aa49eb`  
		Last Modified: Wed, 12 May 2021 08:12:35 GMT  
		Size: 13.4 MB (13447524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497efbd93a3eb09094c94c3a06b0a2fc6b8cc224812b464a8dd4889d5c2af266`  
		Last Modified: Wed, 12 May 2021 08:12:29 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fddf10c2c2d7643ac60e6e748d418847c6c5b8d2d772d6d777e5bc4cfed299`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16415d159dfb70afbd4d25c43bd44d506c6d3b15d7f7518494331f7001c7d024`  
		Last Modified: Wed, 12 May 2021 08:13:01 GMT  
		Size: 115.8 MB (115805815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e530ffc6b73401d9bb9ecff4a3ec072184ae79f4d858fa37f6373a7b731f483`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a4a1a771782ef8e5e7d4ef8ace68fd47ba9b9cacff585f7b6b619b0eb60ea2`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 5.5 KB (5539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd90f92aa9ef2e393330b60b73d8e18f473a780a7caaa2e97378379d08da920e`  
		Last Modified: Wed, 12 May 2021 08:12:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
