<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.37`](#mysql5737)
-	[`mysql:5.7.37-debian`](#mysql5737-debian)
-	[`mysql:5.7.37-oracle`](#mysql5737-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.28`](#mysql8028)
-	[`mysql:8.0.28-debian`](#mysql8028-debian)
-	[`mysql:8.0.28-oracle`](#mysql8028-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:151ecb87a07404f2c2588464e86381bdf74795c6d24090f9c50bc8e947a57797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:1520c2db1591b37fc7f2c0bc72b4e0a002afed6fcc2397f7bcd2bbdff490c930
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155418011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d2d47667cf062cc9e70c31b9322fafc527ed61806f32f48d8797a0e1488ac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 20 Apr 2022 10:05:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:39 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:39 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291c7612f7a8b5fd8feb6101f3a75ce0b3f7defc3f68b667d211a879d6cf0d89`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc84226e0b0ca7a955eea02187200d31feb8727db2c7c34a3ea0d9bc2ee814`  
		Last Modified: Wed, 20 Apr 2022 10:07:13 GMT  
		Size: 108.6 MB (108637145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81340df4a52ccf60343f023e99b7a69e3820e7552bd8dfbbcd9198edd21a9df1`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 5.1 KB (5132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec63f52b870c5b816a615abf5592cf5798326dd932ef2b01d6efd222f064d5`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:151ecb87a07404f2c2588464e86381bdf74795c6d24090f9c50bc8e947a57797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:1520c2db1591b37fc7f2c0bc72b4e0a002afed6fcc2397f7bcd2bbdff490c930
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155418011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d2d47667cf062cc9e70c31b9322fafc527ed61806f32f48d8797a0e1488ac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 20 Apr 2022 10:05:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:39 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:39 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291c7612f7a8b5fd8feb6101f3a75ce0b3f7defc3f68b667d211a879d6cf0d89`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc84226e0b0ca7a955eea02187200d31feb8727db2c7c34a3ea0d9bc2ee814`  
		Last Modified: Wed, 20 Apr 2022 10:07:13 GMT  
		Size: 108.6 MB (108637145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81340df4a52ccf60343f023e99b7a69e3820e7552bd8dfbbcd9198edd21a9df1`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 5.1 KB (5132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec63f52b870c5b816a615abf5592cf5798326dd932ef2b01d6efd222f064d5`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:bafce326af2e71c855dc0df3121049e6b1182e7f9098d5c9ae4e4b4612943650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1e755fd5ab6cd782256827067603dbef93493c4a91bbb88d51362dbf1f57e8b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125246919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca04d328ed5ac0823dd3252bdf8432e49da9fdf36631d6850ddcf1284a8bbdee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:12:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:12:23 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:12:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:12:36 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 31 Mar 2022 02:12:37 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Thu, 31 Mar 2022 02:12:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 31 Mar 2022 02:12:52 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 31 Mar 2022 02:12:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 31 Mar 2022 02:12:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Thu, 31 Mar 2022 02:13:10 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 31 Mar 2022 02:13:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 31 Mar 2022 02:13:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 31 Mar 2022 02:13:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:13:11 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:13:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1268f9b69b4d2dfc0086f5426266fd97bb99c37e0dc2db707e3e7a5667bba3c`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1084d021338c13d9afc0d3fa5ab8ff753ddd7d97abc2a81074b6fff0807a96`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ad34fb0ede94774c93b333cbdc752915f8d0b45eda981588615248b8fbad9e`  
		Last Modified: Thu, 31 Mar 2022 02:14:12 GMT  
		Size: 3.8 MB (3755164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341499385aec2522efd754b4ba03c458add9de6802a7834b941209fb793dc0f`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31c594d2051139e02d66cb9398ff3c5a88a0028582d910412000794e0bdf8cb`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10402a7aeb1ec24fc39bb20fb660442e97663d31323f62ef129df564b2028e0a`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 25.5 MB (25471062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb1127c3ae153f55defbf50395e6dfccffdf83d2ced9935588799d02e261632`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c376f51d5a2e25c8a3858cb731885b73c177d96433a1e9a591d757ebbb61f3c7`  
		Last Modified: Thu, 31 Mar 2022 02:14:18 GMT  
		Size: 46.3 MB (46323475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144aebf1e30feeda4a8dcd3e7abbab3bc10d0fbe37018acf6d4ff6f0c67742c7`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:151ecb87a07404f2c2588464e86381bdf74795c6d24090f9c50bc8e947a57797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:1520c2db1591b37fc7f2c0bc72b4e0a002afed6fcc2397f7bcd2bbdff490c930
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155418011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d2d47667cf062cc9e70c31b9322fafc527ed61806f32f48d8797a0e1488ac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 20 Apr 2022 10:05:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:39 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:39 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291c7612f7a8b5fd8feb6101f3a75ce0b3f7defc3f68b667d211a879d6cf0d89`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc84226e0b0ca7a955eea02187200d31feb8727db2c7c34a3ea0d9bc2ee814`  
		Last Modified: Wed, 20 Apr 2022 10:07:13 GMT  
		Size: 108.6 MB (108637145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81340df4a52ccf60343f023e99b7a69e3820e7552bd8dfbbcd9198edd21a9df1`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 5.1 KB (5132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec63f52b870c5b816a615abf5592cf5798326dd932ef2b01d6efd222f064d5`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:151ecb87a07404f2c2588464e86381bdf74795c6d24090f9c50bc8e947a57797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:1520c2db1591b37fc7f2c0bc72b4e0a002afed6fcc2397f7bcd2bbdff490c930
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155418011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d2d47667cf062cc9e70c31b9322fafc527ed61806f32f48d8797a0e1488ac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 20 Apr 2022 10:05:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:39 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:39 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291c7612f7a8b5fd8feb6101f3a75ce0b3f7defc3f68b667d211a879d6cf0d89`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc84226e0b0ca7a955eea02187200d31feb8727db2c7c34a3ea0d9bc2ee814`  
		Last Modified: Wed, 20 Apr 2022 10:07:13 GMT  
		Size: 108.6 MB (108637145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81340df4a52ccf60343f023e99b7a69e3820e7552bd8dfbbcd9198edd21a9df1`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 5.1 KB (5132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec63f52b870c5b816a615abf5592cf5798326dd932ef2b01d6efd222f064d5`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:bafce326af2e71c855dc0df3121049e6b1182e7f9098d5c9ae4e4b4612943650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1e755fd5ab6cd782256827067603dbef93493c4a91bbb88d51362dbf1f57e8b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125246919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca04d328ed5ac0823dd3252bdf8432e49da9fdf36631d6850ddcf1284a8bbdee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:12:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:12:23 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:12:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:12:36 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 31 Mar 2022 02:12:37 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Thu, 31 Mar 2022 02:12:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 31 Mar 2022 02:12:52 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 31 Mar 2022 02:12:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 31 Mar 2022 02:12:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Thu, 31 Mar 2022 02:13:10 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 31 Mar 2022 02:13:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 31 Mar 2022 02:13:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 31 Mar 2022 02:13:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:13:11 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:13:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1268f9b69b4d2dfc0086f5426266fd97bb99c37e0dc2db707e3e7a5667bba3c`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1084d021338c13d9afc0d3fa5ab8ff753ddd7d97abc2a81074b6fff0807a96`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ad34fb0ede94774c93b333cbdc752915f8d0b45eda981588615248b8fbad9e`  
		Last Modified: Thu, 31 Mar 2022 02:14:12 GMT  
		Size: 3.8 MB (3755164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341499385aec2522efd754b4ba03c458add9de6802a7834b941209fb793dc0f`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31c594d2051139e02d66cb9398ff3c5a88a0028582d910412000794e0bdf8cb`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10402a7aeb1ec24fc39bb20fb660442e97663d31323f62ef129df564b2028e0a`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 25.5 MB (25471062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb1127c3ae153f55defbf50395e6dfccffdf83d2ced9935588799d02e261632`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c376f51d5a2e25c8a3858cb731885b73c177d96433a1e9a591d757ebbb61f3c7`  
		Last Modified: Thu, 31 Mar 2022 02:14:18 GMT  
		Size: 46.3 MB (46323475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144aebf1e30feeda4a8dcd3e7abbab3bc10d0fbe37018acf6d4ff6f0c67742c7`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37`

```console
$ docker pull mysql@sha256:151ecb87a07404f2c2588464e86381bdf74795c6d24090f9c50bc8e947a57797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37` - linux; amd64

```console
$ docker pull mysql@sha256:1520c2db1591b37fc7f2c0bc72b4e0a002afed6fcc2397f7bcd2bbdff490c930
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155418011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d2d47667cf062cc9e70c31b9322fafc527ed61806f32f48d8797a0e1488ac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 20 Apr 2022 10:05:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:39 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:39 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291c7612f7a8b5fd8feb6101f3a75ce0b3f7defc3f68b667d211a879d6cf0d89`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc84226e0b0ca7a955eea02187200d31feb8727db2c7c34a3ea0d9bc2ee814`  
		Last Modified: Wed, 20 Apr 2022 10:07:13 GMT  
		Size: 108.6 MB (108637145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81340df4a52ccf60343f023e99b7a69e3820e7552bd8dfbbcd9198edd21a9df1`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 5.1 KB (5132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec63f52b870c5b816a615abf5592cf5798326dd932ef2b01d6efd222f064d5`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-debian`

```console
$ docker pull mysql@sha256:151ecb87a07404f2c2588464e86381bdf74795c6d24090f9c50bc8e947a57797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:1520c2db1591b37fc7f2c0bc72b4e0a002afed6fcc2397f7bcd2bbdff490c930
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155418011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d2d47667cf062cc9e70c31b9322fafc527ed61806f32f48d8797a0e1488ac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 20 Apr 2022 10:05:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:39 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:39 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291c7612f7a8b5fd8feb6101f3a75ce0b3f7defc3f68b667d211a879d6cf0d89`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc84226e0b0ca7a955eea02187200d31feb8727db2c7c34a3ea0d9bc2ee814`  
		Last Modified: Wed, 20 Apr 2022 10:07:13 GMT  
		Size: 108.6 MB (108637145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81340df4a52ccf60343f023e99b7a69e3820e7552bd8dfbbcd9198edd21a9df1`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 5.1 KB (5132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec63f52b870c5b816a615abf5592cf5798326dd932ef2b01d6efd222f064d5`  
		Last Modified: Wed, 20 Apr 2022 10:06:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-oracle`

```console
$ docker pull mysql@sha256:bafce326af2e71c855dc0df3121049e6b1182e7f9098d5c9ae4e4b4612943650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1e755fd5ab6cd782256827067603dbef93493c4a91bbb88d51362dbf1f57e8b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125246919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca04d328ed5ac0823dd3252bdf8432e49da9fdf36631d6850ddcf1284a8bbdee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:12:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:12:23 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:12:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:12:36 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 31 Mar 2022 02:12:37 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Thu, 31 Mar 2022 02:12:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 31 Mar 2022 02:12:52 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 31 Mar 2022 02:12:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 31 Mar 2022 02:12:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Thu, 31 Mar 2022 02:13:10 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 31 Mar 2022 02:13:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 31 Mar 2022 02:13:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 31 Mar 2022 02:13:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:13:11 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:13:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1268f9b69b4d2dfc0086f5426266fd97bb99c37e0dc2db707e3e7a5667bba3c`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1084d021338c13d9afc0d3fa5ab8ff753ddd7d97abc2a81074b6fff0807a96`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ad34fb0ede94774c93b333cbdc752915f8d0b45eda981588615248b8fbad9e`  
		Last Modified: Thu, 31 Mar 2022 02:14:12 GMT  
		Size: 3.8 MB (3755164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341499385aec2522efd754b4ba03c458add9de6802a7834b941209fb793dc0f`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31c594d2051139e02d66cb9398ff3c5a88a0028582d910412000794e0bdf8cb`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10402a7aeb1ec24fc39bb20fb660442e97663d31323f62ef129df564b2028e0a`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 25.5 MB (25471062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb1127c3ae153f55defbf50395e6dfccffdf83d2ced9935588799d02e261632`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c376f51d5a2e25c8a3858cb731885b73c177d96433a1e9a591d757ebbb61f3c7`  
		Last Modified: Thu, 31 Mar 2022 02:14:18 GMT  
		Size: 46.3 MB (46323475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144aebf1e30feeda4a8dcd3e7abbab3bc10d0fbe37018acf6d4ff6f0c67742c7`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:fc77d54cacef90ad3d75964837fad0f2a9a368b69e7d799665a3f4e90e600c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:e9fee3e714fd69cd2ccfa0c6a141fac0a60f2a02f72d43c0e7055601aaf481b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154586725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9f23df82a3e5efabd1574b862a94c0657c73a6179efec07d5cf9ae5a307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 20 Apr 2022 10:04:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Apr 2022 10:05:08 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:08 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654aa78d12d6394284595971c9c2def73c48b58ed70ca2765fd738766f959eb7`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1a07a253d4c7cfa839c93e5be7f0ba6112ab55dc6293c0b32fa434df05803`  
		Last Modified: Wed, 20 Apr 2022 10:06:23 GMT  
		Size: 107.8 MB (107805015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32905dc9e58b246414b41a053d048bdc4e50eec1622ed5712a6a855bce811a9`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d41026e4402a612b991b4b3f98ea0f40aa8cb85a610261ed5409174b801c2`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e0f73ebe3204c8da1391c8439d7fb5474569556972fa43583060abec3f7a9b`  
		Last Modified: Wed, 20 Apr 2022 10:06:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:fc77d54cacef90ad3d75964837fad0f2a9a368b69e7d799665a3f4e90e600c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e9fee3e714fd69cd2ccfa0c6a141fac0a60f2a02f72d43c0e7055601aaf481b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154586725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9f23df82a3e5efabd1574b862a94c0657c73a6179efec07d5cf9ae5a307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 20 Apr 2022 10:04:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Apr 2022 10:05:08 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:08 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654aa78d12d6394284595971c9c2def73c48b58ed70ca2765fd738766f959eb7`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1a07a253d4c7cfa839c93e5be7f0ba6112ab55dc6293c0b32fa434df05803`  
		Last Modified: Wed, 20 Apr 2022 10:06:23 GMT  
		Size: 107.8 MB (107805015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32905dc9e58b246414b41a053d048bdc4e50eec1622ed5712a6a855bce811a9`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d41026e4402a612b991b4b3f98ea0f40aa8cb85a610261ed5409174b801c2`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e0f73ebe3204c8da1391c8439d7fb5474569556972fa43583060abec3f7a9b`  
		Last Modified: Wed, 20 Apr 2022 10:06:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:041a3f0b3d58771afc64762b46289385f2b9126a14ab7b5895e83b87fd26f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:39b3c2650e24da10a4cb31f589e4e4aff70f2f732283ccd05390781e19cec5e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133160323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca4d64ca8783b3263c6bd28f186b4b909b01afa6c06b4a0ce41cc693d0b2ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:47 GMT
ADD file:eaa532cad071c531a759e73fd0fd381f440f180ab45b05a74314f10b0374df67 in / 
# Tue, 29 Mar 2022 18:35:47 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:10:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:10:42 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:11:06 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 31 Mar 2022 02:11:07 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:11:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 31 Mar 2022 02:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 31 Mar 2022 02:11:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 31 Mar 2022 02:11:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:12:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 31 Mar 2022 02:12:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 31 Mar 2022 02:12:06 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 31 Mar 2022 02:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:12:06 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4430e06691f65e516df7d62db0ee5393acea9ade644cc6bc620efef0956dd17`  
		Last Modified: Tue, 29 Mar 2022 18:36:53 GMT  
		Size: 42.1 MB (42113609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99677fe408e062a57b32fb00d5ff00e4eab318db52b12da3c7a4dbedf9ad6244`  
		Last Modified: Thu, 31 Mar 2022 02:13:48 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911aa3c638bfef7796ef2177249b0d29ad0e6fdada580629689c49a92f2fb602`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 928.8 KB (928834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a50ae0f36756838cc7b35ef9bfe9c1e123fd92120fa773506ba4a5dc44c35f2`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 4.6 MB (4556552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e229cecb99fa4470f4b33d9c67dac8ec41c198b819f86b61f33239a56b07602`  
		Last Modified: Thu, 31 Mar 2022 02:13:45 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1790c22e04b08b7c8530b41dc5c1ae59f6bc59768164ec87cbf824042841602`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99e6dd61db9fba984084bd6bb56accf425a248ef7f296e8a852caca0aa863d3`  
		Last Modified: Thu, 31 Mar 2022 02:13:51 GMT  
		Size: 47.3 MB (47274212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb6c638025985d50b50df0eae62d65fa7b642cf514cfabca51641e862347de`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc8a66483d763edfb9ee13132e5bb5b6bbddff5a3cf58c6a88f00c9ac202eb`  
		Last Modified: Thu, 31 Mar 2022 02:13:50 GMT  
		Size: 38.3 MB (38277617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52190d1e6a3f83f9986a3a56ea49a2353f1dd7844356abef3c48c024069d4daa`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a84c40eb932fc324b1232320a83a91bdd0e25292400e44690c956fc036a5826
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141174013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3f4a2767a37c46e2f5424f1f0e8e79ace6fad52400c3220a6b7f7092b52aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 19:36:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 30 Mar 2022 19:36:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 30 Mar 2022 19:36:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 30 Mar 2022 19:36:52 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 30 Mar 2022 19:36:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 30 Mar 2022 19:36:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 30 Mar 2022 19:36:56 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:36:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 30 Mar 2022 19:37:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 30 Mar 2022 19:37:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 30 Mar 2022 19:37:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:37:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 30 Mar 2022 19:37:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 30 Mar 2022 19:37:52 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 30 Mar 2022 19:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 19:37:53 GMT
EXPOSE 3306 33060
# Wed, 30 Mar 2022 19:37:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab860100fd06bf966bba43e945a81bc929141ededd09d9ac425c6f84f6e3e03`  
		Last Modified: Wed, 30 Mar 2022 19:38:24 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beca8ba6c49cf952f7d2a549637ac71b887bba93a5e30f8e8cf1858369fb67d`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c660f342d4fc90e2cae9584677828102e44965aac6e26780916a1e8ef2ff18ee`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 4.4 MB (4378770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ff8141a9459038f2bc38cd3ded605c6f405d4daf7d56cf6b4f52dd9a2cb5dd`  
		Last Modified: Wed, 30 Mar 2022 19:38:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de35ab51f9a083208854e695dc8879ecf7b9820ef90d9c2c356219ba2651fc`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fd10c0fb45dc51fe4815d510ad7c71fef44e80dd9393308f7ad1a475c465c`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 53.4 MB (53429900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42744cc7790693010c1abb7779bc759b995d9e50d8904bd37afebaf941dcf12b`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cc9d0d65fd6d9afa6e8bcca9941cd6fdaab5a37ee45ce68ea4def7528d673a`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 40.5 MB (40479681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f188c7be958b84ecc16d325c13dd32543ff1e126d9fe14bec3b8397ec173c`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:fc77d54cacef90ad3d75964837fad0f2a9a368b69e7d799665a3f4e90e600c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:e9fee3e714fd69cd2ccfa0c6a141fac0a60f2a02f72d43c0e7055601aaf481b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154586725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9f23df82a3e5efabd1574b862a94c0657c73a6179efec07d5cf9ae5a307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 20 Apr 2022 10:04:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Apr 2022 10:05:08 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:08 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654aa78d12d6394284595971c9c2def73c48b58ed70ca2765fd738766f959eb7`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1a07a253d4c7cfa839c93e5be7f0ba6112ab55dc6293c0b32fa434df05803`  
		Last Modified: Wed, 20 Apr 2022 10:06:23 GMT  
		Size: 107.8 MB (107805015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32905dc9e58b246414b41a053d048bdc4e50eec1622ed5712a6a855bce811a9`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d41026e4402a612b991b4b3f98ea0f40aa8cb85a610261ed5409174b801c2`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e0f73ebe3204c8da1391c8439d7fb5474569556972fa43583060abec3f7a9b`  
		Last Modified: Wed, 20 Apr 2022 10:06:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:fc77d54cacef90ad3d75964837fad0f2a9a368b69e7d799665a3f4e90e600c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e9fee3e714fd69cd2ccfa0c6a141fac0a60f2a02f72d43c0e7055601aaf481b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154586725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9f23df82a3e5efabd1574b862a94c0657c73a6179efec07d5cf9ae5a307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 20 Apr 2022 10:04:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Apr 2022 10:05:08 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:08 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654aa78d12d6394284595971c9c2def73c48b58ed70ca2765fd738766f959eb7`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1a07a253d4c7cfa839c93e5be7f0ba6112ab55dc6293c0b32fa434df05803`  
		Last Modified: Wed, 20 Apr 2022 10:06:23 GMT  
		Size: 107.8 MB (107805015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32905dc9e58b246414b41a053d048bdc4e50eec1622ed5712a6a855bce811a9`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d41026e4402a612b991b4b3f98ea0f40aa8cb85a610261ed5409174b801c2`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e0f73ebe3204c8da1391c8439d7fb5474569556972fa43583060abec3f7a9b`  
		Last Modified: Wed, 20 Apr 2022 10:06:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:041a3f0b3d58771afc64762b46289385f2b9126a14ab7b5895e83b87fd26f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:39b3c2650e24da10a4cb31f589e4e4aff70f2f732283ccd05390781e19cec5e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133160323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca4d64ca8783b3263c6bd28f186b4b909b01afa6c06b4a0ce41cc693d0b2ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:47 GMT
ADD file:eaa532cad071c531a759e73fd0fd381f440f180ab45b05a74314f10b0374df67 in / 
# Tue, 29 Mar 2022 18:35:47 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:10:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:10:42 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:11:06 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 31 Mar 2022 02:11:07 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:11:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 31 Mar 2022 02:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 31 Mar 2022 02:11:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 31 Mar 2022 02:11:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:12:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 31 Mar 2022 02:12:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 31 Mar 2022 02:12:06 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 31 Mar 2022 02:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:12:06 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4430e06691f65e516df7d62db0ee5393acea9ade644cc6bc620efef0956dd17`  
		Last Modified: Tue, 29 Mar 2022 18:36:53 GMT  
		Size: 42.1 MB (42113609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99677fe408e062a57b32fb00d5ff00e4eab318db52b12da3c7a4dbedf9ad6244`  
		Last Modified: Thu, 31 Mar 2022 02:13:48 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911aa3c638bfef7796ef2177249b0d29ad0e6fdada580629689c49a92f2fb602`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 928.8 KB (928834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a50ae0f36756838cc7b35ef9bfe9c1e123fd92120fa773506ba4a5dc44c35f2`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 4.6 MB (4556552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e229cecb99fa4470f4b33d9c67dac8ec41c198b819f86b61f33239a56b07602`  
		Last Modified: Thu, 31 Mar 2022 02:13:45 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1790c22e04b08b7c8530b41dc5c1ae59f6bc59768164ec87cbf824042841602`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99e6dd61db9fba984084bd6bb56accf425a248ef7f296e8a852caca0aa863d3`  
		Last Modified: Thu, 31 Mar 2022 02:13:51 GMT  
		Size: 47.3 MB (47274212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb6c638025985d50b50df0eae62d65fa7b642cf514cfabca51641e862347de`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc8a66483d763edfb9ee13132e5bb5b6bbddff5a3cf58c6a88f00c9ac202eb`  
		Last Modified: Thu, 31 Mar 2022 02:13:50 GMT  
		Size: 38.3 MB (38277617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52190d1e6a3f83f9986a3a56ea49a2353f1dd7844356abef3c48c024069d4daa`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a84c40eb932fc324b1232320a83a91bdd0e25292400e44690c956fc036a5826
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141174013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3f4a2767a37c46e2f5424f1f0e8e79ace6fad52400c3220a6b7f7092b52aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 19:36:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 30 Mar 2022 19:36:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 30 Mar 2022 19:36:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 30 Mar 2022 19:36:52 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 30 Mar 2022 19:36:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 30 Mar 2022 19:36:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 30 Mar 2022 19:36:56 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:36:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 30 Mar 2022 19:37:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 30 Mar 2022 19:37:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 30 Mar 2022 19:37:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:37:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 30 Mar 2022 19:37:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 30 Mar 2022 19:37:52 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 30 Mar 2022 19:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 19:37:53 GMT
EXPOSE 3306 33060
# Wed, 30 Mar 2022 19:37:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab860100fd06bf966bba43e945a81bc929141ededd09d9ac425c6f84f6e3e03`  
		Last Modified: Wed, 30 Mar 2022 19:38:24 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beca8ba6c49cf952f7d2a549637ac71b887bba93a5e30f8e8cf1858369fb67d`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c660f342d4fc90e2cae9584677828102e44965aac6e26780916a1e8ef2ff18ee`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 4.4 MB (4378770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ff8141a9459038f2bc38cd3ded605c6f405d4daf7d56cf6b4f52dd9a2cb5dd`  
		Last Modified: Wed, 30 Mar 2022 19:38:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de35ab51f9a083208854e695dc8879ecf7b9820ef90d9c2c356219ba2651fc`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fd10c0fb45dc51fe4815d510ad7c71fef44e80dd9393308f7ad1a475c465c`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 53.4 MB (53429900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42744cc7790693010c1abb7779bc759b995d9e50d8904bd37afebaf941dcf12b`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cc9d0d65fd6d9afa6e8bcca9941cd6fdaab5a37ee45ce68ea4def7528d673a`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 40.5 MB (40479681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f188c7be958b84ecc16d325c13dd32543ff1e126d9fe14bec3b8397ec173c`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28`

```console
$ docker pull mysql@sha256:fc77d54cacef90ad3d75964837fad0f2a9a368b69e7d799665a3f4e90e600c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28` - linux; amd64

```console
$ docker pull mysql@sha256:e9fee3e714fd69cd2ccfa0c6a141fac0a60f2a02f72d43c0e7055601aaf481b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154586725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9f23df82a3e5efabd1574b862a94c0657c73a6179efec07d5cf9ae5a307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 20 Apr 2022 10:04:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Apr 2022 10:05:08 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:08 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654aa78d12d6394284595971c9c2def73c48b58ed70ca2765fd738766f959eb7`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1a07a253d4c7cfa839c93e5be7f0ba6112ab55dc6293c0b32fa434df05803`  
		Last Modified: Wed, 20 Apr 2022 10:06:23 GMT  
		Size: 107.8 MB (107805015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32905dc9e58b246414b41a053d048bdc4e50eec1622ed5712a6a855bce811a9`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d41026e4402a612b991b4b3f98ea0f40aa8cb85a610261ed5409174b801c2`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e0f73ebe3204c8da1391c8439d7fb5474569556972fa43583060abec3f7a9b`  
		Last Modified: Wed, 20 Apr 2022 10:06:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-debian`

```console
$ docker pull mysql@sha256:fc77d54cacef90ad3d75964837fad0f2a9a368b69e7d799665a3f4e90e600c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e9fee3e714fd69cd2ccfa0c6a141fac0a60f2a02f72d43c0e7055601aaf481b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154586725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9f23df82a3e5efabd1574b862a94c0657c73a6179efec07d5cf9ae5a307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 20 Apr 2022 10:04:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Apr 2022 10:05:08 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:08 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654aa78d12d6394284595971c9c2def73c48b58ed70ca2765fd738766f959eb7`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1a07a253d4c7cfa839c93e5be7f0ba6112ab55dc6293c0b32fa434df05803`  
		Last Modified: Wed, 20 Apr 2022 10:06:23 GMT  
		Size: 107.8 MB (107805015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32905dc9e58b246414b41a053d048bdc4e50eec1622ed5712a6a855bce811a9`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d41026e4402a612b991b4b3f98ea0f40aa8cb85a610261ed5409174b801c2`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e0f73ebe3204c8da1391c8439d7fb5474569556972fa43583060abec3f7a9b`  
		Last Modified: Wed, 20 Apr 2022 10:06:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-oracle`

```console
$ docker pull mysql@sha256:041a3f0b3d58771afc64762b46289385f2b9126a14ab7b5895e83b87fd26f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.28-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:39b3c2650e24da10a4cb31f589e4e4aff70f2f732283ccd05390781e19cec5e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133160323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca4d64ca8783b3263c6bd28f186b4b909b01afa6c06b4a0ce41cc693d0b2ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:47 GMT
ADD file:eaa532cad071c531a759e73fd0fd381f440f180ab45b05a74314f10b0374df67 in / 
# Tue, 29 Mar 2022 18:35:47 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:10:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:10:42 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:11:06 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 31 Mar 2022 02:11:07 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:11:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 31 Mar 2022 02:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 31 Mar 2022 02:11:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 31 Mar 2022 02:11:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:12:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 31 Mar 2022 02:12:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 31 Mar 2022 02:12:06 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 31 Mar 2022 02:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:12:06 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4430e06691f65e516df7d62db0ee5393acea9ade644cc6bc620efef0956dd17`  
		Last Modified: Tue, 29 Mar 2022 18:36:53 GMT  
		Size: 42.1 MB (42113609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99677fe408e062a57b32fb00d5ff00e4eab318db52b12da3c7a4dbedf9ad6244`  
		Last Modified: Thu, 31 Mar 2022 02:13:48 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911aa3c638bfef7796ef2177249b0d29ad0e6fdada580629689c49a92f2fb602`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 928.8 KB (928834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a50ae0f36756838cc7b35ef9bfe9c1e123fd92120fa773506ba4a5dc44c35f2`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 4.6 MB (4556552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e229cecb99fa4470f4b33d9c67dac8ec41c198b819f86b61f33239a56b07602`  
		Last Modified: Thu, 31 Mar 2022 02:13:45 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1790c22e04b08b7c8530b41dc5c1ae59f6bc59768164ec87cbf824042841602`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99e6dd61db9fba984084bd6bb56accf425a248ef7f296e8a852caca0aa863d3`  
		Last Modified: Thu, 31 Mar 2022 02:13:51 GMT  
		Size: 47.3 MB (47274212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb6c638025985d50b50df0eae62d65fa7b642cf514cfabca51641e862347de`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc8a66483d763edfb9ee13132e5bb5b6bbddff5a3cf58c6a88f00c9ac202eb`  
		Last Modified: Thu, 31 Mar 2022 02:13:50 GMT  
		Size: 38.3 MB (38277617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52190d1e6a3f83f9986a3a56ea49a2353f1dd7844356abef3c48c024069d4daa`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.28-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a84c40eb932fc324b1232320a83a91bdd0e25292400e44690c956fc036a5826
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141174013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3f4a2767a37c46e2f5424f1f0e8e79ace6fad52400c3220a6b7f7092b52aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 19:36:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 30 Mar 2022 19:36:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 30 Mar 2022 19:36:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 30 Mar 2022 19:36:52 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 30 Mar 2022 19:36:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 30 Mar 2022 19:36:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 30 Mar 2022 19:36:56 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:36:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 30 Mar 2022 19:37:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 30 Mar 2022 19:37:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 30 Mar 2022 19:37:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:37:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 30 Mar 2022 19:37:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 30 Mar 2022 19:37:52 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 30 Mar 2022 19:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 19:37:53 GMT
EXPOSE 3306 33060
# Wed, 30 Mar 2022 19:37:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab860100fd06bf966bba43e945a81bc929141ededd09d9ac425c6f84f6e3e03`  
		Last Modified: Wed, 30 Mar 2022 19:38:24 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beca8ba6c49cf952f7d2a549637ac71b887bba93a5e30f8e8cf1858369fb67d`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c660f342d4fc90e2cae9584677828102e44965aac6e26780916a1e8ef2ff18ee`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 4.4 MB (4378770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ff8141a9459038f2bc38cd3ded605c6f405d4daf7d56cf6b4f52dd9a2cb5dd`  
		Last Modified: Wed, 30 Mar 2022 19:38:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de35ab51f9a083208854e695dc8879ecf7b9820ef90d9c2c356219ba2651fc`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fd10c0fb45dc51fe4815d510ad7c71fef44e80dd9393308f7ad1a475c465c`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 53.4 MB (53429900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42744cc7790693010c1abb7779bc759b995d9e50d8904bd37afebaf941dcf12b`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cc9d0d65fd6d9afa6e8bcca9941cd6fdaab5a37ee45ce68ea4def7528d673a`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 40.5 MB (40479681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f188c7be958b84ecc16d325c13dd32543ff1e126d9fe14bec3b8397ec173c`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:fc77d54cacef90ad3d75964837fad0f2a9a368b69e7d799665a3f4e90e600c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:e9fee3e714fd69cd2ccfa0c6a141fac0a60f2a02f72d43c0e7055601aaf481b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154586725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9f23df82a3e5efabd1574b862a94c0657c73a6179efec07d5cf9ae5a307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 20 Apr 2022 10:04:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Apr 2022 10:05:08 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:08 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654aa78d12d6394284595971c9c2def73c48b58ed70ca2765fd738766f959eb7`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1a07a253d4c7cfa839c93e5be7f0ba6112ab55dc6293c0b32fa434df05803`  
		Last Modified: Wed, 20 Apr 2022 10:06:23 GMT  
		Size: 107.8 MB (107805015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32905dc9e58b246414b41a053d048bdc4e50eec1622ed5712a6a855bce811a9`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d41026e4402a612b991b4b3f98ea0f40aa8cb85a610261ed5409174b801c2`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e0f73ebe3204c8da1391c8439d7fb5474569556972fa43583060abec3f7a9b`  
		Last Modified: Wed, 20 Apr 2022 10:06:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:fc77d54cacef90ad3d75964837fad0f2a9a368b69e7d799665a3f4e90e600c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:e9fee3e714fd69cd2ccfa0c6a141fac0a60f2a02f72d43c0e7055601aaf481b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154586725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9f23df82a3e5efabd1574b862a94c0657c73a6179efec07d5cf9ae5a307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 20 Apr 2022 10:04:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Apr 2022 10:05:08 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:08 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654aa78d12d6394284595971c9c2def73c48b58ed70ca2765fd738766f959eb7`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1a07a253d4c7cfa839c93e5be7f0ba6112ab55dc6293c0b32fa434df05803`  
		Last Modified: Wed, 20 Apr 2022 10:06:23 GMT  
		Size: 107.8 MB (107805015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32905dc9e58b246414b41a053d048bdc4e50eec1622ed5712a6a855bce811a9`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d41026e4402a612b991b4b3f98ea0f40aa8cb85a610261ed5409174b801c2`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e0f73ebe3204c8da1391c8439d7fb5474569556972fa43583060abec3f7a9b`  
		Last Modified: Wed, 20 Apr 2022 10:06:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:041a3f0b3d58771afc64762b46289385f2b9126a14ab7b5895e83b87fd26f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:39b3c2650e24da10a4cb31f589e4e4aff70f2f732283ccd05390781e19cec5e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133160323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca4d64ca8783b3263c6bd28f186b4b909b01afa6c06b4a0ce41cc693d0b2ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:47 GMT
ADD file:eaa532cad071c531a759e73fd0fd381f440f180ab45b05a74314f10b0374df67 in / 
# Tue, 29 Mar 2022 18:35:47 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:10:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:10:42 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:11:06 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 31 Mar 2022 02:11:07 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:11:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 31 Mar 2022 02:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 31 Mar 2022 02:11:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 31 Mar 2022 02:11:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:12:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 31 Mar 2022 02:12:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 31 Mar 2022 02:12:06 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 31 Mar 2022 02:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:12:06 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4430e06691f65e516df7d62db0ee5393acea9ade644cc6bc620efef0956dd17`  
		Last Modified: Tue, 29 Mar 2022 18:36:53 GMT  
		Size: 42.1 MB (42113609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99677fe408e062a57b32fb00d5ff00e4eab318db52b12da3c7a4dbedf9ad6244`  
		Last Modified: Thu, 31 Mar 2022 02:13:48 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911aa3c638bfef7796ef2177249b0d29ad0e6fdada580629689c49a92f2fb602`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 928.8 KB (928834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a50ae0f36756838cc7b35ef9bfe9c1e123fd92120fa773506ba4a5dc44c35f2`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 4.6 MB (4556552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e229cecb99fa4470f4b33d9c67dac8ec41c198b819f86b61f33239a56b07602`  
		Last Modified: Thu, 31 Mar 2022 02:13:45 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1790c22e04b08b7c8530b41dc5c1ae59f6bc59768164ec87cbf824042841602`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99e6dd61db9fba984084bd6bb56accf425a248ef7f296e8a852caca0aa863d3`  
		Last Modified: Thu, 31 Mar 2022 02:13:51 GMT  
		Size: 47.3 MB (47274212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb6c638025985d50b50df0eae62d65fa7b642cf514cfabca51641e862347de`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc8a66483d763edfb9ee13132e5bb5b6bbddff5a3cf58c6a88f00c9ac202eb`  
		Last Modified: Thu, 31 Mar 2022 02:13:50 GMT  
		Size: 38.3 MB (38277617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52190d1e6a3f83f9986a3a56ea49a2353f1dd7844356abef3c48c024069d4daa`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a84c40eb932fc324b1232320a83a91bdd0e25292400e44690c956fc036a5826
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141174013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3f4a2767a37c46e2f5424f1f0e8e79ace6fad52400c3220a6b7f7092b52aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 19:36:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 30 Mar 2022 19:36:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 30 Mar 2022 19:36:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 30 Mar 2022 19:36:52 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 30 Mar 2022 19:36:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 30 Mar 2022 19:36:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 30 Mar 2022 19:36:56 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:36:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 30 Mar 2022 19:37:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 30 Mar 2022 19:37:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 30 Mar 2022 19:37:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:37:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 30 Mar 2022 19:37:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 30 Mar 2022 19:37:52 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 30 Mar 2022 19:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 19:37:53 GMT
EXPOSE 3306 33060
# Wed, 30 Mar 2022 19:37:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab860100fd06bf966bba43e945a81bc929141ededd09d9ac425c6f84f6e3e03`  
		Last Modified: Wed, 30 Mar 2022 19:38:24 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beca8ba6c49cf952f7d2a549637ac71b887bba93a5e30f8e8cf1858369fb67d`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c660f342d4fc90e2cae9584677828102e44965aac6e26780916a1e8ef2ff18ee`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 4.4 MB (4378770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ff8141a9459038f2bc38cd3ded605c6f405d4daf7d56cf6b4f52dd9a2cb5dd`  
		Last Modified: Wed, 30 Mar 2022 19:38:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de35ab51f9a083208854e695dc8879ecf7b9820ef90d9c2c356219ba2651fc`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fd10c0fb45dc51fe4815d510ad7c71fef44e80dd9393308f7ad1a475c465c`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 53.4 MB (53429900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42744cc7790693010c1abb7779bc759b995d9e50d8904bd37afebaf941dcf12b`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cc9d0d65fd6d9afa6e8bcca9941cd6fdaab5a37ee45ce68ea4def7528d673a`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 40.5 MB (40479681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f188c7be958b84ecc16d325c13dd32543ff1e126d9fe14bec3b8397ec173c`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
