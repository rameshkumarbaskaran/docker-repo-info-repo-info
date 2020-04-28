<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.48`](#mysql5648)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.30`](#mysql5730)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.20`](#mysql8020)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:e821ca8cc7a44d354486f30c6a193ec6b70a4eed8c8362aeede4e9b8d74b8ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:34ae988981413ec8a6bd9735bdc78bc44943bcebc2899578c9b63d65aca283e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154405308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f965319e89deaebf165f58d08b1a217971bf411e9d9860e294634b72d09ab6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:13:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:13:59 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:14:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:14:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:15:08 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Apr 2020 01:53:14 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Tue, 28 Apr 2020 01:53:15 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Apr 2020 01:53:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 28 Apr 2020 01:53:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Apr 2020 01:53:38 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Tue, 28 Apr 2020 01:53:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Apr 2020 01:53:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2020 01:53:39 GMT
EXPOSE 3306 33060
# Tue, 28 Apr 2020 01:53:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc6c614591231a51a8abf93a762208fd1aed3f72f3e3fd0b8907904e3c9a38b`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c3d959c9d9548b3c320af7856e6e16c967daf7d280ac2607e49aa2b3816dd`  
		Last Modified: Thu, 23 Apr 2020 04:17:32 GMT  
		Size: 4.2 MB (4178101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de4d0e206e076ed00d1b32a5104bcd7246484f51de192ba7d5b5c75fe215d0`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.4 MB (1419225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f0394ef4231f3e9f43809855fba117032c697e51c94defda703f34a527b43`  
		Last Modified: Thu, 23 Apr 2020 04:17:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9185034607beae95fac5ee5b684c0182fa10a66b51ba65a7e81345e860b91c2`  
		Last Modified: Thu, 23 Apr 2020 04:17:35 GMT  
		Size: 13.4 MB (13443052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a9c64dadc90a7aef7354825e9668f7b7667ad915df865cb4d05142a76938e`  
		Last Modified: Thu, 23 Apr 2020 04:17:28 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e745b33616262bd650a554bb10b60f10945f670c6e534cf8a76e84adcec60500`  
		Last Modified: Tue, 28 Apr 2020 01:54:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03145d87b451d5e545361351f6c36837d504930a1597d9372a352a49fbce4289`  
		Last Modified: Tue, 28 Apr 2020 01:54:56 GMT  
		Size: 108.3 MB (108256954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3991a6b182ee395a9d599513128506214ff9bf4fe5edd363b954e55ffc22d6b4`  
		Last Modified: Tue, 28 Apr 2020 01:54:40 GMT  
		Size: 5.1 KB (5133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62335de06f7d86c53bc2f1e07fed62cc610e11c3cb1105b2b4b90211c78f5793`  
		Last Modified: Tue, 28 Apr 2020 01:54:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:f77b19ed0467ccb44d54550b9707aec339d61d570dd4d6f648a9d35e1310eafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:ff5bb22baefbea0afa63c0d0df5fa22c0b79f6fac7d316e1a4768f0aa8e3bd89
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102880917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa411733b0ca406f1a2b0115832c29ad45a9fed385b92e5a8afbc6f1cdddf32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:16:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:16:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:16:13 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:16:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:16:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:16:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:16:44 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:16:44 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 28 Apr 2020 01:53:44 GMT
ENV MYSQL_VERSION=5.6.48-1debian9
# Tue, 28 Apr 2020 01:53:45 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Apr 2020 01:54:03 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 28 Apr 2020 01:54:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Apr 2020 01:54:04 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Tue, 28 Apr 2020 01:54:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Apr 2020 01:54:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2020 01:54:05 GMT
EXPOSE 3306
# Tue, 28 Apr 2020 01:54:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0058702edba7456c09cc65fc8215cdb4de22e5b5619657b3429b4612e0782492`  
		Last Modified: Thu, 23 Apr 2020 04:18:41 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e63f6f229769b34b9dc42ef242e26827f4ef62dc068b8cfb3978896d1f400f`  
		Last Modified: Thu, 23 Apr 2020 04:18:41 GMT  
		Size: 4.5 MB (4501274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad333a340332086ec5356c921af17ee104cf83bc65316ebb8eba19e53baa07`  
		Last Modified: Thu, 23 Apr 2020 04:18:40 GMT  
		Size: 1.4 MB (1412350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3708a6b9545b82d874821a4e519265431f64c59be326f3a8d634c588abec0673`  
		Last Modified: Thu, 23 Apr 2020 04:18:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442342ef4996aa063f2752b7f40a8814f35f583fccb430f62f58087db31d6431`  
		Last Modified: Thu, 23 Apr 2020 04:18:44 GMT  
		Size: 10.2 MB (10222752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf24ffdea0f6a9b3a7ec50870603c50b164d3f65730cea120f246f1421a6952`  
		Last Modified: Thu, 23 Apr 2020 04:18:38 GMT  
		Size: 28.3 KB (28326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7a5158d097132bab3e3cbb6e9f2ec25afd581f0319973c206dc617b9d42daa`  
		Last Modified: Tue, 28 Apr 2020 01:55:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf457681dfd85539a9068ef8c86dab67250c1a52a53dd9cddcc8308d886a384`  
		Last Modified: Tue, 28 Apr 2020 01:55:14 GMT  
		Size: 64.2 MB (64195377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0a8ff4a16b33c280909d33b99836a9a88ab7170401bd67637888068cd54aa3`  
		Last Modified: Tue, 28 Apr 2020 01:55:03 GMT  
		Size: 5.1 KB (5148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161b9a3ea21688f4c5a01f4bdc215218d376cdcabc9a538e3bd7bc9b3df9fb29`  
		Last Modified: Tue, 28 Apr 2020 01:55:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.48`

```console
$ docker pull mysql@sha256:f77b19ed0467ccb44d54550b9707aec339d61d570dd4d6f648a9d35e1310eafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.48` - linux; amd64

```console
$ docker pull mysql@sha256:ff5bb22baefbea0afa63c0d0df5fa22c0b79f6fac7d316e1a4768f0aa8e3bd89
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102880917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa411733b0ca406f1a2b0115832c29ad45a9fed385b92e5a8afbc6f1cdddf32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:16:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:16:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:16:13 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:16:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:16:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:16:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:16:44 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:16:44 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 28 Apr 2020 01:53:44 GMT
ENV MYSQL_VERSION=5.6.48-1debian9
# Tue, 28 Apr 2020 01:53:45 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Apr 2020 01:54:03 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 28 Apr 2020 01:54:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Apr 2020 01:54:04 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Tue, 28 Apr 2020 01:54:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Apr 2020 01:54:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2020 01:54:05 GMT
EXPOSE 3306
# Tue, 28 Apr 2020 01:54:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0058702edba7456c09cc65fc8215cdb4de22e5b5619657b3429b4612e0782492`  
		Last Modified: Thu, 23 Apr 2020 04:18:41 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e63f6f229769b34b9dc42ef242e26827f4ef62dc068b8cfb3978896d1f400f`  
		Last Modified: Thu, 23 Apr 2020 04:18:41 GMT  
		Size: 4.5 MB (4501274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad333a340332086ec5356c921af17ee104cf83bc65316ebb8eba19e53baa07`  
		Last Modified: Thu, 23 Apr 2020 04:18:40 GMT  
		Size: 1.4 MB (1412350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3708a6b9545b82d874821a4e519265431f64c59be326f3a8d634c588abec0673`  
		Last Modified: Thu, 23 Apr 2020 04:18:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442342ef4996aa063f2752b7f40a8814f35f583fccb430f62f58087db31d6431`  
		Last Modified: Thu, 23 Apr 2020 04:18:44 GMT  
		Size: 10.2 MB (10222752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf24ffdea0f6a9b3a7ec50870603c50b164d3f65730cea120f246f1421a6952`  
		Last Modified: Thu, 23 Apr 2020 04:18:38 GMT  
		Size: 28.3 KB (28326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7a5158d097132bab3e3cbb6e9f2ec25afd581f0319973c206dc617b9d42daa`  
		Last Modified: Tue, 28 Apr 2020 01:55:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf457681dfd85539a9068ef8c86dab67250c1a52a53dd9cddcc8308d886a384`  
		Last Modified: Tue, 28 Apr 2020 01:55:14 GMT  
		Size: 64.2 MB (64195377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0a8ff4a16b33c280909d33b99836a9a88ab7170401bd67637888068cd54aa3`  
		Last Modified: Tue, 28 Apr 2020 01:55:03 GMT  
		Size: 5.1 KB (5148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161b9a3ea21688f4c5a01f4bdc215218d376cdcabc9a538e3bd7bc9b3df9fb29`  
		Last Modified: Tue, 28 Apr 2020 01:55:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:e821ca8cc7a44d354486f30c6a193ec6b70a4eed8c8362aeede4e9b8d74b8ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:34ae988981413ec8a6bd9735bdc78bc44943bcebc2899578c9b63d65aca283e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154405308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f965319e89deaebf165f58d08b1a217971bf411e9d9860e294634b72d09ab6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:13:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:13:59 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:14:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:14:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:15:08 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Apr 2020 01:53:14 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Tue, 28 Apr 2020 01:53:15 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Apr 2020 01:53:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 28 Apr 2020 01:53:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Apr 2020 01:53:38 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Tue, 28 Apr 2020 01:53:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Apr 2020 01:53:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2020 01:53:39 GMT
EXPOSE 3306 33060
# Tue, 28 Apr 2020 01:53:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc6c614591231a51a8abf93a762208fd1aed3f72f3e3fd0b8907904e3c9a38b`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c3d959c9d9548b3c320af7856e6e16c967daf7d280ac2607e49aa2b3816dd`  
		Last Modified: Thu, 23 Apr 2020 04:17:32 GMT  
		Size: 4.2 MB (4178101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de4d0e206e076ed00d1b32a5104bcd7246484f51de192ba7d5b5c75fe215d0`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.4 MB (1419225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f0394ef4231f3e9f43809855fba117032c697e51c94defda703f34a527b43`  
		Last Modified: Thu, 23 Apr 2020 04:17:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9185034607beae95fac5ee5b684c0182fa10a66b51ba65a7e81345e860b91c2`  
		Last Modified: Thu, 23 Apr 2020 04:17:35 GMT  
		Size: 13.4 MB (13443052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a9c64dadc90a7aef7354825e9668f7b7667ad915df865cb4d05142a76938e`  
		Last Modified: Thu, 23 Apr 2020 04:17:28 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e745b33616262bd650a554bb10b60f10945f670c6e534cf8a76e84adcec60500`  
		Last Modified: Tue, 28 Apr 2020 01:54:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03145d87b451d5e545361351f6c36837d504930a1597d9372a352a49fbce4289`  
		Last Modified: Tue, 28 Apr 2020 01:54:56 GMT  
		Size: 108.3 MB (108256954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3991a6b182ee395a9d599513128506214ff9bf4fe5edd363b954e55ffc22d6b4`  
		Last Modified: Tue, 28 Apr 2020 01:54:40 GMT  
		Size: 5.1 KB (5133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62335de06f7d86c53bc2f1e07fed62cc610e11c3cb1105b2b4b90211c78f5793`  
		Last Modified: Tue, 28 Apr 2020 01:54:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.30`

```console
$ docker pull mysql@sha256:e821ca8cc7a44d354486f30c6a193ec6b70a4eed8c8362aeede4e9b8d74b8ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.30` - linux; amd64

```console
$ docker pull mysql@sha256:34ae988981413ec8a6bd9735bdc78bc44943bcebc2899578c9b63d65aca283e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154405308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f965319e89deaebf165f58d08b1a217971bf411e9d9860e294634b72d09ab6d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:13:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:13:59 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:14:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:14:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:15:08 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Apr 2020 01:53:14 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Tue, 28 Apr 2020 01:53:15 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Apr 2020 01:53:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 28 Apr 2020 01:53:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Apr 2020 01:53:38 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Tue, 28 Apr 2020 01:53:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Apr 2020 01:53:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2020 01:53:39 GMT
EXPOSE 3306 33060
# Tue, 28 Apr 2020 01:53:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc6c614591231a51a8abf93a762208fd1aed3f72f3e3fd0b8907904e3c9a38b`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c3d959c9d9548b3c320af7856e6e16c967daf7d280ac2607e49aa2b3816dd`  
		Last Modified: Thu, 23 Apr 2020 04:17:32 GMT  
		Size: 4.2 MB (4178101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de4d0e206e076ed00d1b32a5104bcd7246484f51de192ba7d5b5c75fe215d0`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.4 MB (1419225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f0394ef4231f3e9f43809855fba117032c697e51c94defda703f34a527b43`  
		Last Modified: Thu, 23 Apr 2020 04:17:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9185034607beae95fac5ee5b684c0182fa10a66b51ba65a7e81345e860b91c2`  
		Last Modified: Thu, 23 Apr 2020 04:17:35 GMT  
		Size: 13.4 MB (13443052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a9c64dadc90a7aef7354825e9668f7b7667ad915df865cb4d05142a76938e`  
		Last Modified: Thu, 23 Apr 2020 04:17:28 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e745b33616262bd650a554bb10b60f10945f670c6e534cf8a76e84adcec60500`  
		Last Modified: Tue, 28 Apr 2020 01:54:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03145d87b451d5e545361351f6c36837d504930a1597d9372a352a49fbce4289`  
		Last Modified: Tue, 28 Apr 2020 01:54:56 GMT  
		Size: 108.3 MB (108256954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3991a6b182ee395a9d599513128506214ff9bf4fe5edd363b954e55ffc22d6b4`  
		Last Modified: Tue, 28 Apr 2020 01:54:40 GMT  
		Size: 5.1 KB (5133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62335de06f7d86c53bc2f1e07fed62cc610e11c3cb1105b2b4b90211c78f5793`  
		Last Modified: Tue, 28 Apr 2020 01:54:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:61a2a33f4b8b4bc93b7b6b9e65e64044aaec594809f818aeffbff69a893d1944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:573194f1cf7d39f38471d1d766c33e34582c962fa440928b5e1d47bd61796e87
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157635810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a67c95e83189d60dd24cfeb13d9f235a95a7afd7749a7d09845f303fab239c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:13:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:13:59 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:14:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:14:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:14:20 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Apr 2020 01:52:50 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Tue, 28 Apr 2020 01:52:50 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Apr 2020 01:53:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 28 Apr 2020 01:53:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Apr 2020 01:53:09 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 28 Apr 2020 01:53:09 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Tue, 28 Apr 2020 01:53:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Apr 2020 01:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2020 01:53:10 GMT
EXPOSE 3306 33060
# Tue, 28 Apr 2020 01:53:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc6c614591231a51a8abf93a762208fd1aed3f72f3e3fd0b8907904e3c9a38b`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c3d959c9d9548b3c320af7856e6e16c967daf7d280ac2607e49aa2b3816dd`  
		Last Modified: Thu, 23 Apr 2020 04:17:32 GMT  
		Size: 4.2 MB (4178101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de4d0e206e076ed00d1b32a5104bcd7246484f51de192ba7d5b5c75fe215d0`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.4 MB (1419225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f0394ef4231f3e9f43809855fba117032c697e51c94defda703f34a527b43`  
		Last Modified: Thu, 23 Apr 2020 04:17:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9185034607beae95fac5ee5b684c0182fa10a66b51ba65a7e81345e860b91c2`  
		Last Modified: Thu, 23 Apr 2020 04:17:35 GMT  
		Size: 13.4 MB (13443052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a9c64dadc90a7aef7354825e9668f7b7667ad915df865cb4d05142a76938e`  
		Last Modified: Thu, 23 Apr 2020 04:17:28 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f3f7d109035cce30a39f649d976094f35d62bab86d9022bf7ad5b0377f3e6e`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a3851d920765a0bae87d8082006dfef2ed0297b15e2f3f30ca3d381f720cfc`  
		Last Modified: Tue, 28 Apr 2020 01:54:34 GMT  
		Size: 111.5 MB (111486559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a1cc65c182016d748532a12a585dd50a6ba28e757515d898c49c9d24cf0604`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a6b01efa55d0be5d85b7c73ba733e1d2f882448308b4670e4b6d1485f3af29`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca5ce71f9eab99a9eb65248503adcb7c3dd9e49c7d713b7679440135b5a1660`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:61a2a33f4b8b4bc93b7b6b9e65e64044aaec594809f818aeffbff69a893d1944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:573194f1cf7d39f38471d1d766c33e34582c962fa440928b5e1d47bd61796e87
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157635810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a67c95e83189d60dd24cfeb13d9f235a95a7afd7749a7d09845f303fab239c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:13:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:13:59 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:14:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:14:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:14:20 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Apr 2020 01:52:50 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Tue, 28 Apr 2020 01:52:50 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Apr 2020 01:53:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 28 Apr 2020 01:53:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Apr 2020 01:53:09 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 28 Apr 2020 01:53:09 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Tue, 28 Apr 2020 01:53:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Apr 2020 01:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2020 01:53:10 GMT
EXPOSE 3306 33060
# Tue, 28 Apr 2020 01:53:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc6c614591231a51a8abf93a762208fd1aed3f72f3e3fd0b8907904e3c9a38b`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c3d959c9d9548b3c320af7856e6e16c967daf7d280ac2607e49aa2b3816dd`  
		Last Modified: Thu, 23 Apr 2020 04:17:32 GMT  
		Size: 4.2 MB (4178101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de4d0e206e076ed00d1b32a5104bcd7246484f51de192ba7d5b5c75fe215d0`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.4 MB (1419225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f0394ef4231f3e9f43809855fba117032c697e51c94defda703f34a527b43`  
		Last Modified: Thu, 23 Apr 2020 04:17:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9185034607beae95fac5ee5b684c0182fa10a66b51ba65a7e81345e860b91c2`  
		Last Modified: Thu, 23 Apr 2020 04:17:35 GMT  
		Size: 13.4 MB (13443052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a9c64dadc90a7aef7354825e9668f7b7667ad915df865cb4d05142a76938e`  
		Last Modified: Thu, 23 Apr 2020 04:17:28 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f3f7d109035cce30a39f649d976094f35d62bab86d9022bf7ad5b0377f3e6e`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a3851d920765a0bae87d8082006dfef2ed0297b15e2f3f30ca3d381f720cfc`  
		Last Modified: Tue, 28 Apr 2020 01:54:34 GMT  
		Size: 111.5 MB (111486559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a1cc65c182016d748532a12a585dd50a6ba28e757515d898c49c9d24cf0604`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a6b01efa55d0be5d85b7c73ba733e1d2f882448308b4670e4b6d1485f3af29`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca5ce71f9eab99a9eb65248503adcb7c3dd9e49c7d713b7679440135b5a1660`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.20`

```console
$ docker pull mysql@sha256:61a2a33f4b8b4bc93b7b6b9e65e64044aaec594809f818aeffbff69a893d1944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.20` - linux; amd64

```console
$ docker pull mysql@sha256:573194f1cf7d39f38471d1d766c33e34582c962fa440928b5e1d47bd61796e87
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157635810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a67c95e83189d60dd24cfeb13d9f235a95a7afd7749a7d09845f303fab239c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:13:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:13:59 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:14:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:14:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:14:20 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Apr 2020 01:52:50 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Tue, 28 Apr 2020 01:52:50 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Apr 2020 01:53:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 28 Apr 2020 01:53:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Apr 2020 01:53:09 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 28 Apr 2020 01:53:09 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Tue, 28 Apr 2020 01:53:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Apr 2020 01:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2020 01:53:10 GMT
EXPOSE 3306 33060
# Tue, 28 Apr 2020 01:53:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc6c614591231a51a8abf93a762208fd1aed3f72f3e3fd0b8907904e3c9a38b`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c3d959c9d9548b3c320af7856e6e16c967daf7d280ac2607e49aa2b3816dd`  
		Last Modified: Thu, 23 Apr 2020 04:17:32 GMT  
		Size: 4.2 MB (4178101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de4d0e206e076ed00d1b32a5104bcd7246484f51de192ba7d5b5c75fe215d0`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.4 MB (1419225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f0394ef4231f3e9f43809855fba117032c697e51c94defda703f34a527b43`  
		Last Modified: Thu, 23 Apr 2020 04:17:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9185034607beae95fac5ee5b684c0182fa10a66b51ba65a7e81345e860b91c2`  
		Last Modified: Thu, 23 Apr 2020 04:17:35 GMT  
		Size: 13.4 MB (13443052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a9c64dadc90a7aef7354825e9668f7b7667ad915df865cb4d05142a76938e`  
		Last Modified: Thu, 23 Apr 2020 04:17:28 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f3f7d109035cce30a39f649d976094f35d62bab86d9022bf7ad5b0377f3e6e`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a3851d920765a0bae87d8082006dfef2ed0297b15e2f3f30ca3d381f720cfc`  
		Last Modified: Tue, 28 Apr 2020 01:54:34 GMT  
		Size: 111.5 MB (111486559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a1cc65c182016d748532a12a585dd50a6ba28e757515d898c49c9d24cf0604`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a6b01efa55d0be5d85b7c73ba733e1d2f882448308b4670e4b6d1485f3af29`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca5ce71f9eab99a9eb65248503adcb7c3dd9e49c7d713b7679440135b5a1660`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:61a2a33f4b8b4bc93b7b6b9e65e64044aaec594809f818aeffbff69a893d1944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:573194f1cf7d39f38471d1d766c33e34582c962fa440928b5e1d47bd61796e87
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157635810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a67c95e83189d60dd24cfeb13d9f235a95a7afd7749a7d09845f303fab239c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:13:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Apr 2020 04:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:13:59 GMT
ENV GOSU_VERSION=1.12
# Thu, 23 Apr 2020 04:14:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Apr 2020 04:14:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 04:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 23 Apr 2020 04:14:20 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Apr 2020 01:52:50 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Tue, 28 Apr 2020 01:52:50 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Apr 2020 01:53:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 28 Apr 2020 01:53:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Apr 2020 01:53:09 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 28 Apr 2020 01:53:09 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Tue, 28 Apr 2020 01:53:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Apr 2020 01:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2020 01:53:10 GMT
EXPOSE 3306 33060
# Tue, 28 Apr 2020 01:53:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc6c614591231a51a8abf93a762208fd1aed3f72f3e3fd0b8907904e3c9a38b`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c3d959c9d9548b3c320af7856e6e16c967daf7d280ac2607e49aa2b3816dd`  
		Last Modified: Thu, 23 Apr 2020 04:17:32 GMT  
		Size: 4.2 MB (4178101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de4d0e206e076ed00d1b32a5104bcd7246484f51de192ba7d5b5c75fe215d0`  
		Last Modified: Thu, 23 Apr 2020 04:17:30 GMT  
		Size: 1.4 MB (1419225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f0394ef4231f3e9f43809855fba117032c697e51c94defda703f34a527b43`  
		Last Modified: Thu, 23 Apr 2020 04:17:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9185034607beae95fac5ee5b684c0182fa10a66b51ba65a7e81345e860b91c2`  
		Last Modified: Thu, 23 Apr 2020 04:17:35 GMT  
		Size: 13.4 MB (13443052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a9c64dadc90a7aef7354825e9668f7b7667ad915df865cb4d05142a76938e`  
		Last Modified: Thu, 23 Apr 2020 04:17:28 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f3f7d109035cce30a39f649d976094f35d62bab86d9022bf7ad5b0377f3e6e`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a3851d920765a0bae87d8082006dfef2ed0297b15e2f3f30ca3d381f720cfc`  
		Last Modified: Tue, 28 Apr 2020 01:54:34 GMT  
		Size: 111.5 MB (111486559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a1cc65c182016d748532a12a585dd50a6ba28e757515d898c49c9d24cf0604`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a6b01efa55d0be5d85b7c73ba733e1d2f882448308b4670e4b6d1485f3af29`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca5ce71f9eab99a9eb65248503adcb7c3dd9e49c7d713b7679440135b5a1660`  
		Last Modified: Tue, 28 Apr 2020 01:54:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
