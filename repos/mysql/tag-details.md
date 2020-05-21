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
$ docker pull mysql@sha256:d16d9ef7a4ecb29efcd1ba46d5a82bda3c28bd18c0f1e3b86ba54816211e1ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:375d2452a2009a51803d528ad9bd1926eead59b0d74a8e463afd0e6feb11a85e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154406115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fdfd462add8e63749aa08ff0044b13d342a042965f1ec6744586cda10dfce9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Fri, 15 May 2020 20:10:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:11:00 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:11:01 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 May 2020 05:20:19 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 21 May 2020 05:20:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 May 2020 05:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2020 05:20:21 GMT
EXPOSE 3306 33060
# Thu, 21 May 2020 05:20:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eec965ae405548af46a704346d97fcf663f9de2df1d71cbd6113ee803ef0556`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a531a782d709df74f09b2ba98298d124b08e89842a4eae8a918d3c5440b4b584`  
		Last Modified: Fri, 15 May 2020 20:13:21 GMT  
		Size: 108.3 MB (108257035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270aeddb45e3301edd9c682c814c9efc19ef53a43a681cd0c0ba2ea347837289`  
		Last Modified: Thu, 21 May 2020 05:20:42 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25569b610082fcf3711b4b0f087c095bc5c9f7abb46c86dc267a993ad57b43f`  
		Last Modified: Thu, 21 May 2020 05:20:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:60c27b50ca72d81d92a743a965a82f124a4e123c7d374a021887286408878d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:152c5f3e17faa4f71c247e1f53849d96da79f4121d8350a886c6f5901b37455f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102887212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4a20b3bbbc0a4f06337056afe3e26996eda97e00764388b001087facfe24ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:11:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:11:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:11:21 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:11:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:11:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:11:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:11:46 GMT
ENV MYSQL_MAJOR=5.6
# Fri, 15 May 2020 20:11:46 GMT
ENV MYSQL_VERSION=5.6.48-1debian9
# Fri, 15 May 2020 20:11:47 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:12:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:12:07 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 May 2020 05:20:25 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 21 May 2020 05:20:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 May 2020 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2020 05:20:26 GMT
EXPOSE 3306
# Thu, 21 May 2020 05:20:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4539e638b12dd4ea320a33239ccd7797ba40cdf743c134b2e59aedbc8e347fb`  
		Last Modified: Fri, 15 May 2020 20:13:29 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb8f0db2a3779eeb29488ed6fd4922daff7d67424665225276a92c03f8b790`  
		Last Modified: Fri, 15 May 2020 20:13:30 GMT  
		Size: 4.5 MB (4501267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27254901ad3716966d3dc2a05025da58414131cbefac01fb983a02c10f6f69c`  
		Last Modified: Fri, 15 May 2020 20:13:28 GMT  
		Size: 1.4 MB (1412320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e4d538a032b3c580856e0e341e2ec6b8e699eb225f7397226a90045bc95080`  
		Last Modified: Fri, 15 May 2020 20:13:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8608c48c2d6986e8653a844ab5b2cb81d95e3847c4436491da35d147fcbbdfa6`  
		Last Modified: Fri, 15 May 2020 20:13:33 GMT  
		Size: 10.2 MB (10222816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bbeb5e044578c3e7f070948cf75c66eeac765eaf0dccfe61060bc028706c8`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 28.3 KB (28328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c472cfc00c1ed45631189fd52dae6d7358373f57b7889a5a0c053190f6e5b`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3081c249e0eea462831eb7c0d51c38cd3cb97ed63253eb7dfd3a7db366ffaa4a`  
		Last Modified: Fri, 15 May 2020 20:13:43 GMT  
		Size: 64.2 MB (64195226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caddb3474acabee317950bc77f2bb81ca1b54a217b63b79c656f65c93e395200`  
		Last Modified: Thu, 21 May 2020 05:20:46 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec101f8c3a86b2f632d059d66b2740a539174a0e69f742e0cc85988dd218d19d`  
		Last Modified: Thu, 21 May 2020 05:20:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.48`

```console
$ docker pull mysql@sha256:60c27b50ca72d81d92a743a965a82f124a4e123c7d374a021887286408878d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.48` - linux; amd64

```console
$ docker pull mysql@sha256:152c5f3e17faa4f71c247e1f53849d96da79f4121d8350a886c6f5901b37455f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102887212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4a20b3bbbc0a4f06337056afe3e26996eda97e00764388b001087facfe24ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:11:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:11:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:11:21 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:11:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:11:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:11:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:11:46 GMT
ENV MYSQL_MAJOR=5.6
# Fri, 15 May 2020 20:11:46 GMT
ENV MYSQL_VERSION=5.6.48-1debian9
# Fri, 15 May 2020 20:11:47 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:12:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:12:07 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 May 2020 05:20:25 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 21 May 2020 05:20:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 May 2020 05:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2020 05:20:26 GMT
EXPOSE 3306
# Thu, 21 May 2020 05:20:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4539e638b12dd4ea320a33239ccd7797ba40cdf743c134b2e59aedbc8e347fb`  
		Last Modified: Fri, 15 May 2020 20:13:29 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb8f0db2a3779eeb29488ed6fd4922daff7d67424665225276a92c03f8b790`  
		Last Modified: Fri, 15 May 2020 20:13:30 GMT  
		Size: 4.5 MB (4501267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27254901ad3716966d3dc2a05025da58414131cbefac01fb983a02c10f6f69c`  
		Last Modified: Fri, 15 May 2020 20:13:28 GMT  
		Size: 1.4 MB (1412320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e4d538a032b3c580856e0e341e2ec6b8e699eb225f7397226a90045bc95080`  
		Last Modified: Fri, 15 May 2020 20:13:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8608c48c2d6986e8653a844ab5b2cb81d95e3847c4436491da35d147fcbbdfa6`  
		Last Modified: Fri, 15 May 2020 20:13:33 GMT  
		Size: 10.2 MB (10222816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bbeb5e044578c3e7f070948cf75c66eeac765eaf0dccfe61060bc028706c8`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 28.3 KB (28328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c472cfc00c1ed45631189fd52dae6d7358373f57b7889a5a0c053190f6e5b`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3081c249e0eea462831eb7c0d51c38cd3cb97ed63253eb7dfd3a7db366ffaa4a`  
		Last Modified: Fri, 15 May 2020 20:13:43 GMT  
		Size: 64.2 MB (64195226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caddb3474acabee317950bc77f2bb81ca1b54a217b63b79c656f65c93e395200`  
		Last Modified: Thu, 21 May 2020 05:20:46 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec101f8c3a86b2f632d059d66b2740a539174a0e69f742e0cc85988dd218d19d`  
		Last Modified: Thu, 21 May 2020 05:20:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:d16d9ef7a4ecb29efcd1ba46d5a82bda3c28bd18c0f1e3b86ba54816211e1ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:375d2452a2009a51803d528ad9bd1926eead59b0d74a8e463afd0e6feb11a85e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154406115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fdfd462add8e63749aa08ff0044b13d342a042965f1ec6744586cda10dfce9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Fri, 15 May 2020 20:10:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:11:00 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:11:01 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 May 2020 05:20:19 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 21 May 2020 05:20:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 May 2020 05:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2020 05:20:21 GMT
EXPOSE 3306 33060
# Thu, 21 May 2020 05:20:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eec965ae405548af46a704346d97fcf663f9de2df1d71cbd6113ee803ef0556`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a531a782d709df74f09b2ba98298d124b08e89842a4eae8a918d3c5440b4b584`  
		Last Modified: Fri, 15 May 2020 20:13:21 GMT  
		Size: 108.3 MB (108257035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270aeddb45e3301edd9c682c814c9efc19ef53a43a681cd0c0ba2ea347837289`  
		Last Modified: Thu, 21 May 2020 05:20:42 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25569b610082fcf3711b4b0f087c095bc5c9f7abb46c86dc267a993ad57b43f`  
		Last Modified: Thu, 21 May 2020 05:20:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.30`

```console
$ docker pull mysql@sha256:d16d9ef7a4ecb29efcd1ba46d5a82bda3c28bd18c0f1e3b86ba54816211e1ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.30` - linux; amd64

```console
$ docker pull mysql@sha256:375d2452a2009a51803d528ad9bd1926eead59b0d74a8e463afd0e6feb11a85e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154406115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fdfd462add8e63749aa08ff0044b13d342a042965f1ec6744586cda10dfce9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Fri, 15 May 2020 20:10:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:11:00 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:11:01 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 May 2020 05:20:19 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 21 May 2020 05:20:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 May 2020 05:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2020 05:20:21 GMT
EXPOSE 3306 33060
# Thu, 21 May 2020 05:20:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eec965ae405548af46a704346d97fcf663f9de2df1d71cbd6113ee803ef0556`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a531a782d709df74f09b2ba98298d124b08e89842a4eae8a918d3c5440b4b584`  
		Last Modified: Fri, 15 May 2020 20:13:21 GMT  
		Size: 108.3 MB (108257035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270aeddb45e3301edd9c682c814c9efc19ef53a43a681cd0c0ba2ea347837289`  
		Last Modified: Thu, 21 May 2020 05:20:42 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25569b610082fcf3711b4b0f087c095bc5c9f7abb46c86dc267a993ad57b43f`  
		Last Modified: Thu, 21 May 2020 05:20:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:a31a277d8d39450220c722c1302a345c84206e7fd4cdb619e7face046e89031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:3857435f3cf9de798f86a88708e27b17b8c6b4b281279e758f399e22f3a81b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f937e841c82981a9a6363f7f6f35ed6b9d5e3f16df50a72207e4a2a389983f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Fri, 15 May 2020 20:09:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:10:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 15 May 2020 20:10:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:10:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Thu, 21 May 2020 05:20:14 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 21 May 2020 05:20:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 May 2020 05:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2020 05:20:15 GMT
EXPOSE 3306 33060
# Thu, 21 May 2020 05:20:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597069368ef1ce225516b1597000747b3490cadcfc3becb2bc850de0bd68912a`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce39a5501878554bce3bd6fcbf89eeaa87e004ffe6b67bf73f3e9c00c3317733`  
		Last Modified: Fri, 15 May 2020 20:12:49 GMT  
		Size: 111.5 MB (111486682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d545bca14bf36c108e916a30ff7cf643598eaede713f8f9501cc33a2504e4a2`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e5bb2ae7b44fab344aaccde543035893d1d256e645f5a879cb19ce26daa91`  
		Last Modified: Thu, 21 May 2020 05:20:36 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5914e537c077ed87d8cbad0debb29747b54a395760acc51b94b2891de553d179`  
		Last Modified: Thu, 21 May 2020 05:20:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:a31a277d8d39450220c722c1302a345c84206e7fd4cdb619e7face046e89031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:3857435f3cf9de798f86a88708e27b17b8c6b4b281279e758f399e22f3a81b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f937e841c82981a9a6363f7f6f35ed6b9d5e3f16df50a72207e4a2a389983f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Fri, 15 May 2020 20:09:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:10:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 15 May 2020 20:10:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:10:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Thu, 21 May 2020 05:20:14 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 21 May 2020 05:20:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 May 2020 05:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2020 05:20:15 GMT
EXPOSE 3306 33060
# Thu, 21 May 2020 05:20:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597069368ef1ce225516b1597000747b3490cadcfc3becb2bc850de0bd68912a`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce39a5501878554bce3bd6fcbf89eeaa87e004ffe6b67bf73f3e9c00c3317733`  
		Last Modified: Fri, 15 May 2020 20:12:49 GMT  
		Size: 111.5 MB (111486682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d545bca14bf36c108e916a30ff7cf643598eaede713f8f9501cc33a2504e4a2`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e5bb2ae7b44fab344aaccde543035893d1d256e645f5a879cb19ce26daa91`  
		Last Modified: Thu, 21 May 2020 05:20:36 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5914e537c077ed87d8cbad0debb29747b54a395760acc51b94b2891de553d179`  
		Last Modified: Thu, 21 May 2020 05:20:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.20`

```console
$ docker pull mysql@sha256:a31a277d8d39450220c722c1302a345c84206e7fd4cdb619e7face046e89031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.20` - linux; amd64

```console
$ docker pull mysql@sha256:3857435f3cf9de798f86a88708e27b17b8c6b4b281279e758f399e22f3a81b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f937e841c82981a9a6363f7f6f35ed6b9d5e3f16df50a72207e4a2a389983f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Fri, 15 May 2020 20:09:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:10:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 15 May 2020 20:10:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:10:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Thu, 21 May 2020 05:20:14 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 21 May 2020 05:20:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 May 2020 05:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2020 05:20:15 GMT
EXPOSE 3306 33060
# Thu, 21 May 2020 05:20:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597069368ef1ce225516b1597000747b3490cadcfc3becb2bc850de0bd68912a`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce39a5501878554bce3bd6fcbf89eeaa87e004ffe6b67bf73f3e9c00c3317733`  
		Last Modified: Fri, 15 May 2020 20:12:49 GMT  
		Size: 111.5 MB (111486682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d545bca14bf36c108e916a30ff7cf643598eaede713f8f9501cc33a2504e4a2`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e5bb2ae7b44fab344aaccde543035893d1d256e645f5a879cb19ce26daa91`  
		Last Modified: Thu, 21 May 2020 05:20:36 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5914e537c077ed87d8cbad0debb29747b54a395760acc51b94b2891de553d179`  
		Last Modified: Thu, 21 May 2020 05:20:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:a31a277d8d39450220c722c1302a345c84206e7fd4cdb619e7face046e89031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:3857435f3cf9de798f86a88708e27b17b8c6b4b281279e758f399e22f3a81b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f937e841c82981a9a6363f7f6f35ed6b9d5e3f16df50a72207e4a2a389983f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Fri, 15 May 2020 20:09:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:10:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 15 May 2020 20:10:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:10:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Thu, 21 May 2020 05:20:14 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Thu, 21 May 2020 05:20:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 May 2020 05:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2020 05:20:15 GMT
EXPOSE 3306 33060
# Thu, 21 May 2020 05:20:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597069368ef1ce225516b1597000747b3490cadcfc3becb2bc850de0bd68912a`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce39a5501878554bce3bd6fcbf89eeaa87e004ffe6b67bf73f3e9c00c3317733`  
		Last Modified: Fri, 15 May 2020 20:12:49 GMT  
		Size: 111.5 MB (111486682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d545bca14bf36c108e916a30ff7cf643598eaede713f8f9501cc33a2504e4a2`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e5bb2ae7b44fab344aaccde543035893d1d256e645f5a879cb19ce26daa91`  
		Last Modified: Thu, 21 May 2020 05:20:36 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5914e537c077ed87d8cbad0debb29747b54a395760acc51b94b2891de553d179`  
		Last Modified: Thu, 21 May 2020 05:20:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
