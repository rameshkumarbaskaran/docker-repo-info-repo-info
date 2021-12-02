<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.51`](#mysql5651)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.36`](#mysql5736)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.27`](#mysql8027)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:d1cc87a3bd5dc07defc837bc9084f748a130606ff41923f46dec1986e0dc828d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:9415bfb9a83752d30b6395c84dde03573eeba7b5b9c937c0e09c3e7b32c76c93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154849221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e7101490b45decf606211a5437ed87aa6a82f1ff03c354564bf9375ce20f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:22:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 02 Dec 2021 11:22:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:22:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 02 Dec 2021 11:22:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Dec 2021 11:22:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Dec 2021 11:22:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:23:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 02 Dec 2021 11:23:43 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 02 Dec 2021 11:23:44 GMT
ENV MYSQL_VERSION=5.7.36-1debian10
# Thu, 02 Dec 2021 11:23:45 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 02 Dec 2021 11:24:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 02 Dec 2021 11:24:07 GMT
VOLUME [/var/lib/mysql]
# Thu, 02 Dec 2021 11:24:07 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 02 Dec 2021 11:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 11:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 11:24:08 GMT
EXPOSE 3306 33060
# Thu, 02 Dec 2021 11:24:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df186527fc4698f1a41fbbdaec1ae1c7e76b2b4fd34e8750db82f5c9dd1cf7da`  
		Last Modified: Thu, 02 Dec 2021 11:25:45 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa362a6aa7bd8aef47b5fa3c7d6c907f5d87f315792e677d2d1fce86258d6861`  
		Last Modified: Thu, 02 Dec 2021 11:25:46 GMT  
		Size: 4.2 MB (4179256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7cb1a200e984186d41ea2204b7bc8d81442cf59a2e2bf61c4625f43d9c8b3`  
		Last Modified: Thu, 02 Dec 2021 11:25:43 GMT  
		Size: 1.4 MB (1419462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949da226cc6d2b8a906157e7fc547dc4319d01e823bf8f872d6e516cd3c0ec9b`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce007079ee9d2f73484aa3a0c51ea4b93aece5b247df45045ceb5a944b9c18f`  
		Last Modified: Thu, 02 Dec 2021 11:25:47 GMT  
		Size: 13.4 MB (13448631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9f076e5a305da5cad538c80c188e0af815aa2d7fc5d4c20dfabe0fa7c907d`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b24c3f27affc7c0d6dc7f5e36582cfa4340f9cc85ad9d4c68baa344e6c7a52`  
		Last Modified: Thu, 02 Dec 2021 11:26:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc26ff6705a0608cf6da9ca3fbebaa0ea0bc39a60fb64843b34766447795b65`  
		Last Modified: Thu, 02 Dec 2021 11:26:42 GMT  
		Size: 108.6 MB (108637986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec5cdb5e7f7ae379b1884607863586b13219683657a4b6464574b5490a9bc60`  
		Last Modified: Thu, 02 Dec 2021 11:26:22 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1cb25f7525f2aa38e78d08c43df603fb33d3a74eaf4f7f54d5272582175f9c`  
		Last Modified: Thu, 02 Dec 2021 11:26:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:d0822b1b059e59fef7571b1a96224fb59fb0a84dffa59d8f3859281bde675a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:99d967e2880d67c5bc8a57813c29a291787457ffb91c74a4b9022b1833552df2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102979190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0befd40a091b063217be99ee9d87167851bc5c8c07fbe9a36d24567ece493a87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:24:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 02 Dec 2021 11:24:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:24:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 02 Dec 2021 11:24:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Dec 2021 11:24:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Dec 2021 11:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:24:48 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 02 Dec 2021 11:24:49 GMT
ENV MYSQL_MAJOR=5.6
# Thu, 02 Dec 2021 11:24:49 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Thu, 02 Dec 2021 11:24:50 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Thu, 02 Dec 2021 11:25:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 02 Dec 2021 11:25:07 GMT
VOLUME [/var/lib/mysql]
# Thu, 02 Dec 2021 11:25:08 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 02 Dec 2021 11:25:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 11:25:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 11:25:09 GMT
EXPOSE 3306
# Thu, 02 Dec 2021 11:25:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea446d3dd1a4fecc95ccdd97fd45e8f8401c751bd179b8115b35eca27179b3d`  
		Last Modified: Thu, 02 Dec 2021 11:27:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12b9de3971c6380773d4b420862a84d67fddefc511def03fe28082879770f90`  
		Last Modified: Thu, 02 Dec 2021 11:27:00 GMT  
		Size: 4.5 MB (4503815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cece02ee84c4f223dae24907324f34bf2f3943c84bf3257e3d5dee0df42855a`  
		Last Modified: Thu, 02 Dec 2021 11:27:00 GMT  
		Size: 1.4 MB (1412253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81584261ce182d915ab20a0834bfd844792b0c324fcf8a585171bf7ecde9e91a`  
		Last Modified: Thu, 02 Dec 2021 11:26:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a511d4a684485e250407a3b84b99ed670c28287f5d734f6a4dd20659c06a4f7d`  
		Last Modified: Thu, 02 Dec 2021 11:27:02 GMT  
		Size: 10.2 MB (10225793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2451f19813d4b19ca00ec4f70055d75e8978d28689fc1e8b0d3e81315d6e69`  
		Last Modified: Thu, 02 Dec 2021 11:26:56 GMT  
		Size: 26.1 KB (26079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d341343e375fd5892ba0cd3128489bc8952950c842bbf5226ea4c3a58dc99f`  
		Last Modified: Thu, 02 Dec 2021 11:26:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde17f57816b6c25e9f9b8166c353f9efc8568f23e0e7097b377b7262b6760e4`  
		Last Modified: Thu, 02 Dec 2021 11:27:07 GMT  
		Size: 64.3 MB (64274378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a542d7e95c600a3406e83cd2559e350c9150e5b25ab9d81ae46175c9d43946b`  
		Last Modified: Thu, 02 Dec 2021 11:26:56 GMT  
		Size: 5.6 KB (5557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06fd3c106aea0b66a10ea46b175252011a658f956b207c128bdfec73e96af24`  
		Last Modified: Thu, 02 Dec 2021 11:26:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.51`

```console
$ docker pull mysql@sha256:d0822b1b059e59fef7571b1a96224fb59fb0a84dffa59d8f3859281bde675a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.6.51` - linux; amd64

```console
$ docker pull mysql@sha256:99d967e2880d67c5bc8a57813c29a291787457ffb91c74a4b9022b1833552df2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102979190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0befd40a091b063217be99ee9d87167851bc5c8c07fbe9a36d24567ece493a87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:24:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 02 Dec 2021 11:24:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:24:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 02 Dec 2021 11:24:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Dec 2021 11:24:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Dec 2021 11:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:24:48 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 02 Dec 2021 11:24:49 GMT
ENV MYSQL_MAJOR=5.6
# Thu, 02 Dec 2021 11:24:49 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Thu, 02 Dec 2021 11:24:50 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Thu, 02 Dec 2021 11:25:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 02 Dec 2021 11:25:07 GMT
VOLUME [/var/lib/mysql]
# Thu, 02 Dec 2021 11:25:08 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 02 Dec 2021 11:25:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 11:25:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 11:25:09 GMT
EXPOSE 3306
# Thu, 02 Dec 2021 11:25:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea446d3dd1a4fecc95ccdd97fd45e8f8401c751bd179b8115b35eca27179b3d`  
		Last Modified: Thu, 02 Dec 2021 11:27:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12b9de3971c6380773d4b420862a84d67fddefc511def03fe28082879770f90`  
		Last Modified: Thu, 02 Dec 2021 11:27:00 GMT  
		Size: 4.5 MB (4503815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cece02ee84c4f223dae24907324f34bf2f3943c84bf3257e3d5dee0df42855a`  
		Last Modified: Thu, 02 Dec 2021 11:27:00 GMT  
		Size: 1.4 MB (1412253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81584261ce182d915ab20a0834bfd844792b0c324fcf8a585171bf7ecde9e91a`  
		Last Modified: Thu, 02 Dec 2021 11:26:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a511d4a684485e250407a3b84b99ed670c28287f5d734f6a4dd20659c06a4f7d`  
		Last Modified: Thu, 02 Dec 2021 11:27:02 GMT  
		Size: 10.2 MB (10225793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2451f19813d4b19ca00ec4f70055d75e8978d28689fc1e8b0d3e81315d6e69`  
		Last Modified: Thu, 02 Dec 2021 11:26:56 GMT  
		Size: 26.1 KB (26079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d341343e375fd5892ba0cd3128489bc8952950c842bbf5226ea4c3a58dc99f`  
		Last Modified: Thu, 02 Dec 2021 11:26:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde17f57816b6c25e9f9b8166c353f9efc8568f23e0e7097b377b7262b6760e4`  
		Last Modified: Thu, 02 Dec 2021 11:27:07 GMT  
		Size: 64.3 MB (64274378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a542d7e95c600a3406e83cd2559e350c9150e5b25ab9d81ae46175c9d43946b`  
		Last Modified: Thu, 02 Dec 2021 11:26:56 GMT  
		Size: 5.6 KB (5557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06fd3c106aea0b66a10ea46b175252011a658f956b207c128bdfec73e96af24`  
		Last Modified: Thu, 02 Dec 2021 11:26:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:d1cc87a3bd5dc07defc837bc9084f748a130606ff41923f46dec1986e0dc828d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:9415bfb9a83752d30b6395c84dde03573eeba7b5b9c937c0e09c3e7b32c76c93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154849221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e7101490b45decf606211a5437ed87aa6a82f1ff03c354564bf9375ce20f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:22:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 02 Dec 2021 11:22:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:22:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 02 Dec 2021 11:22:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Dec 2021 11:22:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Dec 2021 11:22:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:23:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 02 Dec 2021 11:23:43 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 02 Dec 2021 11:23:44 GMT
ENV MYSQL_VERSION=5.7.36-1debian10
# Thu, 02 Dec 2021 11:23:45 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 02 Dec 2021 11:24:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 02 Dec 2021 11:24:07 GMT
VOLUME [/var/lib/mysql]
# Thu, 02 Dec 2021 11:24:07 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 02 Dec 2021 11:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 11:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 11:24:08 GMT
EXPOSE 3306 33060
# Thu, 02 Dec 2021 11:24:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df186527fc4698f1a41fbbdaec1ae1c7e76b2b4fd34e8750db82f5c9dd1cf7da`  
		Last Modified: Thu, 02 Dec 2021 11:25:45 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa362a6aa7bd8aef47b5fa3c7d6c907f5d87f315792e677d2d1fce86258d6861`  
		Last Modified: Thu, 02 Dec 2021 11:25:46 GMT  
		Size: 4.2 MB (4179256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7cb1a200e984186d41ea2204b7bc8d81442cf59a2e2bf61c4625f43d9c8b3`  
		Last Modified: Thu, 02 Dec 2021 11:25:43 GMT  
		Size: 1.4 MB (1419462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949da226cc6d2b8a906157e7fc547dc4319d01e823bf8f872d6e516cd3c0ec9b`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce007079ee9d2f73484aa3a0c51ea4b93aece5b247df45045ceb5a944b9c18f`  
		Last Modified: Thu, 02 Dec 2021 11:25:47 GMT  
		Size: 13.4 MB (13448631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9f076e5a305da5cad538c80c188e0af815aa2d7fc5d4c20dfabe0fa7c907d`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b24c3f27affc7c0d6dc7f5e36582cfa4340f9cc85ad9d4c68baa344e6c7a52`  
		Last Modified: Thu, 02 Dec 2021 11:26:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc26ff6705a0608cf6da9ca3fbebaa0ea0bc39a60fb64843b34766447795b65`  
		Last Modified: Thu, 02 Dec 2021 11:26:42 GMT  
		Size: 108.6 MB (108637986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec5cdb5e7f7ae379b1884607863586b13219683657a4b6464574b5490a9bc60`  
		Last Modified: Thu, 02 Dec 2021 11:26:22 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1cb25f7525f2aa38e78d08c43df603fb33d3a74eaf4f7f54d5272582175f9c`  
		Last Modified: Thu, 02 Dec 2021 11:26:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.36`

```console
$ docker pull mysql@sha256:d1cc87a3bd5dc07defc837bc9084f748a130606ff41923f46dec1986e0dc828d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.36` - linux; amd64

```console
$ docker pull mysql@sha256:9415bfb9a83752d30b6395c84dde03573eeba7b5b9c937c0e09c3e7b32c76c93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154849221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e7101490b45decf606211a5437ed87aa6a82f1ff03c354564bf9375ce20f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:22:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 02 Dec 2021 11:22:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:22:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 02 Dec 2021 11:22:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Dec 2021 11:22:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Dec 2021 11:22:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:23:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 02 Dec 2021 11:23:43 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 02 Dec 2021 11:23:44 GMT
ENV MYSQL_VERSION=5.7.36-1debian10
# Thu, 02 Dec 2021 11:23:45 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 02 Dec 2021 11:24:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 02 Dec 2021 11:24:07 GMT
VOLUME [/var/lib/mysql]
# Thu, 02 Dec 2021 11:24:07 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 02 Dec 2021 11:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 11:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 11:24:08 GMT
EXPOSE 3306 33060
# Thu, 02 Dec 2021 11:24:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df186527fc4698f1a41fbbdaec1ae1c7e76b2b4fd34e8750db82f5c9dd1cf7da`  
		Last Modified: Thu, 02 Dec 2021 11:25:45 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa362a6aa7bd8aef47b5fa3c7d6c907f5d87f315792e677d2d1fce86258d6861`  
		Last Modified: Thu, 02 Dec 2021 11:25:46 GMT  
		Size: 4.2 MB (4179256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7cb1a200e984186d41ea2204b7bc8d81442cf59a2e2bf61c4625f43d9c8b3`  
		Last Modified: Thu, 02 Dec 2021 11:25:43 GMT  
		Size: 1.4 MB (1419462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949da226cc6d2b8a906157e7fc547dc4319d01e823bf8f872d6e516cd3c0ec9b`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce007079ee9d2f73484aa3a0c51ea4b93aece5b247df45045ceb5a944b9c18f`  
		Last Modified: Thu, 02 Dec 2021 11:25:47 GMT  
		Size: 13.4 MB (13448631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9f076e5a305da5cad538c80c188e0af815aa2d7fc5d4c20dfabe0fa7c907d`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b24c3f27affc7c0d6dc7f5e36582cfa4340f9cc85ad9d4c68baa344e6c7a52`  
		Last Modified: Thu, 02 Dec 2021 11:26:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc26ff6705a0608cf6da9ca3fbebaa0ea0bc39a60fb64843b34766447795b65`  
		Last Modified: Thu, 02 Dec 2021 11:26:42 GMT  
		Size: 108.6 MB (108637986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec5cdb5e7f7ae379b1884607863586b13219683657a4b6464574b5490a9bc60`  
		Last Modified: Thu, 02 Dec 2021 11:26:22 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1cb25f7525f2aa38e78d08c43df603fb33d3a74eaf4f7f54d5272582175f9c`  
		Last Modified: Thu, 02 Dec 2021 11:26:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:ff9a288d1ecf4397967989b5d1ec269f7d9042a46fc8bc2c3ae35458c1a26727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:eb791004631abe3bf842b3597043318d19a91e8c86adca55a5f6d4d7b409f2ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151446665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf6571db4977fe13c3f4e6289c1409fc6f98c2899eabad39bfe07cad8f64f67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:22:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 02 Dec 2021 11:22:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:22:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 02 Dec 2021 11:22:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Dec 2021 11:22:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Dec 2021 11:22:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:23:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 02 Dec 2021 11:23:00 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 02 Dec 2021 11:23:00 GMT
ENV MYSQL_VERSION=8.0.27-1debian10
# Thu, 02 Dec 2021 11:23:02 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 02 Dec 2021 11:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 02 Dec 2021 11:23:27 GMT
VOLUME [/var/lib/mysql]
# Thu, 02 Dec 2021 11:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 02 Dec 2021 11:23:28 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 02 Dec 2021 11:23:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 11:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 11:23:31 GMT
EXPOSE 3306 33060
# Thu, 02 Dec 2021 11:23:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df186527fc4698f1a41fbbdaec1ae1c7e76b2b4fd34e8750db82f5c9dd1cf7da`  
		Last Modified: Thu, 02 Dec 2021 11:25:45 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa362a6aa7bd8aef47b5fa3c7d6c907f5d87f315792e677d2d1fce86258d6861`  
		Last Modified: Thu, 02 Dec 2021 11:25:46 GMT  
		Size: 4.2 MB (4179256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7cb1a200e984186d41ea2204b7bc8d81442cf59a2e2bf61c4625f43d9c8b3`  
		Last Modified: Thu, 02 Dec 2021 11:25:43 GMT  
		Size: 1.4 MB (1419462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949da226cc6d2b8a906157e7fc547dc4319d01e823bf8f872d6e516cd3c0ec9b`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce007079ee9d2f73484aa3a0c51ea4b93aece5b247df45045ceb5a944b9c18f`  
		Last Modified: Thu, 02 Dec 2021 11:25:47 GMT  
		Size: 13.4 MB (13448631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9f076e5a305da5cad538c80c188e0af815aa2d7fc5d4c20dfabe0fa7c907d`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57a7529e8dcb4fe5b9117cdb7ddefdfd8787aea3d3e454b2a90ebb6eab667d`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ccc6ed6fc70560de95b1be29c81fa8b7c7a59e4edadccba780276feeeeff7f`  
		Last Modified: Thu, 02 Dec 2021 11:26:03 GMT  
		Size: 105.2 MB (105234576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4af75e641696973711fd8e91ee49486798348135647eef01855ad9ee5d50300`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aed6a9cd68130351b239f734cadcb099290b15b66d4b18eef82f0c4fd406383`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23390142f76f55e001c182a477ec3befb0283aae2fc4368612bd22debf49b14f`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:ff9a288d1ecf4397967989b5d1ec269f7d9042a46fc8bc2c3ae35458c1a26727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:eb791004631abe3bf842b3597043318d19a91e8c86adca55a5f6d4d7b409f2ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151446665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf6571db4977fe13c3f4e6289c1409fc6f98c2899eabad39bfe07cad8f64f67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:22:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 02 Dec 2021 11:22:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:22:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 02 Dec 2021 11:22:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Dec 2021 11:22:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Dec 2021 11:22:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:23:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 02 Dec 2021 11:23:00 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 02 Dec 2021 11:23:00 GMT
ENV MYSQL_VERSION=8.0.27-1debian10
# Thu, 02 Dec 2021 11:23:02 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 02 Dec 2021 11:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 02 Dec 2021 11:23:27 GMT
VOLUME [/var/lib/mysql]
# Thu, 02 Dec 2021 11:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 02 Dec 2021 11:23:28 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 02 Dec 2021 11:23:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 11:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 11:23:31 GMT
EXPOSE 3306 33060
# Thu, 02 Dec 2021 11:23:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df186527fc4698f1a41fbbdaec1ae1c7e76b2b4fd34e8750db82f5c9dd1cf7da`  
		Last Modified: Thu, 02 Dec 2021 11:25:45 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa362a6aa7bd8aef47b5fa3c7d6c907f5d87f315792e677d2d1fce86258d6861`  
		Last Modified: Thu, 02 Dec 2021 11:25:46 GMT  
		Size: 4.2 MB (4179256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7cb1a200e984186d41ea2204b7bc8d81442cf59a2e2bf61c4625f43d9c8b3`  
		Last Modified: Thu, 02 Dec 2021 11:25:43 GMT  
		Size: 1.4 MB (1419462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949da226cc6d2b8a906157e7fc547dc4319d01e823bf8f872d6e516cd3c0ec9b`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce007079ee9d2f73484aa3a0c51ea4b93aece5b247df45045ceb5a944b9c18f`  
		Last Modified: Thu, 02 Dec 2021 11:25:47 GMT  
		Size: 13.4 MB (13448631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9f076e5a305da5cad538c80c188e0af815aa2d7fc5d4c20dfabe0fa7c907d`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57a7529e8dcb4fe5b9117cdb7ddefdfd8787aea3d3e454b2a90ebb6eab667d`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ccc6ed6fc70560de95b1be29c81fa8b7c7a59e4edadccba780276feeeeff7f`  
		Last Modified: Thu, 02 Dec 2021 11:26:03 GMT  
		Size: 105.2 MB (105234576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4af75e641696973711fd8e91ee49486798348135647eef01855ad9ee5d50300`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aed6a9cd68130351b239f734cadcb099290b15b66d4b18eef82f0c4fd406383`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23390142f76f55e001c182a477ec3befb0283aae2fc4368612bd22debf49b14f`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.27`

```console
$ docker pull mysql@sha256:ff9a288d1ecf4397967989b5d1ec269f7d9042a46fc8bc2c3ae35458c1a26727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.27` - linux; amd64

```console
$ docker pull mysql@sha256:eb791004631abe3bf842b3597043318d19a91e8c86adca55a5f6d4d7b409f2ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151446665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf6571db4977fe13c3f4e6289c1409fc6f98c2899eabad39bfe07cad8f64f67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:22:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 02 Dec 2021 11:22:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:22:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 02 Dec 2021 11:22:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Dec 2021 11:22:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Dec 2021 11:22:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:23:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 02 Dec 2021 11:23:00 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 02 Dec 2021 11:23:00 GMT
ENV MYSQL_VERSION=8.0.27-1debian10
# Thu, 02 Dec 2021 11:23:02 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 02 Dec 2021 11:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 02 Dec 2021 11:23:27 GMT
VOLUME [/var/lib/mysql]
# Thu, 02 Dec 2021 11:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 02 Dec 2021 11:23:28 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 02 Dec 2021 11:23:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 11:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 11:23:31 GMT
EXPOSE 3306 33060
# Thu, 02 Dec 2021 11:23:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df186527fc4698f1a41fbbdaec1ae1c7e76b2b4fd34e8750db82f5c9dd1cf7da`  
		Last Modified: Thu, 02 Dec 2021 11:25:45 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa362a6aa7bd8aef47b5fa3c7d6c907f5d87f315792e677d2d1fce86258d6861`  
		Last Modified: Thu, 02 Dec 2021 11:25:46 GMT  
		Size: 4.2 MB (4179256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7cb1a200e984186d41ea2204b7bc8d81442cf59a2e2bf61c4625f43d9c8b3`  
		Last Modified: Thu, 02 Dec 2021 11:25:43 GMT  
		Size: 1.4 MB (1419462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949da226cc6d2b8a906157e7fc547dc4319d01e823bf8f872d6e516cd3c0ec9b`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce007079ee9d2f73484aa3a0c51ea4b93aece5b247df45045ceb5a944b9c18f`  
		Last Modified: Thu, 02 Dec 2021 11:25:47 GMT  
		Size: 13.4 MB (13448631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9f076e5a305da5cad538c80c188e0af815aa2d7fc5d4c20dfabe0fa7c907d`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57a7529e8dcb4fe5b9117cdb7ddefdfd8787aea3d3e454b2a90ebb6eab667d`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ccc6ed6fc70560de95b1be29c81fa8b7c7a59e4edadccba780276feeeeff7f`  
		Last Modified: Thu, 02 Dec 2021 11:26:03 GMT  
		Size: 105.2 MB (105234576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4af75e641696973711fd8e91ee49486798348135647eef01855ad9ee5d50300`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aed6a9cd68130351b239f734cadcb099290b15b66d4b18eef82f0c4fd406383`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23390142f76f55e001c182a477ec3befb0283aae2fc4368612bd22debf49b14f`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:ff9a288d1ecf4397967989b5d1ec269f7d9042a46fc8bc2c3ae35458c1a26727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:eb791004631abe3bf842b3597043318d19a91e8c86adca55a5f6d4d7b409f2ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151446665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf6571db4977fe13c3f4e6289c1409fc6f98c2899eabad39bfe07cad8f64f67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:22:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 02 Dec 2021 11:22:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:22:28 GMT
ENV GOSU_VERSION=1.12
# Thu, 02 Dec 2021 11:22:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Dec 2021 11:22:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Dec 2021 11:22:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:23:00 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 02 Dec 2021 11:23:00 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 02 Dec 2021 11:23:00 GMT
ENV MYSQL_VERSION=8.0.27-1debian10
# Thu, 02 Dec 2021 11:23:02 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 02 Dec 2021 11:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 02 Dec 2021 11:23:27 GMT
VOLUME [/var/lib/mysql]
# Thu, 02 Dec 2021 11:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 02 Dec 2021 11:23:28 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 02 Dec 2021 11:23:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 11:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 11:23:31 GMT
EXPOSE 3306 33060
# Thu, 02 Dec 2021 11:23:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df186527fc4698f1a41fbbdaec1ae1c7e76b2b4fd34e8750db82f5c9dd1cf7da`  
		Last Modified: Thu, 02 Dec 2021 11:25:45 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa362a6aa7bd8aef47b5fa3c7d6c907f5d87f315792e677d2d1fce86258d6861`  
		Last Modified: Thu, 02 Dec 2021 11:25:46 GMT  
		Size: 4.2 MB (4179256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7cb1a200e984186d41ea2204b7bc8d81442cf59a2e2bf61c4625f43d9c8b3`  
		Last Modified: Thu, 02 Dec 2021 11:25:43 GMT  
		Size: 1.4 MB (1419462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949da226cc6d2b8a906157e7fc547dc4319d01e823bf8f872d6e516cd3c0ec9b`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce007079ee9d2f73484aa3a0c51ea4b93aece5b247df45045ceb5a944b9c18f`  
		Last Modified: Thu, 02 Dec 2021 11:25:47 GMT  
		Size: 13.4 MB (13448631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9f076e5a305da5cad538c80c188e0af815aa2d7fc5d4c20dfabe0fa7c907d`  
		Last Modified: Thu, 02 Dec 2021 11:25:42 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57a7529e8dcb4fe5b9117cdb7ddefdfd8787aea3d3e454b2a90ebb6eab667d`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ccc6ed6fc70560de95b1be29c81fa8b7c7a59e4edadccba780276feeeeff7f`  
		Last Modified: Thu, 02 Dec 2021 11:26:03 GMT  
		Size: 105.2 MB (105234576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4af75e641696973711fd8e91ee49486798348135647eef01855ad9ee5d50300`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aed6a9cd68130351b239f734cadcb099290b15b66d4b18eef82f0c4fd406383`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23390142f76f55e001c182a477ec3befb0283aae2fc4368612bd22debf49b14f`  
		Last Modified: Thu, 02 Dec 2021 11:25:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
