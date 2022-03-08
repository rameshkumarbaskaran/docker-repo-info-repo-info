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
$ docker pull mysql@sha256:66d52e6baa8093820c09fec56992a5ee734f17e9fad8ef5ffc31597b231bd048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:143400b13686d43df0c78e8afe27c21ea4c16b9a22928185cfff9404eeb2430e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d8667108c29e3b7a0984860b9c262d6867b20084921c0108ee077a60ad4102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:42 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:43 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 08 Mar 2022 19:27:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:28:01 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:28:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:28:02 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:28:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:28:03 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:28:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a7517cdca397718e74aafc5107fd1d925b991fd809151087339e7e44c5aaa`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac645a526e45d45d9b53899bfadb7a5ae3ec5a4bb790c45350d2f72f1cbcdcb3`  
		Last Modified: Tue, 08 Mar 2022 19:30:21 GMT  
		Size: 108.6 MB (108637135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a292dcc315cc0dae819c6e88aa9370cd05df8f443f57cdb7993f133526004110`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 5.1 KB (5139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff70b7ef8a8b8abba05cf9ab312f1d082cfc069e3f900aab6b5c8a510ac0a488`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:66d52e6baa8093820c09fec56992a5ee734f17e9fad8ef5ffc31597b231bd048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:143400b13686d43df0c78e8afe27c21ea4c16b9a22928185cfff9404eeb2430e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d8667108c29e3b7a0984860b9c262d6867b20084921c0108ee077a60ad4102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:42 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:43 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 08 Mar 2022 19:27:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:28:01 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:28:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:28:02 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:28:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:28:03 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:28:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a7517cdca397718e74aafc5107fd1d925b991fd809151087339e7e44c5aaa`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac645a526e45d45d9b53899bfadb7a5ae3ec5a4bb790c45350d2f72f1cbcdcb3`  
		Last Modified: Tue, 08 Mar 2022 19:30:21 GMT  
		Size: 108.6 MB (108637135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a292dcc315cc0dae819c6e88aa9370cd05df8f443f57cdb7993f133526004110`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 5.1 KB (5139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff70b7ef8a8b8abba05cf9ab312f1d082cfc069e3f900aab6b5c8a510ac0a488`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:6a7a8a0c15fa4ca0d9ec85ac3fda70b4749e52fd13c9ca4d5eb0d16efc192e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:847a9c4e83c6bd9fe737e8fb841a2d6197d1407a4657ddb810060a9fff475e76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124779861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63e577980bf587f2bafeea4ae79d9eb41c5744cde8f9d24501a7c3a806a23da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:33:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:33:55 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:33:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:26:31 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 08 Mar 2022 19:27:03 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Tue, 08 Mar 2022 19:27:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:27:18 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:27:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:27:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Tue, 08 Mar 2022 19:27:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:27:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:27:38 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:27:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:27:38 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:27:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4915557694f2e99ba4f3c31018dd343c5dd684cc17dfc82bc6907c0ad8b7c7be`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda14bdaa732132cfb0a98e28a5372b750b07f7c701dd3f23b27209d91359dd0`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 930.2 KB (930235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b5fb768db2157c6bdb3a1bcac58e3652bf1543d39f8a81f3ee8be220b3a712`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 3.7 MB (3708422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd86b448d395b76436c8bbfc3b07df034056a757f7420243eb4e4c8783d9503`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a856e87d733fdb342899ec85fff5eb1f64b798a865fa1cda8a2aea57ec9c6f31`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af78d167e47009381ea4d0fe0033d991f03d879159801424084ffca52ed2a075`  
		Last Modified: Tue, 08 Mar 2022 19:29:50 GMT  
		Size: 25.4 MB (25445899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f23017b8e617195316dee8808ceb16ecb9c4e1da4e8230a88af69a9070c077f`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e418ba1e823bddac09c2b166a2d7cbcc06166878249d85ad07119637d8d4a`  
		Last Modified: Tue, 08 Mar 2022 19:29:54 GMT  
		Size: 46.4 MB (46354930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d661b191f612f8741ee6366a28d4f6231833fed59ccf3b145a95c68fd49bcfbf`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:66d52e6baa8093820c09fec56992a5ee734f17e9fad8ef5ffc31597b231bd048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:143400b13686d43df0c78e8afe27c21ea4c16b9a22928185cfff9404eeb2430e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d8667108c29e3b7a0984860b9c262d6867b20084921c0108ee077a60ad4102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:42 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:43 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 08 Mar 2022 19:27:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:28:01 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:28:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:28:02 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:28:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:28:03 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:28:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a7517cdca397718e74aafc5107fd1d925b991fd809151087339e7e44c5aaa`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac645a526e45d45d9b53899bfadb7a5ae3ec5a4bb790c45350d2f72f1cbcdcb3`  
		Last Modified: Tue, 08 Mar 2022 19:30:21 GMT  
		Size: 108.6 MB (108637135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a292dcc315cc0dae819c6e88aa9370cd05df8f443f57cdb7993f133526004110`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 5.1 KB (5139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff70b7ef8a8b8abba05cf9ab312f1d082cfc069e3f900aab6b5c8a510ac0a488`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:66d52e6baa8093820c09fec56992a5ee734f17e9fad8ef5ffc31597b231bd048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:143400b13686d43df0c78e8afe27c21ea4c16b9a22928185cfff9404eeb2430e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d8667108c29e3b7a0984860b9c262d6867b20084921c0108ee077a60ad4102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:42 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:43 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 08 Mar 2022 19:27:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:28:01 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:28:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:28:02 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:28:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:28:03 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:28:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a7517cdca397718e74aafc5107fd1d925b991fd809151087339e7e44c5aaa`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac645a526e45d45d9b53899bfadb7a5ae3ec5a4bb790c45350d2f72f1cbcdcb3`  
		Last Modified: Tue, 08 Mar 2022 19:30:21 GMT  
		Size: 108.6 MB (108637135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a292dcc315cc0dae819c6e88aa9370cd05df8f443f57cdb7993f133526004110`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 5.1 KB (5139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff70b7ef8a8b8abba05cf9ab312f1d082cfc069e3f900aab6b5c8a510ac0a488`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:6a7a8a0c15fa4ca0d9ec85ac3fda70b4749e52fd13c9ca4d5eb0d16efc192e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:847a9c4e83c6bd9fe737e8fb841a2d6197d1407a4657ddb810060a9fff475e76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124779861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63e577980bf587f2bafeea4ae79d9eb41c5744cde8f9d24501a7c3a806a23da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:33:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:33:55 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:33:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:26:31 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 08 Mar 2022 19:27:03 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Tue, 08 Mar 2022 19:27:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:27:18 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:27:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:27:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Tue, 08 Mar 2022 19:27:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:27:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:27:38 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:27:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:27:38 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:27:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4915557694f2e99ba4f3c31018dd343c5dd684cc17dfc82bc6907c0ad8b7c7be`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda14bdaa732132cfb0a98e28a5372b750b07f7c701dd3f23b27209d91359dd0`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 930.2 KB (930235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b5fb768db2157c6bdb3a1bcac58e3652bf1543d39f8a81f3ee8be220b3a712`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 3.7 MB (3708422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd86b448d395b76436c8bbfc3b07df034056a757f7420243eb4e4c8783d9503`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a856e87d733fdb342899ec85fff5eb1f64b798a865fa1cda8a2aea57ec9c6f31`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af78d167e47009381ea4d0fe0033d991f03d879159801424084ffca52ed2a075`  
		Last Modified: Tue, 08 Mar 2022 19:29:50 GMT  
		Size: 25.4 MB (25445899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f23017b8e617195316dee8808ceb16ecb9c4e1da4e8230a88af69a9070c077f`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e418ba1e823bddac09c2b166a2d7cbcc06166878249d85ad07119637d8d4a`  
		Last Modified: Tue, 08 Mar 2022 19:29:54 GMT  
		Size: 46.4 MB (46354930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d661b191f612f8741ee6366a28d4f6231833fed59ccf3b145a95c68fd49bcfbf`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37`

```console
$ docker pull mysql@sha256:66d52e6baa8093820c09fec56992a5ee734f17e9fad8ef5ffc31597b231bd048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37` - linux; amd64

```console
$ docker pull mysql@sha256:143400b13686d43df0c78e8afe27c21ea4c16b9a22928185cfff9404eeb2430e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d8667108c29e3b7a0984860b9c262d6867b20084921c0108ee077a60ad4102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:42 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:43 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 08 Mar 2022 19:27:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:28:01 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:28:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:28:02 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:28:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:28:03 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:28:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a7517cdca397718e74aafc5107fd1d925b991fd809151087339e7e44c5aaa`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac645a526e45d45d9b53899bfadb7a5ae3ec5a4bb790c45350d2f72f1cbcdcb3`  
		Last Modified: Tue, 08 Mar 2022 19:30:21 GMT  
		Size: 108.6 MB (108637135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a292dcc315cc0dae819c6e88aa9370cd05df8f443f57cdb7993f133526004110`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 5.1 KB (5139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff70b7ef8a8b8abba05cf9ab312f1d082cfc069e3f900aab6b5c8a510ac0a488`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-debian`

```console
$ docker pull mysql@sha256:66d52e6baa8093820c09fec56992a5ee734f17e9fad8ef5ffc31597b231bd048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:143400b13686d43df0c78e8afe27c21ea4c16b9a22928185cfff9404eeb2430e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d8667108c29e3b7a0984860b9c262d6867b20084921c0108ee077a60ad4102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:42 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:43 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 08 Mar 2022 19:27:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:28:01 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:28:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:28:02 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:28:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:28:03 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:28:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a7517cdca397718e74aafc5107fd1d925b991fd809151087339e7e44c5aaa`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac645a526e45d45d9b53899bfadb7a5ae3ec5a4bb790c45350d2f72f1cbcdcb3`  
		Last Modified: Tue, 08 Mar 2022 19:30:21 GMT  
		Size: 108.6 MB (108637135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a292dcc315cc0dae819c6e88aa9370cd05df8f443f57cdb7993f133526004110`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 5.1 KB (5139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff70b7ef8a8b8abba05cf9ab312f1d082cfc069e3f900aab6b5c8a510ac0a488`  
		Last Modified: Tue, 08 Mar 2022 19:30:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-oracle`

```console
$ docker pull mysql@sha256:6a7a8a0c15fa4ca0d9ec85ac3fda70b4749e52fd13c9ca4d5eb0d16efc192e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:847a9c4e83c6bd9fe737e8fb841a2d6197d1407a4657ddb810060a9fff475e76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124779861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63e577980bf587f2bafeea4ae79d9eb41c5744cde8f9d24501a7c3a806a23da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:33:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:33:55 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:33:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:26:31 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 08 Mar 2022 19:27:03 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Tue, 08 Mar 2022 19:27:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:27:18 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:27:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:27:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Tue, 08 Mar 2022 19:27:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:27:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:27:38 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:27:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:27:38 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:27:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4915557694f2e99ba4f3c31018dd343c5dd684cc17dfc82bc6907c0ad8b7c7be`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda14bdaa732132cfb0a98e28a5372b750b07f7c701dd3f23b27209d91359dd0`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 930.2 KB (930235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b5fb768db2157c6bdb3a1bcac58e3652bf1543d39f8a81f3ee8be220b3a712`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 3.7 MB (3708422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd86b448d395b76436c8bbfc3b07df034056a757f7420243eb4e4c8783d9503`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a856e87d733fdb342899ec85fff5eb1f64b798a865fa1cda8a2aea57ec9c6f31`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af78d167e47009381ea4d0fe0033d991f03d879159801424084ffca52ed2a075`  
		Last Modified: Tue, 08 Mar 2022 19:29:50 GMT  
		Size: 25.4 MB (25445899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f23017b8e617195316dee8808ceb16ecb9c4e1da4e8230a88af69a9070c077f`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e418ba1e823bddac09c2b166a2d7cbcc06166878249d85ad07119637d8d4a`  
		Last Modified: Tue, 08 Mar 2022 19:29:54 GMT  
		Size: 46.4 MB (46354930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d661b191f612f8741ee6366a28d4f6231833fed59ccf3b145a95c68fd49bcfbf`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:b17a66b49277a68066559416cf44a185cfee538d0e16b5624781019bc716c122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:83469837189400492f32d23cadbfc97fae3dc019871337a841609f0b71a34907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154587970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826efd84393bb2451404ae04fd24c97aa0094d6072242001a9505e0a8099aac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 08 Mar 2022 19:25:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:26:10 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:26:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:26:11 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 08 Mar 2022 19:26:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:26:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:26:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:26:12 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:26:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e745fe86aaf15d9370cb4ce8a9fe13edd5766abd587de26bfc18e6426d4d9f1`  
		Last Modified: Tue, 08 Mar 2022 19:28:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab75add93486640aba1eea75ed97d92720de01183eefc6ed3a64f4a20d3d7677`  
		Last Modified: Tue, 08 Mar 2022 19:29:13 GMT  
		Size: 107.8 MB (107805092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e3960383f33688441f03174496b1296aa8b0311bf43a9c3007f77955acb257`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f7809659515c4ff4e0dbb9ec46a54dd7e6d6e8f08f9b0c0b2b9bda6488c4bb`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ead2303095cebcd241d0cb58c97d92e83a408d5cc587e088888fee40d9aa0a7`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:b17a66b49277a68066559416cf44a185cfee538d0e16b5624781019bc716c122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:83469837189400492f32d23cadbfc97fae3dc019871337a841609f0b71a34907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154587970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826efd84393bb2451404ae04fd24c97aa0094d6072242001a9505e0a8099aac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 08 Mar 2022 19:25:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:26:10 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:26:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:26:11 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 08 Mar 2022 19:26:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:26:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:26:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:26:12 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:26:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e745fe86aaf15d9370cb4ce8a9fe13edd5766abd587de26bfc18e6426d4d9f1`  
		Last Modified: Tue, 08 Mar 2022 19:28:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab75add93486640aba1eea75ed97d92720de01183eefc6ed3a64f4a20d3d7677`  
		Last Modified: Tue, 08 Mar 2022 19:29:13 GMT  
		Size: 107.8 MB (107805092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e3960383f33688441f03174496b1296aa8b0311bf43a9c3007f77955acb257`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f7809659515c4ff4e0dbb9ec46a54dd7e6d6e8f08f9b0c0b2b9bda6488c4bb`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ead2303095cebcd241d0cb58c97d92e83a408d5cc587e088888fee40d9aa0a7`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:4377686768c90f2048b264d5a35b0e5946e04e7d6135ff9a6b0095ec09841c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9e1153be4b9c62a158d15b0e6f77799759bcd8a0766d3bb7038272fe21179370
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132915921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110c7218bb7188c986e7febc2f55d6a959818ac34d4d345a65aa7f98613a4d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:31:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:31:44 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:31:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:23:08 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:23:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:23:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:24:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:24:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:24:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:24:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:24:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:24:54 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:24:54 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:24:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5207ba089c5352dfd5cafa4419213f7e6c2dfb2a3d8301f9911ec66fc683c9`  
		Last Modified: Fri, 25 Feb 2022 03:36:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598adc979ae4bcf156eb841c681302fa8f44b58dea06ce95ccf11afb915fd3c2`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84657b0f541b69d0df5959c2a2bf58e9015de5f8e3aec3604f07692e18bea39a`  
		Last Modified: Tue, 08 Mar 2022 19:28:33 GMT  
		Size: 4.5 MB (4549263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b564ce0a68e22f654e153a1aba91e74956614f223ba2ccadb4250f1527c5e0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:31 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5790554ab14a56904f0c6c10c45bb623c160349b3590540ac790c931eadaedf2`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c8157d30bc26ba6e81fa5e10143c100ed056a439a0836568678490d46d0a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 47.3 MB (47263779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390e812ba33fe1baf908f76e9ab2e26607cc5d7790893c4f7c20502ff9702a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c924b76189376a203d08a1c022f536033ef154ad1c29842d233347101a1b8fc`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 38.3 MB (38283274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a3deabc6af673361daaf9cd0bde8f2da0054e0ee36cb3b0a2825d364c8df16`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd32a12635aee6af9d552ec32dd353a8c5abe5726e931023a3b6c12b07eb55b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141154782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0356e0d737001e53d9109c189846ca8a8dcb6dfa5058522fac5ff0590757a7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:58:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 02:58:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 02:58:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:50:32 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:51:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:51:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:51:17 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:51:18 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:51:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:51:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:51:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:52:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:52:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:52:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:52:13 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:52:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e43073605675017fa1d3f45abfea0fa0d6b3f0dcc26eb29a4920adc5d49b`  
		Last Modified: Fri, 25 Feb 2022 03:00:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811e76642f83f9e9101fd42b5f55528b93b5e1943f6d61006f71ee6291bcde0`  
		Last Modified: Fri, 25 Feb 2022 03:00:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a8bda1feeb7c2f1d3be071ebe0e2eb0fcd0ccd3ead359c52ec1aade8fb1c81`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 4.4 MB (4387324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2e1490447a6058e6894a33d6e3059a6a8e3f77d9b5015529ecf481747a6383`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbcebabf3bd13e9e4e457f8f863a5e30541efd7edf9a7321acf231d69f52c24`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f336d193ba9eb36ca50acb329aad504ddc5fb057c38baa92cdadb136243d351a`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 53.4 MB (53435007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377fdaaf480b2bc83cc6dc95000b54c3ac4d858319775baf4bcba5a9c12002f`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77464d80dfef5c59883655a88a449266f939dc59c01727245d89ac8648290f34`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 40.5 MB (40514019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01868f6e8e34bb8f26a9cc3da8ee584ab3e0a726936f325928a413a9f68853a6`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:b17a66b49277a68066559416cf44a185cfee538d0e16b5624781019bc716c122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:83469837189400492f32d23cadbfc97fae3dc019871337a841609f0b71a34907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154587970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826efd84393bb2451404ae04fd24c97aa0094d6072242001a9505e0a8099aac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 08 Mar 2022 19:25:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:26:10 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:26:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:26:11 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 08 Mar 2022 19:26:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:26:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:26:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:26:12 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:26:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e745fe86aaf15d9370cb4ce8a9fe13edd5766abd587de26bfc18e6426d4d9f1`  
		Last Modified: Tue, 08 Mar 2022 19:28:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab75add93486640aba1eea75ed97d92720de01183eefc6ed3a64f4a20d3d7677`  
		Last Modified: Tue, 08 Mar 2022 19:29:13 GMT  
		Size: 107.8 MB (107805092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e3960383f33688441f03174496b1296aa8b0311bf43a9c3007f77955acb257`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f7809659515c4ff4e0dbb9ec46a54dd7e6d6e8f08f9b0c0b2b9bda6488c4bb`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ead2303095cebcd241d0cb58c97d92e83a408d5cc587e088888fee40d9aa0a7`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:b17a66b49277a68066559416cf44a185cfee538d0e16b5624781019bc716c122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:83469837189400492f32d23cadbfc97fae3dc019871337a841609f0b71a34907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154587970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826efd84393bb2451404ae04fd24c97aa0094d6072242001a9505e0a8099aac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 08 Mar 2022 19:25:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:26:10 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:26:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:26:11 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 08 Mar 2022 19:26:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:26:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:26:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:26:12 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:26:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e745fe86aaf15d9370cb4ce8a9fe13edd5766abd587de26bfc18e6426d4d9f1`  
		Last Modified: Tue, 08 Mar 2022 19:28:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab75add93486640aba1eea75ed97d92720de01183eefc6ed3a64f4a20d3d7677`  
		Last Modified: Tue, 08 Mar 2022 19:29:13 GMT  
		Size: 107.8 MB (107805092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e3960383f33688441f03174496b1296aa8b0311bf43a9c3007f77955acb257`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f7809659515c4ff4e0dbb9ec46a54dd7e6d6e8f08f9b0c0b2b9bda6488c4bb`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ead2303095cebcd241d0cb58c97d92e83a408d5cc587e088888fee40d9aa0a7`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:4377686768c90f2048b264d5a35b0e5946e04e7d6135ff9a6b0095ec09841c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9e1153be4b9c62a158d15b0e6f77799759bcd8a0766d3bb7038272fe21179370
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132915921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110c7218bb7188c986e7febc2f55d6a959818ac34d4d345a65aa7f98613a4d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:31:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:31:44 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:31:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:23:08 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:23:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:23:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:24:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:24:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:24:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:24:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:24:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:24:54 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:24:54 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:24:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5207ba089c5352dfd5cafa4419213f7e6c2dfb2a3d8301f9911ec66fc683c9`  
		Last Modified: Fri, 25 Feb 2022 03:36:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598adc979ae4bcf156eb841c681302fa8f44b58dea06ce95ccf11afb915fd3c2`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84657b0f541b69d0df5959c2a2bf58e9015de5f8e3aec3604f07692e18bea39a`  
		Last Modified: Tue, 08 Mar 2022 19:28:33 GMT  
		Size: 4.5 MB (4549263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b564ce0a68e22f654e153a1aba91e74956614f223ba2ccadb4250f1527c5e0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:31 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5790554ab14a56904f0c6c10c45bb623c160349b3590540ac790c931eadaedf2`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c8157d30bc26ba6e81fa5e10143c100ed056a439a0836568678490d46d0a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 47.3 MB (47263779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390e812ba33fe1baf908f76e9ab2e26607cc5d7790893c4f7c20502ff9702a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c924b76189376a203d08a1c022f536033ef154ad1c29842d233347101a1b8fc`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 38.3 MB (38283274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a3deabc6af673361daaf9cd0bde8f2da0054e0ee36cb3b0a2825d364c8df16`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd32a12635aee6af9d552ec32dd353a8c5abe5726e931023a3b6c12b07eb55b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141154782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0356e0d737001e53d9109c189846ca8a8dcb6dfa5058522fac5ff0590757a7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:58:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 02:58:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 02:58:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:50:32 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:51:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:51:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:51:17 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:51:18 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:51:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:51:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:51:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:52:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:52:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:52:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:52:13 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:52:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e43073605675017fa1d3f45abfea0fa0d6b3f0dcc26eb29a4920adc5d49b`  
		Last Modified: Fri, 25 Feb 2022 03:00:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811e76642f83f9e9101fd42b5f55528b93b5e1943f6d61006f71ee6291bcde0`  
		Last Modified: Fri, 25 Feb 2022 03:00:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a8bda1feeb7c2f1d3be071ebe0e2eb0fcd0ccd3ead359c52ec1aade8fb1c81`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 4.4 MB (4387324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2e1490447a6058e6894a33d6e3059a6a8e3f77d9b5015529ecf481747a6383`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbcebabf3bd13e9e4e457f8f863a5e30541efd7edf9a7321acf231d69f52c24`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f336d193ba9eb36ca50acb329aad504ddc5fb057c38baa92cdadb136243d351a`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 53.4 MB (53435007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377fdaaf480b2bc83cc6dc95000b54c3ac4d858319775baf4bcba5a9c12002f`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77464d80dfef5c59883655a88a449266f939dc59c01727245d89ac8648290f34`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 40.5 MB (40514019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01868f6e8e34bb8f26a9cc3da8ee584ab3e0a726936f325928a413a9f68853a6`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28`

```console
$ docker pull mysql@sha256:b17a66b49277a68066559416cf44a185cfee538d0e16b5624781019bc716c122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28` - linux; amd64

```console
$ docker pull mysql@sha256:83469837189400492f32d23cadbfc97fae3dc019871337a841609f0b71a34907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154587970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826efd84393bb2451404ae04fd24c97aa0094d6072242001a9505e0a8099aac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 08 Mar 2022 19:25:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:26:10 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:26:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:26:11 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 08 Mar 2022 19:26:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:26:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:26:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:26:12 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:26:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e745fe86aaf15d9370cb4ce8a9fe13edd5766abd587de26bfc18e6426d4d9f1`  
		Last Modified: Tue, 08 Mar 2022 19:28:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab75add93486640aba1eea75ed97d92720de01183eefc6ed3a64f4a20d3d7677`  
		Last Modified: Tue, 08 Mar 2022 19:29:13 GMT  
		Size: 107.8 MB (107805092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e3960383f33688441f03174496b1296aa8b0311bf43a9c3007f77955acb257`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f7809659515c4ff4e0dbb9ec46a54dd7e6d6e8f08f9b0c0b2b9bda6488c4bb`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ead2303095cebcd241d0cb58c97d92e83a408d5cc587e088888fee40d9aa0a7`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-debian`

```console
$ docker pull mysql@sha256:b17a66b49277a68066559416cf44a185cfee538d0e16b5624781019bc716c122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28-debian` - linux; amd64

```console
$ docker pull mysql@sha256:83469837189400492f32d23cadbfc97fae3dc019871337a841609f0b71a34907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154587970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826efd84393bb2451404ae04fd24c97aa0094d6072242001a9505e0a8099aac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 08 Mar 2022 19:25:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:26:10 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:26:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:26:11 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 08 Mar 2022 19:26:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:26:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:26:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:26:12 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:26:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e745fe86aaf15d9370cb4ce8a9fe13edd5766abd587de26bfc18e6426d4d9f1`  
		Last Modified: Tue, 08 Mar 2022 19:28:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab75add93486640aba1eea75ed97d92720de01183eefc6ed3a64f4a20d3d7677`  
		Last Modified: Tue, 08 Mar 2022 19:29:13 GMT  
		Size: 107.8 MB (107805092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e3960383f33688441f03174496b1296aa8b0311bf43a9c3007f77955acb257`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f7809659515c4ff4e0dbb9ec46a54dd7e6d6e8f08f9b0c0b2b9bda6488c4bb`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ead2303095cebcd241d0cb58c97d92e83a408d5cc587e088888fee40d9aa0a7`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-oracle`

```console
$ docker pull mysql@sha256:4377686768c90f2048b264d5a35b0e5946e04e7d6135ff9a6b0095ec09841c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.28-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9e1153be4b9c62a158d15b0e6f77799759bcd8a0766d3bb7038272fe21179370
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132915921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110c7218bb7188c986e7febc2f55d6a959818ac34d4d345a65aa7f98613a4d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:31:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:31:44 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:31:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:23:08 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:23:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:23:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:24:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:24:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:24:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:24:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:24:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:24:54 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:24:54 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:24:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5207ba089c5352dfd5cafa4419213f7e6c2dfb2a3d8301f9911ec66fc683c9`  
		Last Modified: Fri, 25 Feb 2022 03:36:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598adc979ae4bcf156eb841c681302fa8f44b58dea06ce95ccf11afb915fd3c2`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84657b0f541b69d0df5959c2a2bf58e9015de5f8e3aec3604f07692e18bea39a`  
		Last Modified: Tue, 08 Mar 2022 19:28:33 GMT  
		Size: 4.5 MB (4549263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b564ce0a68e22f654e153a1aba91e74956614f223ba2ccadb4250f1527c5e0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:31 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5790554ab14a56904f0c6c10c45bb623c160349b3590540ac790c931eadaedf2`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c8157d30bc26ba6e81fa5e10143c100ed056a439a0836568678490d46d0a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 47.3 MB (47263779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390e812ba33fe1baf908f76e9ab2e26607cc5d7790893c4f7c20502ff9702a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c924b76189376a203d08a1c022f536033ef154ad1c29842d233347101a1b8fc`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 38.3 MB (38283274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a3deabc6af673361daaf9cd0bde8f2da0054e0ee36cb3b0a2825d364c8df16`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.28-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd32a12635aee6af9d552ec32dd353a8c5abe5726e931023a3b6c12b07eb55b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141154782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0356e0d737001e53d9109c189846ca8a8dcb6dfa5058522fac5ff0590757a7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:58:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 02:58:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 02:58:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:50:32 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:51:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:51:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:51:17 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:51:18 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:51:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:51:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:51:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:52:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:52:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:52:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:52:13 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:52:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e43073605675017fa1d3f45abfea0fa0d6b3f0dcc26eb29a4920adc5d49b`  
		Last Modified: Fri, 25 Feb 2022 03:00:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811e76642f83f9e9101fd42b5f55528b93b5e1943f6d61006f71ee6291bcde0`  
		Last Modified: Fri, 25 Feb 2022 03:00:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a8bda1feeb7c2f1d3be071ebe0e2eb0fcd0ccd3ead359c52ec1aade8fb1c81`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 4.4 MB (4387324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2e1490447a6058e6894a33d6e3059a6a8e3f77d9b5015529ecf481747a6383`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbcebabf3bd13e9e4e457f8f863a5e30541efd7edf9a7321acf231d69f52c24`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f336d193ba9eb36ca50acb329aad504ddc5fb057c38baa92cdadb136243d351a`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 53.4 MB (53435007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377fdaaf480b2bc83cc6dc95000b54c3ac4d858319775baf4bcba5a9c12002f`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77464d80dfef5c59883655a88a449266f939dc59c01727245d89ac8648290f34`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 40.5 MB (40514019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01868f6e8e34bb8f26a9cc3da8ee584ab3e0a726936f325928a413a9f68853a6`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:b17a66b49277a68066559416cf44a185cfee538d0e16b5624781019bc716c122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:83469837189400492f32d23cadbfc97fae3dc019871337a841609f0b71a34907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154587970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826efd84393bb2451404ae04fd24c97aa0094d6072242001a9505e0a8099aac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 08 Mar 2022 19:25:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:26:10 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:26:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:26:11 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 08 Mar 2022 19:26:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:26:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:26:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:26:12 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:26:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e745fe86aaf15d9370cb4ce8a9fe13edd5766abd587de26bfc18e6426d4d9f1`  
		Last Modified: Tue, 08 Mar 2022 19:28:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab75add93486640aba1eea75ed97d92720de01183eefc6ed3a64f4a20d3d7677`  
		Last Modified: Tue, 08 Mar 2022 19:29:13 GMT  
		Size: 107.8 MB (107805092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e3960383f33688441f03174496b1296aa8b0311bf43a9c3007f77955acb257`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f7809659515c4ff4e0dbb9ec46a54dd7e6d6e8f08f9b0c0b2b9bda6488c4bb`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ead2303095cebcd241d0cb58c97d92e83a408d5cc587e088888fee40d9aa0a7`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:b17a66b49277a68066559416cf44a185cfee538d0e16b5624781019bc716c122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:83469837189400492f32d23cadbfc97fae3dc019871337a841609f0b71a34907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154587970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826efd84393bb2451404ae04fd24c97aa0094d6072242001a9505e0a8099aac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Mar 2022 19:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Mar 2022 19:25:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:25:56 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 08 Mar 2022 19:25:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 08 Mar 2022 19:26:10 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 08 Mar 2022 19:26:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:26:11 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 08 Mar 2022 19:26:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:26:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 08 Mar 2022 19:26:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:26:12 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:26:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28abcb7f57e0160acfd10563c106f591200e134e1b85b2b50562f325e271afc5`  
		Last Modified: Tue, 08 Mar 2022 19:29:02 GMT  
		Size: 14.1 MB (14052434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d27a4317033ac7924fdeac237c5f2f1698c9945a98f0c652569633cef85a0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:59 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e745fe86aaf15d9370cb4ce8a9fe13edd5766abd587de26bfc18e6426d4d9f1`  
		Last Modified: Tue, 08 Mar 2022 19:28:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab75add93486640aba1eea75ed97d92720de01183eefc6ed3a64f4a20d3d7677`  
		Last Modified: Tue, 08 Mar 2022 19:29:13 GMT  
		Size: 107.8 MB (107805092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e3960383f33688441f03174496b1296aa8b0311bf43a9c3007f77955acb257`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f7809659515c4ff4e0dbb9ec46a54dd7e6d6e8f08f9b0c0b2b9bda6488c4bb`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ead2303095cebcd241d0cb58c97d92e83a408d5cc587e088888fee40d9aa0a7`  
		Last Modified: Tue, 08 Mar 2022 19:28:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:4377686768c90f2048b264d5a35b0e5946e04e7d6135ff9a6b0095ec09841c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9e1153be4b9c62a158d15b0e6f77799759bcd8a0766d3bb7038272fe21179370
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132915921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110c7218bb7188c986e7febc2f55d6a959818ac34d4d345a65aa7f98613a4d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:31:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:31:44 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:31:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:23:08 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:23:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:23:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:24:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:24:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:24:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:24:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:24:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:24:54 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:24:54 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:24:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5207ba089c5352dfd5cafa4419213f7e6c2dfb2a3d8301f9911ec66fc683c9`  
		Last Modified: Fri, 25 Feb 2022 03:36:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598adc979ae4bcf156eb841c681302fa8f44b58dea06ce95ccf11afb915fd3c2`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84657b0f541b69d0df5959c2a2bf58e9015de5f8e3aec3604f07692e18bea39a`  
		Last Modified: Tue, 08 Mar 2022 19:28:33 GMT  
		Size: 4.5 MB (4549263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b564ce0a68e22f654e153a1aba91e74956614f223ba2ccadb4250f1527c5e0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:31 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5790554ab14a56904f0c6c10c45bb623c160349b3590540ac790c931eadaedf2`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c8157d30bc26ba6e81fa5e10143c100ed056a439a0836568678490d46d0a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 47.3 MB (47263779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390e812ba33fe1baf908f76e9ab2e26607cc5d7790893c4f7c20502ff9702a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c924b76189376a203d08a1c022f536033ef154ad1c29842d233347101a1b8fc`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 38.3 MB (38283274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a3deabc6af673361daaf9cd0bde8f2da0054e0ee36cb3b0a2825d364c8df16`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd32a12635aee6af9d552ec32dd353a8c5abe5726e931023a3b6c12b07eb55b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141154782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0356e0d737001e53d9109c189846ca8a8dcb6dfa5058522fac5ff0590757a7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:58:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 02:58:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 02:58:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:50:32 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:51:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:51:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:51:17 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:51:18 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:51:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:51:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:51:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:52:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:52:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:52:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:52:13 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:52:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e43073605675017fa1d3f45abfea0fa0d6b3f0dcc26eb29a4920adc5d49b`  
		Last Modified: Fri, 25 Feb 2022 03:00:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811e76642f83f9e9101fd42b5f55528b93b5e1943f6d61006f71ee6291bcde0`  
		Last Modified: Fri, 25 Feb 2022 03:00:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a8bda1feeb7c2f1d3be071ebe0e2eb0fcd0ccd3ead359c52ec1aade8fb1c81`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 4.4 MB (4387324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2e1490447a6058e6894a33d6e3059a6a8e3f77d9b5015529ecf481747a6383`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbcebabf3bd13e9e4e457f8f863a5e30541efd7edf9a7321acf231d69f52c24`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f336d193ba9eb36ca50acb329aad504ddc5fb057c38baa92cdadb136243d351a`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 53.4 MB (53435007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377fdaaf480b2bc83cc6dc95000b54c3ac4d858319775baf4bcba5a9c12002f`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77464d80dfef5c59883655a88a449266f939dc59c01727245d89ac8648290f34`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 40.5 MB (40514019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01868f6e8e34bb8f26a9cc3da8ee584ab3e0a726936f325928a413a9f68853a6`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
