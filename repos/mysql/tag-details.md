<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.51`](#mysql5651)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.33`](#mysql5733)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.23`](#mysql8023)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:dce7f54b744d09e95525ff8c767c5ba1c6a5a54d04c208fa55e3052ded713453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:95a3b244b2e990ce5633dd449326cec6ce20e9e366ba01fdf11ebc15a9cd38d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154635817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f0b1e283d233c244996ebe85014ed694b9016abd352837d46e6a53866c271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:49:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 31 Mar 2021 04:49:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:49:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 31 Mar 2021 04:49:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 04:49:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 31 Mar 2021 04:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:50:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 31 Mar 2021 04:50:36 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 31 Mar 2021 04:50:36 GMT
ENV MYSQL_VERSION=5.7.33-1debian10
# Wed, 31 Mar 2021 04:50:38 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 31 Mar 2021 04:51:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 31 Mar 2021 04:51:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 Mar 2021 04:51:07 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Wed, 31 Mar 2021 04:51:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 31 Mar 2021 04:51:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 04:51:10 GMT
EXPOSE 3306 33060
# Wed, 31 Mar 2021 04:51:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f3d947b1044b89f9efd8ac9de505b80683b6dcb92a52529dd211fcd8b6629`  
		Last Modified: Wed, 31 Mar 2021 04:52:40 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2dd2f75b0455d2023b8e3b567ace83f81c55a6fbdff66273271293b36662de`  
		Last Modified: Wed, 31 Mar 2021 04:52:42 GMT  
		Size: 4.2 MB (4179249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faaceef2b9443f21f90fcada32491c6f3c1002e5b583fc79116b2ca161ac9ea`  
		Last Modified: Wed, 31 Mar 2021 04:52:38 GMT  
		Size: 1.4 MB (1419399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77c8c445ec2f71c0f105947e74edebe59c5e81f76f1f56c31a1c963c8102af1`  
		Last Modified: Wed, 31 Mar 2021 04:52:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074029aeaa5ff29609bab1a049751d43c22e3f219176e329df4f4f48ae97f41a`  
		Last Modified: Wed, 31 Mar 2021 04:52:39 GMT  
		Size: 13.4 MB (13447674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1122545c6cfc89fd6072f380bd1137afee34ab4305c9b5ddc7abd2924636ca`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0539e5d96e0ac2f76a27eb34f0d46adc47f3238cbf83defcc0998b502de398ec`  
		Last Modified: Wed, 31 Mar 2021 04:53:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf3befab801eaf75adfacfbb5838f9be5b42259ed841a17f6de4bd6f26515e2`  
		Last Modified: Wed, 31 Mar 2021 04:53:40 GMT  
		Size: 108.4 MB (108440064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ba39ab191fef40e877965582fb9583a02292df1340f5b793c0d55f368e0550`  
		Last Modified: Wed, 31 Mar 2021 04:53:18 GMT  
		Size: 5.5 KB (5519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d472d441f7e92a470b1a49ffc0ccd33b19d5c0aad8d2c4b27322c99694e29fc1`  
		Last Modified: Wed, 31 Mar 2021 04:53:18 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:e6c6bdc8cff8960953db5cb42f8be2d1db2931fafbf5f217d65b99ba0edae5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:8de2ea5aa07c8aea29b6ebfbe0e69f22ca199854e392d7ab8874dce88f1698b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102980592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d1008b853c9bceb939ed6cd92072b94802a9cbd850b2b7ba4d1f809d62cf0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:51:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 31 Mar 2021 04:51:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:51:30 GMT
ENV GOSU_VERSION=1.12
# Wed, 31 Mar 2021 04:51:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 04:51:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 31 Mar 2021 04:51:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:51:56 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 31 Mar 2021 04:51:56 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 31 Mar 2021 04:51:56 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Wed, 31 Mar 2021 04:51:57 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Wed, 31 Mar 2021 04:52:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 31 Mar 2021 04:52:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 Mar 2021 04:52:14 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Wed, 31 Mar 2021 04:52:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 31 Mar 2021 04:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 04:52:16 GMT
EXPOSE 3306
# Wed, 31 Mar 2021 04:52:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde922a9980f2144b8307af857be3be7fa6a9df4dc8b5c95e1641137fba0c810`  
		Last Modified: Wed, 31 Mar 2021 04:54:02 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5e58faa9a877dd702974cc41fb6094d08b3dcd249bbc3f2b04717bf3e25166`  
		Last Modified: Wed, 31 Mar 2021 04:54:01 GMT  
		Size: 4.5 MB (4503289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d7b1499787a96a76dd48bf1cb359a761f74226fe6e6bdba829d0d4f8a4c9f8`  
		Last Modified: Wed, 31 Mar 2021 04:54:00 GMT  
		Size: 1.4 MB (1412249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67575f8b7b802a8adb1813f35e62038cf4b38d03152d471e548acdd521945088`  
		Last Modified: Wed, 31 Mar 2021 04:53:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2844490be173204293f1d6b474b79f220256356cb949528569cd6666d0211bc`  
		Last Modified: Wed, 31 Mar 2021 04:54:04 GMT  
		Size: 10.2 MB (10225707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f6510c6a65c8634066e8f462b505aa3c34d65870669d0040b25149c4ed688b`  
		Last Modified: Wed, 31 Mar 2021 04:53:56 GMT  
		Size: 29.0 KB (28955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877a22faf2fc89313ceeab2f2bef77c09c3b4cbae55d94195eb53f648fde9301`  
		Last Modified: Wed, 31 Mar 2021 04:53:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6259bafdad044b8d750a9db221e8d0b0df129d1ecd91065c5d572641a4d0575c`  
		Last Modified: Wed, 31 Mar 2021 04:54:14 GMT  
		Size: 64.3 MB (64274365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2909034558722ca804d8f1fad3169160e5f6ba1073327e1c54cf87f3b143d3b1`  
		Last Modified: Wed, 31 Mar 2021 04:53:57 GMT  
		Size: 5.5 KB (5534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ba80fc86c34d36378ac91e078ed5089a583f8f1c0c57f913c05e651d34df4e`  
		Last Modified: Wed, 31 Mar 2021 04:53:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.51`

```console
$ docker pull mysql@sha256:e6c6bdc8cff8960953db5cb42f8be2d1db2931fafbf5f217d65b99ba0edae5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.51` - linux; amd64

```console
$ docker pull mysql@sha256:8de2ea5aa07c8aea29b6ebfbe0e69f22ca199854e392d7ab8874dce88f1698b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102980592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d1008b853c9bceb939ed6cd92072b94802a9cbd850b2b7ba4d1f809d62cf0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:51:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 31 Mar 2021 04:51:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:51:30 GMT
ENV GOSU_VERSION=1.12
# Wed, 31 Mar 2021 04:51:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 04:51:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 31 Mar 2021 04:51:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:51:56 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 31 Mar 2021 04:51:56 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 31 Mar 2021 04:51:56 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Wed, 31 Mar 2021 04:51:57 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Wed, 31 Mar 2021 04:52:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 31 Mar 2021 04:52:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 Mar 2021 04:52:14 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Wed, 31 Mar 2021 04:52:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 31 Mar 2021 04:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 04:52:16 GMT
EXPOSE 3306
# Wed, 31 Mar 2021 04:52:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde922a9980f2144b8307af857be3be7fa6a9df4dc8b5c95e1641137fba0c810`  
		Last Modified: Wed, 31 Mar 2021 04:54:02 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5e58faa9a877dd702974cc41fb6094d08b3dcd249bbc3f2b04717bf3e25166`  
		Last Modified: Wed, 31 Mar 2021 04:54:01 GMT  
		Size: 4.5 MB (4503289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d7b1499787a96a76dd48bf1cb359a761f74226fe6e6bdba829d0d4f8a4c9f8`  
		Last Modified: Wed, 31 Mar 2021 04:54:00 GMT  
		Size: 1.4 MB (1412249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67575f8b7b802a8adb1813f35e62038cf4b38d03152d471e548acdd521945088`  
		Last Modified: Wed, 31 Mar 2021 04:53:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2844490be173204293f1d6b474b79f220256356cb949528569cd6666d0211bc`  
		Last Modified: Wed, 31 Mar 2021 04:54:04 GMT  
		Size: 10.2 MB (10225707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f6510c6a65c8634066e8f462b505aa3c34d65870669d0040b25149c4ed688b`  
		Last Modified: Wed, 31 Mar 2021 04:53:56 GMT  
		Size: 29.0 KB (28955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877a22faf2fc89313ceeab2f2bef77c09c3b4cbae55d94195eb53f648fde9301`  
		Last Modified: Wed, 31 Mar 2021 04:53:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6259bafdad044b8d750a9db221e8d0b0df129d1ecd91065c5d572641a4d0575c`  
		Last Modified: Wed, 31 Mar 2021 04:54:14 GMT  
		Size: 64.3 MB (64274365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2909034558722ca804d8f1fad3169160e5f6ba1073327e1c54cf87f3b143d3b1`  
		Last Modified: Wed, 31 Mar 2021 04:53:57 GMT  
		Size: 5.5 KB (5534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ba80fc86c34d36378ac91e078ed5089a583f8f1c0c57f913c05e651d34df4e`  
		Last Modified: Wed, 31 Mar 2021 04:53:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:dce7f54b744d09e95525ff8c767c5ba1c6a5a54d04c208fa55e3052ded713453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:95a3b244b2e990ce5633dd449326cec6ce20e9e366ba01fdf11ebc15a9cd38d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154635817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f0b1e283d233c244996ebe85014ed694b9016abd352837d46e6a53866c271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:49:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 31 Mar 2021 04:49:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:49:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 31 Mar 2021 04:49:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 04:49:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 31 Mar 2021 04:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:50:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 31 Mar 2021 04:50:36 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 31 Mar 2021 04:50:36 GMT
ENV MYSQL_VERSION=5.7.33-1debian10
# Wed, 31 Mar 2021 04:50:38 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 31 Mar 2021 04:51:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 31 Mar 2021 04:51:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 Mar 2021 04:51:07 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Wed, 31 Mar 2021 04:51:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 31 Mar 2021 04:51:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 04:51:10 GMT
EXPOSE 3306 33060
# Wed, 31 Mar 2021 04:51:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f3d947b1044b89f9efd8ac9de505b80683b6dcb92a52529dd211fcd8b6629`  
		Last Modified: Wed, 31 Mar 2021 04:52:40 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2dd2f75b0455d2023b8e3b567ace83f81c55a6fbdff66273271293b36662de`  
		Last Modified: Wed, 31 Mar 2021 04:52:42 GMT  
		Size: 4.2 MB (4179249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faaceef2b9443f21f90fcada32491c6f3c1002e5b583fc79116b2ca161ac9ea`  
		Last Modified: Wed, 31 Mar 2021 04:52:38 GMT  
		Size: 1.4 MB (1419399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77c8c445ec2f71c0f105947e74edebe59c5e81f76f1f56c31a1c963c8102af1`  
		Last Modified: Wed, 31 Mar 2021 04:52:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074029aeaa5ff29609bab1a049751d43c22e3f219176e329df4f4f48ae97f41a`  
		Last Modified: Wed, 31 Mar 2021 04:52:39 GMT  
		Size: 13.4 MB (13447674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1122545c6cfc89fd6072f380bd1137afee34ab4305c9b5ddc7abd2924636ca`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0539e5d96e0ac2f76a27eb34f0d46adc47f3238cbf83defcc0998b502de398ec`  
		Last Modified: Wed, 31 Mar 2021 04:53:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf3befab801eaf75adfacfbb5838f9be5b42259ed841a17f6de4bd6f26515e2`  
		Last Modified: Wed, 31 Mar 2021 04:53:40 GMT  
		Size: 108.4 MB (108440064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ba39ab191fef40e877965582fb9583a02292df1340f5b793c0d55f368e0550`  
		Last Modified: Wed, 31 Mar 2021 04:53:18 GMT  
		Size: 5.5 KB (5519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d472d441f7e92a470b1a49ffc0ccd33b19d5c0aad8d2c4b27322c99694e29fc1`  
		Last Modified: Wed, 31 Mar 2021 04:53:18 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.33`

```console
$ docker pull mysql@sha256:dce7f54b744d09e95525ff8c767c5ba1c6a5a54d04c208fa55e3052ded713453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.33` - linux; amd64

```console
$ docker pull mysql@sha256:95a3b244b2e990ce5633dd449326cec6ce20e9e366ba01fdf11ebc15a9cd38d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154635817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f0b1e283d233c244996ebe85014ed694b9016abd352837d46e6a53866c271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:49:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 31 Mar 2021 04:49:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:49:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 31 Mar 2021 04:49:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 04:49:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 31 Mar 2021 04:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:50:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 31 Mar 2021 04:50:36 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 31 Mar 2021 04:50:36 GMT
ENV MYSQL_VERSION=5.7.33-1debian10
# Wed, 31 Mar 2021 04:50:38 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 31 Mar 2021 04:51:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 31 Mar 2021 04:51:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 Mar 2021 04:51:07 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Wed, 31 Mar 2021 04:51:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 31 Mar 2021 04:51:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 04:51:10 GMT
EXPOSE 3306 33060
# Wed, 31 Mar 2021 04:51:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f3d947b1044b89f9efd8ac9de505b80683b6dcb92a52529dd211fcd8b6629`  
		Last Modified: Wed, 31 Mar 2021 04:52:40 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2dd2f75b0455d2023b8e3b567ace83f81c55a6fbdff66273271293b36662de`  
		Last Modified: Wed, 31 Mar 2021 04:52:42 GMT  
		Size: 4.2 MB (4179249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faaceef2b9443f21f90fcada32491c6f3c1002e5b583fc79116b2ca161ac9ea`  
		Last Modified: Wed, 31 Mar 2021 04:52:38 GMT  
		Size: 1.4 MB (1419399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77c8c445ec2f71c0f105947e74edebe59c5e81f76f1f56c31a1c963c8102af1`  
		Last Modified: Wed, 31 Mar 2021 04:52:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074029aeaa5ff29609bab1a049751d43c22e3f219176e329df4f4f48ae97f41a`  
		Last Modified: Wed, 31 Mar 2021 04:52:39 GMT  
		Size: 13.4 MB (13447674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1122545c6cfc89fd6072f380bd1137afee34ab4305c9b5ddc7abd2924636ca`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0539e5d96e0ac2f76a27eb34f0d46adc47f3238cbf83defcc0998b502de398ec`  
		Last Modified: Wed, 31 Mar 2021 04:53:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf3befab801eaf75adfacfbb5838f9be5b42259ed841a17f6de4bd6f26515e2`  
		Last Modified: Wed, 31 Mar 2021 04:53:40 GMT  
		Size: 108.4 MB (108440064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ba39ab191fef40e877965582fb9583a02292df1340f5b793c0d55f368e0550`  
		Last Modified: Wed, 31 Mar 2021 04:53:18 GMT  
		Size: 5.5 KB (5519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d472d441f7e92a470b1a49ffc0ccd33b19d5c0aad8d2c4b27322c99694e29fc1`  
		Last Modified: Wed, 31 Mar 2021 04:53:18 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:c35eb76bbccfd0138c8c68ccb9b4cffe42c488a27f64ddc31a2b5f65aa93fce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:2878ca7ca986b54c948966b7103aeceb747f50b9ecf34ecf934036cca58274db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159323624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e646c6533b0bcb75743ea9b176a03012610b2df7072dc312bf5921d1fbc5149c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:49:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 31 Mar 2021 04:49:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:49:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 31 Mar 2021 04:49:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 04:49:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 31 Mar 2021 04:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:50:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 31 Mar 2021 04:50:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 31 Mar 2021 04:50:01 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Wed, 31 Mar 2021 04:50:03 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 31 Mar 2021 04:50:25 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 31 Mar 2021 04:50:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 Mar 2021 04:50:26 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 31 Mar 2021 04:50:26 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Wed, 31 Mar 2021 04:50:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 31 Mar 2021 04:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 04:50:28 GMT
EXPOSE 3306 33060
# Wed, 31 Mar 2021 04:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f3d947b1044b89f9efd8ac9de505b80683b6dcb92a52529dd211fcd8b6629`  
		Last Modified: Wed, 31 Mar 2021 04:52:40 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2dd2f75b0455d2023b8e3b567ace83f81c55a6fbdff66273271293b36662de`  
		Last Modified: Wed, 31 Mar 2021 04:52:42 GMT  
		Size: 4.2 MB (4179249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faaceef2b9443f21f90fcada32491c6f3c1002e5b583fc79116b2ca161ac9ea`  
		Last Modified: Wed, 31 Mar 2021 04:52:38 GMT  
		Size: 1.4 MB (1419399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77c8c445ec2f71c0f105947e74edebe59c5e81f76f1f56c31a1c963c8102af1`  
		Last Modified: Wed, 31 Mar 2021 04:52:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074029aeaa5ff29609bab1a049751d43c22e3f219176e329df4f4f48ae97f41a`  
		Last Modified: Wed, 31 Mar 2021 04:52:39 GMT  
		Size: 13.4 MB (13447674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1122545c6cfc89fd6072f380bd1137afee34ab4305c9b5ddc7abd2924636ca`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95ccd00139ee90331a4baea4d567709c0e153d81119fbb777e32bb89902121`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a719448fdb20bca98a642f1895edd0e2588e41519e8431d7e479fbf97f377d`  
		Last Modified: Wed, 31 Mar 2021 04:52:53 GMT  
		Size: 113.1 MB (113127023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31898a387a312497016da3222f9fc76aaa80d9cc19d1f2baec1e13a09cc16e3`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf402a978dc1496e28a0a5a30f068b40197af79df5d726862e87be9e0ac3704`  
		Last Modified: Wed, 31 Mar 2021 04:52:33 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bc7da512e3d6d5a9fd53e05db8669b09b958d12983fe3f1c0490e79786d46`  
		Last Modified: Wed, 31 Mar 2021 04:52:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:c35eb76bbccfd0138c8c68ccb9b4cffe42c488a27f64ddc31a2b5f65aa93fce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:2878ca7ca986b54c948966b7103aeceb747f50b9ecf34ecf934036cca58274db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159323624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e646c6533b0bcb75743ea9b176a03012610b2df7072dc312bf5921d1fbc5149c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:49:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 31 Mar 2021 04:49:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:49:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 31 Mar 2021 04:49:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 04:49:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 31 Mar 2021 04:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:50:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 31 Mar 2021 04:50:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 31 Mar 2021 04:50:01 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Wed, 31 Mar 2021 04:50:03 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 31 Mar 2021 04:50:25 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 31 Mar 2021 04:50:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 Mar 2021 04:50:26 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 31 Mar 2021 04:50:26 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Wed, 31 Mar 2021 04:50:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 31 Mar 2021 04:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 04:50:28 GMT
EXPOSE 3306 33060
# Wed, 31 Mar 2021 04:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f3d947b1044b89f9efd8ac9de505b80683b6dcb92a52529dd211fcd8b6629`  
		Last Modified: Wed, 31 Mar 2021 04:52:40 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2dd2f75b0455d2023b8e3b567ace83f81c55a6fbdff66273271293b36662de`  
		Last Modified: Wed, 31 Mar 2021 04:52:42 GMT  
		Size: 4.2 MB (4179249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faaceef2b9443f21f90fcada32491c6f3c1002e5b583fc79116b2ca161ac9ea`  
		Last Modified: Wed, 31 Mar 2021 04:52:38 GMT  
		Size: 1.4 MB (1419399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77c8c445ec2f71c0f105947e74edebe59c5e81f76f1f56c31a1c963c8102af1`  
		Last Modified: Wed, 31 Mar 2021 04:52:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074029aeaa5ff29609bab1a049751d43c22e3f219176e329df4f4f48ae97f41a`  
		Last Modified: Wed, 31 Mar 2021 04:52:39 GMT  
		Size: 13.4 MB (13447674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1122545c6cfc89fd6072f380bd1137afee34ab4305c9b5ddc7abd2924636ca`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95ccd00139ee90331a4baea4d567709c0e153d81119fbb777e32bb89902121`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a719448fdb20bca98a642f1895edd0e2588e41519e8431d7e479fbf97f377d`  
		Last Modified: Wed, 31 Mar 2021 04:52:53 GMT  
		Size: 113.1 MB (113127023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31898a387a312497016da3222f9fc76aaa80d9cc19d1f2baec1e13a09cc16e3`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf402a978dc1496e28a0a5a30f068b40197af79df5d726862e87be9e0ac3704`  
		Last Modified: Wed, 31 Mar 2021 04:52:33 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bc7da512e3d6d5a9fd53e05db8669b09b958d12983fe3f1c0490e79786d46`  
		Last Modified: Wed, 31 Mar 2021 04:52:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.23`

```console
$ docker pull mysql@sha256:c35eb76bbccfd0138c8c68ccb9b4cffe42c488a27f64ddc31a2b5f65aa93fce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.23` - linux; amd64

```console
$ docker pull mysql@sha256:2878ca7ca986b54c948966b7103aeceb747f50b9ecf34ecf934036cca58274db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159323624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e646c6533b0bcb75743ea9b176a03012610b2df7072dc312bf5921d1fbc5149c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:49:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 31 Mar 2021 04:49:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:49:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 31 Mar 2021 04:49:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 04:49:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 31 Mar 2021 04:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:50:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 31 Mar 2021 04:50:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 31 Mar 2021 04:50:01 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Wed, 31 Mar 2021 04:50:03 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 31 Mar 2021 04:50:25 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 31 Mar 2021 04:50:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 Mar 2021 04:50:26 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 31 Mar 2021 04:50:26 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Wed, 31 Mar 2021 04:50:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 31 Mar 2021 04:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 04:50:28 GMT
EXPOSE 3306 33060
# Wed, 31 Mar 2021 04:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f3d947b1044b89f9efd8ac9de505b80683b6dcb92a52529dd211fcd8b6629`  
		Last Modified: Wed, 31 Mar 2021 04:52:40 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2dd2f75b0455d2023b8e3b567ace83f81c55a6fbdff66273271293b36662de`  
		Last Modified: Wed, 31 Mar 2021 04:52:42 GMT  
		Size: 4.2 MB (4179249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faaceef2b9443f21f90fcada32491c6f3c1002e5b583fc79116b2ca161ac9ea`  
		Last Modified: Wed, 31 Mar 2021 04:52:38 GMT  
		Size: 1.4 MB (1419399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77c8c445ec2f71c0f105947e74edebe59c5e81f76f1f56c31a1c963c8102af1`  
		Last Modified: Wed, 31 Mar 2021 04:52:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074029aeaa5ff29609bab1a049751d43c22e3f219176e329df4f4f48ae97f41a`  
		Last Modified: Wed, 31 Mar 2021 04:52:39 GMT  
		Size: 13.4 MB (13447674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1122545c6cfc89fd6072f380bd1137afee34ab4305c9b5ddc7abd2924636ca`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95ccd00139ee90331a4baea4d567709c0e153d81119fbb777e32bb89902121`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a719448fdb20bca98a642f1895edd0e2588e41519e8431d7e479fbf97f377d`  
		Last Modified: Wed, 31 Mar 2021 04:52:53 GMT  
		Size: 113.1 MB (113127023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31898a387a312497016da3222f9fc76aaa80d9cc19d1f2baec1e13a09cc16e3`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf402a978dc1496e28a0a5a30f068b40197af79df5d726862e87be9e0ac3704`  
		Last Modified: Wed, 31 Mar 2021 04:52:33 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bc7da512e3d6d5a9fd53e05db8669b09b958d12983fe3f1c0490e79786d46`  
		Last Modified: Wed, 31 Mar 2021 04:52:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:c35eb76bbccfd0138c8c68ccb9b4cffe42c488a27f64ddc31a2b5f65aa93fce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:2878ca7ca986b54c948966b7103aeceb747f50b9ecf34ecf934036cca58274db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159323624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e646c6533b0bcb75743ea9b176a03012610b2df7072dc312bf5921d1fbc5149c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:49:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 31 Mar 2021 04:49:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:49:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 31 Mar 2021 04:49:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 04:49:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 31 Mar 2021 04:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:50:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 31 Mar 2021 04:50:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 31 Mar 2021 04:50:01 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Wed, 31 Mar 2021 04:50:03 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 31 Mar 2021 04:50:25 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 31 Mar 2021 04:50:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 Mar 2021 04:50:26 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 31 Mar 2021 04:50:26 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Wed, 31 Mar 2021 04:50:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 31 Mar 2021 04:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 04:50:28 GMT
EXPOSE 3306 33060
# Wed, 31 Mar 2021 04:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f3d947b1044b89f9efd8ac9de505b80683b6dcb92a52529dd211fcd8b6629`  
		Last Modified: Wed, 31 Mar 2021 04:52:40 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2dd2f75b0455d2023b8e3b567ace83f81c55a6fbdff66273271293b36662de`  
		Last Modified: Wed, 31 Mar 2021 04:52:42 GMT  
		Size: 4.2 MB (4179249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faaceef2b9443f21f90fcada32491c6f3c1002e5b583fc79116b2ca161ac9ea`  
		Last Modified: Wed, 31 Mar 2021 04:52:38 GMT  
		Size: 1.4 MB (1419399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77c8c445ec2f71c0f105947e74edebe59c5e81f76f1f56c31a1c963c8102af1`  
		Last Modified: Wed, 31 Mar 2021 04:52:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074029aeaa5ff29609bab1a049751d43c22e3f219176e329df4f4f48ae97f41a`  
		Last Modified: Wed, 31 Mar 2021 04:52:39 GMT  
		Size: 13.4 MB (13447674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1122545c6cfc89fd6072f380bd1137afee34ab4305c9b5ddc7abd2924636ca`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95ccd00139ee90331a4baea4d567709c0e153d81119fbb777e32bb89902121`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a719448fdb20bca98a642f1895edd0e2588e41519e8431d7e479fbf97f377d`  
		Last Modified: Wed, 31 Mar 2021 04:52:53 GMT  
		Size: 113.1 MB (113127023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31898a387a312497016da3222f9fc76aaa80d9cc19d1f2baec1e13a09cc16e3`  
		Last Modified: Wed, 31 Mar 2021 04:52:35 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf402a978dc1496e28a0a5a30f068b40197af79df5d726862e87be9e0ac3704`  
		Last Modified: Wed, 31 Mar 2021 04:52:33 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0bc7da512e3d6d5a9fd53e05db8669b09b958d12983fe3f1c0490e79786d46`  
		Last Modified: Wed, 31 Mar 2021 04:52:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
