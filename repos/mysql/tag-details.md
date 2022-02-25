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
$ docker pull mysql@sha256:ea24ddf1116d6e5053919748d2c27c8200e39ac0dbe9540f213a2d9141b66167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:5adbbb05d43e67a7ed5f4856d3831b22ece5178d23c565b31cef61f92e3467ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538ec2c8721c073370299bf83ae46b940c83899f44cc90d89799a046afc5816b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 23 Feb 2022 22:27:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:28:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:28:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:28:15 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:28:16 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:28:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45b9a309e746ae5e6074efb8d35490146b3188f1375fd6abe60763a4b13b79`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90242da46c5709e3df233b61e042de5002a59567de7c18a68c75935d386195d9`  
		Last Modified: Wed, 23 Feb 2022 22:30:30 GMT  
		Size: 108.6 MB (108636729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8d822d1293bf6661e4e6c69c425a5e9fca7b43bbf1201c1c66effbebd275d4`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 5.0 KB (4954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1704bf9fa7759625eeda74bcf484357dd06e4ef8d46319f09b59d4fd4c154eab`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:ea24ddf1116d6e5053919748d2c27c8200e39ac0dbe9540f213a2d9141b66167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:5adbbb05d43e67a7ed5f4856d3831b22ece5178d23c565b31cef61f92e3467ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538ec2c8721c073370299bf83ae46b940c83899f44cc90d89799a046afc5816b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 23 Feb 2022 22:27:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:28:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:28:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:28:15 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:28:16 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:28:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45b9a309e746ae5e6074efb8d35490146b3188f1375fd6abe60763a4b13b79`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90242da46c5709e3df233b61e042de5002a59567de7c18a68c75935d386195d9`  
		Last Modified: Wed, 23 Feb 2022 22:30:30 GMT  
		Size: 108.6 MB (108636729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8d822d1293bf6661e4e6c69c425a5e9fca7b43bbf1201c1c66effbebd275d4`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 5.0 KB (4954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1704bf9fa7759625eeda74bcf484357dd06e4ef8d46319f09b59d4fd4c154eab`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:7bab537633b1955d01d10fcea459da545d1fb8bd5345ecb7934fa22cf59f8d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f82078cf4647dab1229b20ce5f0b877fc9d0ff1e004fe5ed381ac49111bd2e31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123652103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4d7f4f7f485571b1ee8ed8cc37368884da5e73b1db25b851ef12d4fdabc94e`
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
# Fri, 25 Feb 2022 03:34:10 GMT
RUN set -eux; 	yum install -y 		gzip 		xz 	; 	yum clean all
# Fri, 25 Feb 2022 03:34:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 03:34:47 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 25 Feb 2022 03:34:47 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Fri, 25 Feb 2022 03:34:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 03:35:07 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 03:35:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 03:35:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Fri, 25 Feb 2022 03:35:27 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:35:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:35:28 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:35:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:35:28 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:35:28 GMT
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
	-	`sha256:717da021737923f3dedb7a5d42e088a49fd88858199b4896c90e26a12b980725`  
		Last Modified: Fri, 25 Feb 2022 03:36:24 GMT  
		Size: 2.7 MB (2667688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c870db35ffe1eca150aea5d46e9d3c8c7351a8117b7f880e48cb3fd83f54b8c`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9e012335bb37e2d78a5b25ae542ed05eeecc9c7ee04784e0a2b82a09ef9e04`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dfabeb5ffffa978096a9dd68b54bbc1dc5117a5b6c11a0b9fc9f95b8802448`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 25.4 MB (25397512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fa53264d9d4fcd7ba835996d0246996ff398b8e06dbe6e44852828002684b4`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a237e3df161318234fdec2f8c2cdbfb6386cb86d7b9c565e3545532daefe6643`  
		Last Modified: Fri, 25 Feb 2022 03:36:29 GMT  
		Size: 46.3 MB (46316473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d643c0f9440b2ba54a6c4bfe5e5033aeaa2c68c1831c997c3fe937c37f4721d5`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:ea24ddf1116d6e5053919748d2c27c8200e39ac0dbe9540f213a2d9141b66167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:5adbbb05d43e67a7ed5f4856d3831b22ece5178d23c565b31cef61f92e3467ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538ec2c8721c073370299bf83ae46b940c83899f44cc90d89799a046afc5816b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 23 Feb 2022 22:27:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:28:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:28:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:28:15 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:28:16 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:28:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45b9a309e746ae5e6074efb8d35490146b3188f1375fd6abe60763a4b13b79`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90242da46c5709e3df233b61e042de5002a59567de7c18a68c75935d386195d9`  
		Last Modified: Wed, 23 Feb 2022 22:30:30 GMT  
		Size: 108.6 MB (108636729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8d822d1293bf6661e4e6c69c425a5e9fca7b43bbf1201c1c66effbebd275d4`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 5.0 KB (4954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1704bf9fa7759625eeda74bcf484357dd06e4ef8d46319f09b59d4fd4c154eab`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:ea24ddf1116d6e5053919748d2c27c8200e39ac0dbe9540f213a2d9141b66167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:5adbbb05d43e67a7ed5f4856d3831b22ece5178d23c565b31cef61f92e3467ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538ec2c8721c073370299bf83ae46b940c83899f44cc90d89799a046afc5816b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 23 Feb 2022 22:27:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:28:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:28:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:28:15 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:28:16 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:28:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45b9a309e746ae5e6074efb8d35490146b3188f1375fd6abe60763a4b13b79`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90242da46c5709e3df233b61e042de5002a59567de7c18a68c75935d386195d9`  
		Last Modified: Wed, 23 Feb 2022 22:30:30 GMT  
		Size: 108.6 MB (108636729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8d822d1293bf6661e4e6c69c425a5e9fca7b43bbf1201c1c66effbebd275d4`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 5.0 KB (4954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1704bf9fa7759625eeda74bcf484357dd06e4ef8d46319f09b59d4fd4c154eab`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:7bab537633b1955d01d10fcea459da545d1fb8bd5345ecb7934fa22cf59f8d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f82078cf4647dab1229b20ce5f0b877fc9d0ff1e004fe5ed381ac49111bd2e31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123652103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4d7f4f7f485571b1ee8ed8cc37368884da5e73b1db25b851ef12d4fdabc94e`
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
# Fri, 25 Feb 2022 03:34:10 GMT
RUN set -eux; 	yum install -y 		gzip 		xz 	; 	yum clean all
# Fri, 25 Feb 2022 03:34:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 03:34:47 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 25 Feb 2022 03:34:47 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Fri, 25 Feb 2022 03:34:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 03:35:07 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 03:35:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 03:35:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Fri, 25 Feb 2022 03:35:27 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:35:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:35:28 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:35:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:35:28 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:35:28 GMT
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
	-	`sha256:717da021737923f3dedb7a5d42e088a49fd88858199b4896c90e26a12b980725`  
		Last Modified: Fri, 25 Feb 2022 03:36:24 GMT  
		Size: 2.7 MB (2667688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c870db35ffe1eca150aea5d46e9d3c8c7351a8117b7f880e48cb3fd83f54b8c`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9e012335bb37e2d78a5b25ae542ed05eeecc9c7ee04784e0a2b82a09ef9e04`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dfabeb5ffffa978096a9dd68b54bbc1dc5117a5b6c11a0b9fc9f95b8802448`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 25.4 MB (25397512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fa53264d9d4fcd7ba835996d0246996ff398b8e06dbe6e44852828002684b4`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a237e3df161318234fdec2f8c2cdbfb6386cb86d7b9c565e3545532daefe6643`  
		Last Modified: Fri, 25 Feb 2022 03:36:29 GMT  
		Size: 46.3 MB (46316473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d643c0f9440b2ba54a6c4bfe5e5033aeaa2c68c1831c997c3fe937c37f4721d5`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37`

```console
$ docker pull mysql@sha256:ea24ddf1116d6e5053919748d2c27c8200e39ac0dbe9540f213a2d9141b66167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37` - linux; amd64

```console
$ docker pull mysql@sha256:5adbbb05d43e67a7ed5f4856d3831b22ece5178d23c565b31cef61f92e3467ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538ec2c8721c073370299bf83ae46b940c83899f44cc90d89799a046afc5816b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 23 Feb 2022 22:27:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:28:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:28:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:28:15 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:28:16 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:28:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45b9a309e746ae5e6074efb8d35490146b3188f1375fd6abe60763a4b13b79`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90242da46c5709e3df233b61e042de5002a59567de7c18a68c75935d386195d9`  
		Last Modified: Wed, 23 Feb 2022 22:30:30 GMT  
		Size: 108.6 MB (108636729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8d822d1293bf6661e4e6c69c425a5e9fca7b43bbf1201c1c66effbebd275d4`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 5.0 KB (4954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1704bf9fa7759625eeda74bcf484357dd06e4ef8d46319f09b59d4fd4c154eab`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-debian`

```console
$ docker pull mysql@sha256:ea24ddf1116d6e5053919748d2c27c8200e39ac0dbe9540f213a2d9141b66167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:5adbbb05d43e67a7ed5f4856d3831b22ece5178d23c565b31cef61f92e3467ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538ec2c8721c073370299bf83ae46b940c83899f44cc90d89799a046afc5816b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 23 Feb 2022 22:27:54 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Wed, 23 Feb 2022 22:27:55 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:28:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:28:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:28:15 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:28:16 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:28:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45b9a309e746ae5e6074efb8d35490146b3188f1375fd6abe60763a4b13b79`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90242da46c5709e3df233b61e042de5002a59567de7c18a68c75935d386195d9`  
		Last Modified: Wed, 23 Feb 2022 22:30:30 GMT  
		Size: 108.6 MB (108636729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8d822d1293bf6661e4e6c69c425a5e9fca7b43bbf1201c1c66effbebd275d4`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 5.0 KB (4954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1704bf9fa7759625eeda74bcf484357dd06e4ef8d46319f09b59d4fd4c154eab`  
		Last Modified: Wed, 23 Feb 2022 22:30:15 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-oracle`

```console
$ docker pull mysql@sha256:7bab537633b1955d01d10fcea459da545d1fb8bd5345ecb7934fa22cf59f8d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f82078cf4647dab1229b20ce5f0b877fc9d0ff1e004fe5ed381ac49111bd2e31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123652103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4d7f4f7f485571b1ee8ed8cc37368884da5e73b1db25b851ef12d4fdabc94e`
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
# Fri, 25 Feb 2022 03:34:10 GMT
RUN set -eux; 	yum install -y 		gzip 		xz 	; 	yum clean all
# Fri, 25 Feb 2022 03:34:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 03:34:47 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 25 Feb 2022 03:34:47 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Fri, 25 Feb 2022 03:34:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 03:35:07 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 03:35:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 03:35:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Fri, 25 Feb 2022 03:35:27 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:35:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:35:28 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:35:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:35:28 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:35:28 GMT
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
	-	`sha256:717da021737923f3dedb7a5d42e088a49fd88858199b4896c90e26a12b980725`  
		Last Modified: Fri, 25 Feb 2022 03:36:24 GMT  
		Size: 2.7 MB (2667688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c870db35ffe1eca150aea5d46e9d3c8c7351a8117b7f880e48cb3fd83f54b8c`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9e012335bb37e2d78a5b25ae542ed05eeecc9c7ee04784e0a2b82a09ef9e04`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dfabeb5ffffa978096a9dd68b54bbc1dc5117a5b6c11a0b9fc9f95b8802448`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 25.4 MB (25397512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fa53264d9d4fcd7ba835996d0246996ff398b8e06dbe6e44852828002684b4`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a237e3df161318234fdec2f8c2cdbfb6386cb86d7b9c565e3545532daefe6643`  
		Last Modified: Fri, 25 Feb 2022 03:36:29 GMT  
		Size: 46.3 MB (46316473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d643c0f9440b2ba54a6c4bfe5e5033aeaa2c68c1831c997c3fe937c37f4721d5`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:0962b771c2398c6dcddbbe77b3cf6658408396229b612035d938fb7c8d11c23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:cb4641c97c8f216961b223f676fc68bd376b5197d64d2657b5c331a89af6c08b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126b4587b1b7a4ecbfcbabfa34164ca060416d0b58b2aa55d5a7e8f5e336761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:25:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 22:25:53 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 23 Feb 2022 22:25:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:26:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:26:09 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:26:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 23 Feb 2022 22:26:09 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:26:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:26:10 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:26:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71174f5fcbee70701ee49220cb1c6dc17c80ecccd06f591416a72bedfcd84e37`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e368ab37acf00b9102e4ad1989d99174aba158de3348550f244de2bc96d7d7`  
		Last Modified: Wed, 23 Feb 2022 22:29:25 GMT  
		Size: 107.8 MB (107804538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd10975b5ee27e41ce108ad67ad33b3f3d71590588e46336fd6785602e0e82`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9459cbd3ebfd000d9ed6f515804cad2e3d81e2782387e0e7dbdab8b0de1e7`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c49252794494c412bf391410f784ed593bd5f41693a1fd1d9de50c8f60db1f`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:0962b771c2398c6dcddbbe77b3cf6658408396229b612035d938fb7c8d11c23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cb4641c97c8f216961b223f676fc68bd376b5197d64d2657b5c331a89af6c08b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126b4587b1b7a4ecbfcbabfa34164ca060416d0b58b2aa55d5a7e8f5e336761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:25:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 22:25:53 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 23 Feb 2022 22:25:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:26:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:26:09 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:26:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 23 Feb 2022 22:26:09 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:26:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:26:10 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:26:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71174f5fcbee70701ee49220cb1c6dc17c80ecccd06f591416a72bedfcd84e37`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e368ab37acf00b9102e4ad1989d99174aba158de3348550f244de2bc96d7d7`  
		Last Modified: Wed, 23 Feb 2022 22:29:25 GMT  
		Size: 107.8 MB (107804538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd10975b5ee27e41ce108ad67ad33b3f3d71590588e46336fd6785602e0e82`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9459cbd3ebfd000d9ed6f515804cad2e3d81e2782387e0e7dbdab8b0de1e7`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c49252794494c412bf391410f784ed593bd5f41693a1fd1d9de50c8f60db1f`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:3b3288074ba41224f475737d211cfcbcf067ceab8bcc33bce335e7e68733eb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c9fec3bd72bbe0b2823c8146e6496127c2956f0a8b5f8ccfc55182a2721400e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131397757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c40e8c9733a486a75f03c9b38d2487e2a2ed3176b4b2e4b635fde969c7cb10`
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
# Fri, 25 Feb 2022 03:32:07 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 03:32:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:32:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 03:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 03:33:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 03:33:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:33:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:33:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:33:44 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:33:45 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:33:45 GMT
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
	-	`sha256:b69cc9c42213611889f94baffd34bae26e70b5c649f08f8413b11e768c161a2f`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 3.1 MB (3113129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7216bd700f0e78596085fdfe14df3b52f8a1ffa74c36fb1347ecebd666f43565`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed60440ccffd47e25d61aae903ee39fe7e94f84279b00ed2ac45519e617c096b`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f9c0fb50c73b47a6985efcb852651a804c512dc2435ea248c0c391d3384d9`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 47.2 MB (47216437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea56ac1a1fe9b67a35c85910563c7cb4515c4f6fec5422685442c76f32b16f9`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66437fa01c48af6a7230b921b18cd451d7c9f7c4d55b6dd2660595c954b4e5df`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 38.2 MB (38248768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad48a805d9f1a437c87f20327806cb37f7b44f9c0d1d14d1664efd505b7de5`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed9f0eb3b100fc28d9a5946b48de127cbbe846af0a49c07e1b3488f70bad6000
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139932347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ba820812516512aad540266121d6b6f5ff261efef5e1a30e43537c90ecc250`
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
# Fri, 25 Feb 2022 02:58:41 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 02:59:17 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 02:59:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 02:59:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 02:59:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 02:59:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 02:59:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 02:59:47 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:00:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:00:30 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:00:32 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:00:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:00:33 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:00:34 GMT
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
	-	`sha256:e99e7cda9427a7e16e3c00fd2d0e3c09a589a827177c9b3bd00562cd23fcc290`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 3.3 MB (3257102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7073284934f73f97f317a638af1c6f296e22717b7384f524497183dfae152`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97067f99c33d1d930cdeb33ead10f729fc121dfa0030bed96bae455c3cb190c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea6bac00966feeb96a990385efe9d1ae852191034ba52b0f15bf244f76d4ef`  
		Last Modified: Fri, 25 Feb 2022 03:01:01 GMT  
		Size: 53.4 MB (53380825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b97d6d1f3243fd9432aa48783caf6738ba38e70cd4d2ac02a7e4ec0de0811f`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96691f58fb8e44a6255e1f0e4915ebf5f1abc3a8072b1955d65bc7c5d76e44f8`  
		Last Modified: Fri, 25 Feb 2022 03:01:00 GMT  
		Size: 40.5 MB (40476174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc29ad3e8e8b2ca29d8e03393fe1ced3c309a955cf8943fa0f33a670b74e7c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:0962b771c2398c6dcddbbe77b3cf6658408396229b612035d938fb7c8d11c23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:cb4641c97c8f216961b223f676fc68bd376b5197d64d2657b5c331a89af6c08b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126b4587b1b7a4ecbfcbabfa34164ca060416d0b58b2aa55d5a7e8f5e336761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:25:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 22:25:53 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 23 Feb 2022 22:25:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:26:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:26:09 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:26:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 23 Feb 2022 22:26:09 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:26:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:26:10 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:26:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71174f5fcbee70701ee49220cb1c6dc17c80ecccd06f591416a72bedfcd84e37`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e368ab37acf00b9102e4ad1989d99174aba158de3348550f244de2bc96d7d7`  
		Last Modified: Wed, 23 Feb 2022 22:29:25 GMT  
		Size: 107.8 MB (107804538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd10975b5ee27e41ce108ad67ad33b3f3d71590588e46336fd6785602e0e82`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9459cbd3ebfd000d9ed6f515804cad2e3d81e2782387e0e7dbdab8b0de1e7`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c49252794494c412bf391410f784ed593bd5f41693a1fd1d9de50c8f60db1f`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:0962b771c2398c6dcddbbe77b3cf6658408396229b612035d938fb7c8d11c23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cb4641c97c8f216961b223f676fc68bd376b5197d64d2657b5c331a89af6c08b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126b4587b1b7a4ecbfcbabfa34164ca060416d0b58b2aa55d5a7e8f5e336761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:25:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 22:25:53 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 23 Feb 2022 22:25:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:26:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:26:09 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:26:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 23 Feb 2022 22:26:09 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:26:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:26:10 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:26:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71174f5fcbee70701ee49220cb1c6dc17c80ecccd06f591416a72bedfcd84e37`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e368ab37acf00b9102e4ad1989d99174aba158de3348550f244de2bc96d7d7`  
		Last Modified: Wed, 23 Feb 2022 22:29:25 GMT  
		Size: 107.8 MB (107804538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd10975b5ee27e41ce108ad67ad33b3f3d71590588e46336fd6785602e0e82`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9459cbd3ebfd000d9ed6f515804cad2e3d81e2782387e0e7dbdab8b0de1e7`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c49252794494c412bf391410f784ed593bd5f41693a1fd1d9de50c8f60db1f`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:3b3288074ba41224f475737d211cfcbcf067ceab8bcc33bce335e7e68733eb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c9fec3bd72bbe0b2823c8146e6496127c2956f0a8b5f8ccfc55182a2721400e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131397757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c40e8c9733a486a75f03c9b38d2487e2a2ed3176b4b2e4b635fde969c7cb10`
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
# Fri, 25 Feb 2022 03:32:07 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 03:32:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:32:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 03:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 03:33:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 03:33:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:33:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:33:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:33:44 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:33:45 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:33:45 GMT
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
	-	`sha256:b69cc9c42213611889f94baffd34bae26e70b5c649f08f8413b11e768c161a2f`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 3.1 MB (3113129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7216bd700f0e78596085fdfe14df3b52f8a1ffa74c36fb1347ecebd666f43565`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed60440ccffd47e25d61aae903ee39fe7e94f84279b00ed2ac45519e617c096b`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f9c0fb50c73b47a6985efcb852651a804c512dc2435ea248c0c391d3384d9`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 47.2 MB (47216437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea56ac1a1fe9b67a35c85910563c7cb4515c4f6fec5422685442c76f32b16f9`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66437fa01c48af6a7230b921b18cd451d7c9f7c4d55b6dd2660595c954b4e5df`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 38.2 MB (38248768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad48a805d9f1a437c87f20327806cb37f7b44f9c0d1d14d1664efd505b7de5`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed9f0eb3b100fc28d9a5946b48de127cbbe846af0a49c07e1b3488f70bad6000
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139932347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ba820812516512aad540266121d6b6f5ff261efef5e1a30e43537c90ecc250`
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
# Fri, 25 Feb 2022 02:58:41 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 02:59:17 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 02:59:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 02:59:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 02:59:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 02:59:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 02:59:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 02:59:47 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:00:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:00:30 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:00:32 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:00:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:00:33 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:00:34 GMT
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
	-	`sha256:e99e7cda9427a7e16e3c00fd2d0e3c09a589a827177c9b3bd00562cd23fcc290`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 3.3 MB (3257102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7073284934f73f97f317a638af1c6f296e22717b7384f524497183dfae152`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97067f99c33d1d930cdeb33ead10f729fc121dfa0030bed96bae455c3cb190c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea6bac00966feeb96a990385efe9d1ae852191034ba52b0f15bf244f76d4ef`  
		Last Modified: Fri, 25 Feb 2022 03:01:01 GMT  
		Size: 53.4 MB (53380825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b97d6d1f3243fd9432aa48783caf6738ba38e70cd4d2ac02a7e4ec0de0811f`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96691f58fb8e44a6255e1f0e4915ebf5f1abc3a8072b1955d65bc7c5d76e44f8`  
		Last Modified: Fri, 25 Feb 2022 03:01:00 GMT  
		Size: 40.5 MB (40476174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc29ad3e8e8b2ca29d8e03393fe1ced3c309a955cf8943fa0f33a670b74e7c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28`

```console
$ docker pull mysql@sha256:0962b771c2398c6dcddbbe77b3cf6658408396229b612035d938fb7c8d11c23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28` - linux; amd64

```console
$ docker pull mysql@sha256:cb4641c97c8f216961b223f676fc68bd376b5197d64d2657b5c331a89af6c08b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126b4587b1b7a4ecbfcbabfa34164ca060416d0b58b2aa55d5a7e8f5e336761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:25:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 22:25:53 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 23 Feb 2022 22:25:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:26:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:26:09 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:26:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 23 Feb 2022 22:26:09 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:26:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:26:10 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:26:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71174f5fcbee70701ee49220cb1c6dc17c80ecccd06f591416a72bedfcd84e37`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e368ab37acf00b9102e4ad1989d99174aba158de3348550f244de2bc96d7d7`  
		Last Modified: Wed, 23 Feb 2022 22:29:25 GMT  
		Size: 107.8 MB (107804538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd10975b5ee27e41ce108ad67ad33b3f3d71590588e46336fd6785602e0e82`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9459cbd3ebfd000d9ed6f515804cad2e3d81e2782387e0e7dbdab8b0de1e7`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c49252794494c412bf391410f784ed593bd5f41693a1fd1d9de50c8f60db1f`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-debian`

```console
$ docker pull mysql@sha256:0962b771c2398c6dcddbbe77b3cf6658408396229b612035d938fb7c8d11c23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cb4641c97c8f216961b223f676fc68bd376b5197d64d2657b5c331a89af6c08b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126b4587b1b7a4ecbfcbabfa34164ca060416d0b58b2aa55d5a7e8f5e336761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:25:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 22:25:53 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 23 Feb 2022 22:25:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:26:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:26:09 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:26:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 23 Feb 2022 22:26:09 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:26:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:26:10 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:26:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71174f5fcbee70701ee49220cb1c6dc17c80ecccd06f591416a72bedfcd84e37`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e368ab37acf00b9102e4ad1989d99174aba158de3348550f244de2bc96d7d7`  
		Last Modified: Wed, 23 Feb 2022 22:29:25 GMT  
		Size: 107.8 MB (107804538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd10975b5ee27e41ce108ad67ad33b3f3d71590588e46336fd6785602e0e82`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9459cbd3ebfd000d9ed6f515804cad2e3d81e2782387e0e7dbdab8b0de1e7`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c49252794494c412bf391410f784ed593bd5f41693a1fd1d9de50c8f60db1f`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-oracle`

```console
$ docker pull mysql@sha256:3b3288074ba41224f475737d211cfcbcf067ceab8bcc33bce335e7e68733eb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.28-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c9fec3bd72bbe0b2823c8146e6496127c2956f0a8b5f8ccfc55182a2721400e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131397757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c40e8c9733a486a75f03c9b38d2487e2a2ed3176b4b2e4b635fde969c7cb10`
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
# Fri, 25 Feb 2022 03:32:07 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 03:32:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:32:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 03:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 03:33:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 03:33:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:33:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:33:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:33:44 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:33:45 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:33:45 GMT
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
	-	`sha256:b69cc9c42213611889f94baffd34bae26e70b5c649f08f8413b11e768c161a2f`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 3.1 MB (3113129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7216bd700f0e78596085fdfe14df3b52f8a1ffa74c36fb1347ecebd666f43565`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed60440ccffd47e25d61aae903ee39fe7e94f84279b00ed2ac45519e617c096b`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f9c0fb50c73b47a6985efcb852651a804c512dc2435ea248c0c391d3384d9`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 47.2 MB (47216437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea56ac1a1fe9b67a35c85910563c7cb4515c4f6fec5422685442c76f32b16f9`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66437fa01c48af6a7230b921b18cd451d7c9f7c4d55b6dd2660595c954b4e5df`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 38.2 MB (38248768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad48a805d9f1a437c87f20327806cb37f7b44f9c0d1d14d1664efd505b7de5`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.28-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed9f0eb3b100fc28d9a5946b48de127cbbe846af0a49c07e1b3488f70bad6000
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139932347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ba820812516512aad540266121d6b6f5ff261efef5e1a30e43537c90ecc250`
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
# Fri, 25 Feb 2022 02:58:41 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 02:59:17 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 02:59:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 02:59:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 02:59:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 02:59:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 02:59:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 02:59:47 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:00:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:00:30 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:00:32 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:00:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:00:33 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:00:34 GMT
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
	-	`sha256:e99e7cda9427a7e16e3c00fd2d0e3c09a589a827177c9b3bd00562cd23fcc290`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 3.3 MB (3257102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7073284934f73f97f317a638af1c6f296e22717b7384f524497183dfae152`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97067f99c33d1d930cdeb33ead10f729fc121dfa0030bed96bae455c3cb190c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea6bac00966feeb96a990385efe9d1ae852191034ba52b0f15bf244f76d4ef`  
		Last Modified: Fri, 25 Feb 2022 03:01:01 GMT  
		Size: 53.4 MB (53380825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b97d6d1f3243fd9432aa48783caf6738ba38e70cd4d2ac02a7e4ec0de0811f`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96691f58fb8e44a6255e1f0e4915ebf5f1abc3a8072b1955d65bc7c5d76e44f8`  
		Last Modified: Fri, 25 Feb 2022 03:01:00 GMT  
		Size: 40.5 MB (40476174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc29ad3e8e8b2ca29d8e03393fe1ced3c309a955cf8943fa0f33a670b74e7c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:0962b771c2398c6dcddbbe77b3cf6658408396229b612035d938fb7c8d11c23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:cb4641c97c8f216961b223f676fc68bd376b5197d64d2657b5c331a89af6c08b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126b4587b1b7a4ecbfcbabfa34164ca060416d0b58b2aa55d5a7e8f5e336761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:25:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 22:25:53 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 23 Feb 2022 22:25:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:26:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:26:09 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:26:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 23 Feb 2022 22:26:09 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:26:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:26:10 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:26:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71174f5fcbee70701ee49220cb1c6dc17c80ecccd06f591416a72bedfcd84e37`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e368ab37acf00b9102e4ad1989d99174aba158de3348550f244de2bc96d7d7`  
		Last Modified: Wed, 23 Feb 2022 22:29:25 GMT  
		Size: 107.8 MB (107804538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd10975b5ee27e41ce108ad67ad33b3f3d71590588e46336fd6785602e0e82`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9459cbd3ebfd000d9ed6f515804cad2e3d81e2782387e0e7dbdab8b0de1e7`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c49252794494c412bf391410f784ed593bd5f41693a1fd1d9de50c8f60db1f`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:0962b771c2398c6dcddbbe77b3cf6658408396229b612035d938fb7c8d11c23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:cb4641c97c8f216961b223f676fc68bd376b5197d64d2657b5c331a89af6c08b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126b4587b1b7a4ecbfcbabfa34164ca060416d0b58b2aa55d5a7e8f5e336761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Feb 2022 22:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 22:25:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 22:25:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 22:25:53 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 23 Feb 2022 22:25:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 23 Feb 2022 22:26:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 23 Feb 2022 22:26:09 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 22:26:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 23 Feb 2022 22:26:09 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:26:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Feb 2022 22:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 22:26:10 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 22:26:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f5f7765d10dffc8825a89c30cddc2c753bde7435445ff55a5baaff1fe97654`  
		Last Modified: Wed, 23 Feb 2022 22:29:13 GMT  
		Size: 13.4 MB (13438692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f1dd5efbe2ac5e563ea686d55f58b8dcedf32c1434304652c549fdf299c88`  
		Last Modified: Wed, 23 Feb 2022 22:29:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71174f5fcbee70701ee49220cb1c6dc17c80ecccd06f591416a72bedfcd84e37`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e368ab37acf00b9102e4ad1989d99174aba158de3348550f244de2bc96d7d7`  
		Last Modified: Wed, 23 Feb 2022 22:29:25 GMT  
		Size: 107.8 MB (107804538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd10975b5ee27e41ce108ad67ad33b3f3d71590588e46336fd6785602e0e82`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9459cbd3ebfd000d9ed6f515804cad2e3d81e2782387e0e7dbdab8b0de1e7`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c49252794494c412bf391410f784ed593bd5f41693a1fd1d9de50c8f60db1f`  
		Last Modified: Wed, 23 Feb 2022 22:29:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:3b3288074ba41224f475737d211cfcbcf067ceab8bcc33bce335e7e68733eb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c9fec3bd72bbe0b2823c8146e6496127c2956f0a8b5f8ccfc55182a2721400e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131397757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c40e8c9733a486a75f03c9b38d2487e2a2ed3176b4b2e4b635fde969c7cb10`
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
# Fri, 25 Feb 2022 03:32:07 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 03:32:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:32:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 03:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 03:33:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 03:33:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:33:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:33:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:33:44 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:33:45 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:33:45 GMT
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
	-	`sha256:b69cc9c42213611889f94baffd34bae26e70b5c649f08f8413b11e768c161a2f`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 3.1 MB (3113129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7216bd700f0e78596085fdfe14df3b52f8a1ffa74c36fb1347ecebd666f43565`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed60440ccffd47e25d61aae903ee39fe7e94f84279b00ed2ac45519e617c096b`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f9c0fb50c73b47a6985efcb852651a804c512dc2435ea248c0c391d3384d9`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 47.2 MB (47216437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea56ac1a1fe9b67a35c85910563c7cb4515c4f6fec5422685442c76f32b16f9`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66437fa01c48af6a7230b921b18cd451d7c9f7c4d55b6dd2660595c954b4e5df`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 38.2 MB (38248768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad48a805d9f1a437c87f20327806cb37f7b44f9c0d1d14d1664efd505b7de5`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed9f0eb3b100fc28d9a5946b48de127cbbe846af0a49c07e1b3488f70bad6000
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139932347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ba820812516512aad540266121d6b6f5ff261efef5e1a30e43537c90ecc250`
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
# Fri, 25 Feb 2022 02:58:41 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 02:59:17 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 02:59:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 02:59:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 02:59:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 02:59:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 02:59:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 02:59:47 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:00:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:00:30 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:00:32 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:00:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:00:33 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:00:34 GMT
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
	-	`sha256:e99e7cda9427a7e16e3c00fd2d0e3c09a589a827177c9b3bd00562cd23fcc290`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 3.3 MB (3257102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7073284934f73f97f317a638af1c6f296e22717b7384f524497183dfae152`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97067f99c33d1d930cdeb33ead10f729fc121dfa0030bed96bae455c3cb190c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea6bac00966feeb96a990385efe9d1ae852191034ba52b0f15bf244f76d4ef`  
		Last Modified: Fri, 25 Feb 2022 03:01:01 GMT  
		Size: 53.4 MB (53380825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b97d6d1f3243fd9432aa48783caf6738ba38e70cd4d2ac02a7e4ec0de0811f`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96691f58fb8e44a6255e1f0e4915ebf5f1abc3a8072b1955d65bc7c5d76e44f8`  
		Last Modified: Fri, 25 Feb 2022 03:01:00 GMT  
		Size: 40.5 MB (40476174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc29ad3e8e8b2ca29d8e03393fe1ced3c309a955cf8943fa0f33a670b74e7c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
