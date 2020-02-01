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
$ docker pull mysql@sha256:cf6899e980c38071a78ded028de40e65286bfbbb746b97617ac4c9a84c4e812d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:5e443fc090c75413ffc20665ed1880c7961bc6af8ae8997510fdd7e69d8557ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151942195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f186b9e038c856c5fb5f6b27ca106db3cc064594b7e5706d0350a3ab6220db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:04:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 01 Feb 2020 18:04:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:04:57 GMT
ENV GOSU_VERSION=1.7
# Sat, 01 Feb 2020 18:05:13 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 01 Feb 2020 18:05:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 01 Feb 2020 18:05:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:05:29 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 01 Feb 2020 18:06:18 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 01 Feb 2020 18:06:18 GMT
ENV MYSQL_VERSION=5.7.29-1debian9
# Sat, 01 Feb 2020 18:06:19 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 01 Feb 2020 18:06:45 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 01 Feb 2020 18:06:45 GMT
VOLUME [/var/lib/mysql]
# Sat, 01 Feb 2020 18:06:45 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 01 Feb 2020 18:06:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 01 Feb 2020 18:06:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 01 Feb 2020 18:06:47 GMT
EXPOSE 3306 33060
# Sat, 01 Feb 2020 18:06:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced578c3a5f5e96f33315bb936d3d0bac30f734e820759f370ef0a6fcbd8639`  
		Last Modified: Sat, 01 Feb 2020 18:08:01 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731f6e13d8ea683b85c2d516659def2ada874d12198ccb8aa607b0739cad71f9`  
		Last Modified: Sat, 01 Feb 2020 18:08:03 GMT  
		Size: 4.5 MB (4501283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c183de42679fb8b24485807f24d4d5e83833a5df99f2a1e22b9995d5a77a61c`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 1.3 MB (1270478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de69b5c2f3c8d53585c798ec208eb58375608c919d5b70da51c3e4fcbb90e93`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f0a408640647834fda76cee6930f13533e390421718120cea71b70f5198d3f`  
		Last Modified: Sat, 01 Feb 2020 18:08:07 GMT  
		Size: 12.1 MB (12106622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d93aea836d142026e4ed7c40ea7db85d80b1a069d4f707fde380d0a49cd005`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dd1f3e5a3d2587ba4a313ec73b350e749e399593f8133669ef0149c55503d0`  
		Last Modified: Sat, 01 Feb 2020 18:08:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fb37478ee6532cf6b44e9fa0ba6c3c9075897f7bdf987abf9fbde70ef0eb8f`  
		Last Modified: Sat, 01 Feb 2020 18:08:55 GMT  
		Size: 111.5 MB (111503550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eb21662ebf680659904f1a75810888cc7c18f678de7813baf7642dac0045d8`  
		Last Modified: Sat, 01 Feb 2020 18:08:32 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95057f0a050dfa61bfc86a7c81e725b2b3535cf19a42da20ec13a0c1d210a36`  
		Last Modified: Sat, 01 Feb 2020 18:08:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:bef096aee20d73cbfd87b02856321040ab1127e94b707b41927804776dca02fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:a0314038cc8ca294ac2cacd6f358cd473915b3c2c46f09652ac7b398d6cdc6c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102689503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edea6175b4cb318a108be8f1a004abe2e18678b54d3336a7388a6fd4428a23d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:04:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 01 Feb 2020 18:04:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:04:57 GMT
ENV GOSU_VERSION=1.7
# Sat, 01 Feb 2020 18:05:13 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 01 Feb 2020 18:05:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 01 Feb 2020 18:07:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:07:09 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 01 Feb 2020 18:07:10 GMT
ENV MYSQL_MAJOR=5.6
# Sat, 01 Feb 2020 18:07:10 GMT
ENV MYSQL_VERSION=5.6.47-1debian9
# Sat, 01 Feb 2020 18:07:11 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 01 Feb 2020 18:07:37 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 01 Feb 2020 18:07:38 GMT
VOLUME [/var/lib/mysql]
# Sat, 01 Feb 2020 18:07:38 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 01 Feb 2020 18:07:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 01 Feb 2020 18:07:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 01 Feb 2020 18:07:39 GMT
EXPOSE 3306
# Sat, 01 Feb 2020 18:07:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced578c3a5f5e96f33315bb936d3d0bac30f734e820759f370ef0a6fcbd8639`  
		Last Modified: Sat, 01 Feb 2020 18:08:01 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731f6e13d8ea683b85c2d516659def2ada874d12198ccb8aa607b0739cad71f9`  
		Last Modified: Sat, 01 Feb 2020 18:08:03 GMT  
		Size: 4.5 MB (4501283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c183de42679fb8b24485807f24d4d5e83833a5df99f2a1e22b9995d5a77a61c`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 1.3 MB (1270478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de69b5c2f3c8d53585c798ec208eb58375608c919d5b70da51c3e4fcbb90e93`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1320f6ed12d9642293174877aaa3bd29b0f9ab62dec86da3af896e19468a37`  
		Last Modified: Sat, 01 Feb 2020 18:09:07 GMT  
		Size: 10.2 MB (10168845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba5914ee9f79f15016cdea6da47be38a6fb194c1167b1324c341defc38452fa`  
		Last Modified: Sat, 01 Feb 2020 18:09:01 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cce9dedb8089adf2c521ddf4482398557fa87c13e2faeaeedc839cd4435f1e`  
		Last Modified: Sat, 01 Feb 2020 18:09:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf48d14817eb94981258d74226e5f15277cf9d0f269c48f2fe141315f71720`  
		Last Modified: Sat, 01 Feb 2020 18:09:18 GMT  
		Size: 64.2 MB (64188630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b6601d449a9bd120cea91c657c402849ae4f4ecbf6ecf5a6a302a747ee8c14`  
		Last Modified: Sat, 01 Feb 2020 18:09:01 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f046f35afad247c5c6262520d4f7174673401ddc9874f47376766456f46cb4`  
		Last Modified: Sat, 01 Feb 2020 18:09:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.47`

```console
$ docker pull mysql@sha256:bef096aee20d73cbfd87b02856321040ab1127e94b707b41927804776dca02fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.47` - linux; amd64

```console
$ docker pull mysql@sha256:a0314038cc8ca294ac2cacd6f358cd473915b3c2c46f09652ac7b398d6cdc6c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102689503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edea6175b4cb318a108be8f1a004abe2e18678b54d3336a7388a6fd4428a23d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:04:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 01 Feb 2020 18:04:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:04:57 GMT
ENV GOSU_VERSION=1.7
# Sat, 01 Feb 2020 18:05:13 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 01 Feb 2020 18:05:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 01 Feb 2020 18:07:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:07:09 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 01 Feb 2020 18:07:10 GMT
ENV MYSQL_MAJOR=5.6
# Sat, 01 Feb 2020 18:07:10 GMT
ENV MYSQL_VERSION=5.6.47-1debian9
# Sat, 01 Feb 2020 18:07:11 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 01 Feb 2020 18:07:37 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 01 Feb 2020 18:07:38 GMT
VOLUME [/var/lib/mysql]
# Sat, 01 Feb 2020 18:07:38 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 01 Feb 2020 18:07:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 01 Feb 2020 18:07:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 01 Feb 2020 18:07:39 GMT
EXPOSE 3306
# Sat, 01 Feb 2020 18:07:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced578c3a5f5e96f33315bb936d3d0bac30f734e820759f370ef0a6fcbd8639`  
		Last Modified: Sat, 01 Feb 2020 18:08:01 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731f6e13d8ea683b85c2d516659def2ada874d12198ccb8aa607b0739cad71f9`  
		Last Modified: Sat, 01 Feb 2020 18:08:03 GMT  
		Size: 4.5 MB (4501283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c183de42679fb8b24485807f24d4d5e83833a5df99f2a1e22b9995d5a77a61c`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 1.3 MB (1270478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de69b5c2f3c8d53585c798ec208eb58375608c919d5b70da51c3e4fcbb90e93`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1320f6ed12d9642293174877aaa3bd29b0f9ab62dec86da3af896e19468a37`  
		Last Modified: Sat, 01 Feb 2020 18:09:07 GMT  
		Size: 10.2 MB (10168845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba5914ee9f79f15016cdea6da47be38a6fb194c1167b1324c341defc38452fa`  
		Last Modified: Sat, 01 Feb 2020 18:09:01 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cce9dedb8089adf2c521ddf4482398557fa87c13e2faeaeedc839cd4435f1e`  
		Last Modified: Sat, 01 Feb 2020 18:09:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf48d14817eb94981258d74226e5f15277cf9d0f269c48f2fe141315f71720`  
		Last Modified: Sat, 01 Feb 2020 18:09:18 GMT  
		Size: 64.2 MB (64188630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b6601d449a9bd120cea91c657c402849ae4f4ecbf6ecf5a6a302a747ee8c14`  
		Last Modified: Sat, 01 Feb 2020 18:09:01 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f046f35afad247c5c6262520d4f7174673401ddc9874f47376766456f46cb4`  
		Last Modified: Sat, 01 Feb 2020 18:09:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:cf6899e980c38071a78ded028de40e65286bfbbb746b97617ac4c9a84c4e812d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:5e443fc090c75413ffc20665ed1880c7961bc6af8ae8997510fdd7e69d8557ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151942195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f186b9e038c856c5fb5f6b27ca106db3cc064594b7e5706d0350a3ab6220db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:04:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 01 Feb 2020 18:04:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:04:57 GMT
ENV GOSU_VERSION=1.7
# Sat, 01 Feb 2020 18:05:13 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 01 Feb 2020 18:05:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 01 Feb 2020 18:05:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:05:29 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 01 Feb 2020 18:06:18 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 01 Feb 2020 18:06:18 GMT
ENV MYSQL_VERSION=5.7.29-1debian9
# Sat, 01 Feb 2020 18:06:19 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 01 Feb 2020 18:06:45 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 01 Feb 2020 18:06:45 GMT
VOLUME [/var/lib/mysql]
# Sat, 01 Feb 2020 18:06:45 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 01 Feb 2020 18:06:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 01 Feb 2020 18:06:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 01 Feb 2020 18:06:47 GMT
EXPOSE 3306 33060
# Sat, 01 Feb 2020 18:06:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced578c3a5f5e96f33315bb936d3d0bac30f734e820759f370ef0a6fcbd8639`  
		Last Modified: Sat, 01 Feb 2020 18:08:01 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731f6e13d8ea683b85c2d516659def2ada874d12198ccb8aa607b0739cad71f9`  
		Last Modified: Sat, 01 Feb 2020 18:08:03 GMT  
		Size: 4.5 MB (4501283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c183de42679fb8b24485807f24d4d5e83833a5df99f2a1e22b9995d5a77a61c`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 1.3 MB (1270478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de69b5c2f3c8d53585c798ec208eb58375608c919d5b70da51c3e4fcbb90e93`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f0a408640647834fda76cee6930f13533e390421718120cea71b70f5198d3f`  
		Last Modified: Sat, 01 Feb 2020 18:08:07 GMT  
		Size: 12.1 MB (12106622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d93aea836d142026e4ed7c40ea7db85d80b1a069d4f707fde380d0a49cd005`  
		Last Modified: Sat, 01 Feb 2020 18:08:00 GMT  
		Size: 28.3 KB (28324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dd1f3e5a3d2587ba4a313ec73b350e749e399593f8133669ef0149c55503d0`  
		Last Modified: Sat, 01 Feb 2020 18:08:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fb37478ee6532cf6b44e9fa0ba6c3c9075897f7bdf987abf9fbde70ef0eb8f`  
		Last Modified: Sat, 01 Feb 2020 18:08:55 GMT  
		Size: 111.5 MB (111503550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eb21662ebf680659904f1a75810888cc7c18f678de7813baf7642dac0045d8`  
		Last Modified: Sat, 01 Feb 2020 18:08:32 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95057f0a050dfa61bfc86a7c81e725b2b3535cf19a42da20ec13a0c1d210a36`  
		Last Modified: Sat, 01 Feb 2020 18:08:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.29`

```console
$ docker pull mysql@sha256:2ca675966612f34b4036bbcfa68cb049c03e34b561fba0f88954b03931823d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.29` - linux; amd64

```console
$ docker pull mysql@sha256:52a28dff3b3ef81d48765f67324629de3c090e9cd8d7c882e2459c4bb778c12d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151941822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b598110d0fffc42862269a25d8767dd95764d0740f318fd6c0a097f8a22de5bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 23:00:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 14 Jan 2020 23:21:03 GMT
ENV MYSQL_VERSION=5.7.29-1debian9
# Tue, 14 Jan 2020 23:21:04 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 14 Jan 2020 23:21:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 14 Jan 2020 23:21:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jan 2020 23:21:27 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Tue, 14 Jan 2020 23:21:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Jan 2020 23:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2020 23:21:28 GMT
EXPOSE 3306 33060
# Tue, 14 Jan 2020 23:21:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e05241b77072e8d9d6ce70a65014881839c28e5bbf5f3d930dfb5af29804e73`  
		Last Modified: Tue, 14 Jan 2020 23:22:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822978df8f02c93747ef8a574ee964cd3718c337f082aee04f7b4fd0bb25c39`  
		Last Modified: Tue, 14 Jan 2020 23:22:48 GMT  
		Size: 111.5 MB (111503380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ca71ed53beb374dea871458609da3d1a584395cc5c582348b831df4ff9a01b`  
		Last Modified: Tue, 14 Jan 2020 23:22:31 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026afe6fd35e7b9f0669dd078d39f95e7761cb5394b387d4af8d834d6f957685`  
		Last Modified: Tue, 14 Jan 2020 23:22:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:f1df505c4c6e8eae599a0482e3bde3e761cd700c00cbc371a8161648a26817c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:0b2b26a2eefaf5bd0951a4a37e158f4728db3cc53c02926535ba6618c1fcc8df
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136675781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5e53f6328162f8d8bc70131658a721e8e7dcf7495f2fae7cfe4febdbcfefbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jan 2020 23:20:39 GMT
ENV MYSQL_VERSION=8.0.19-1debian9
# Tue, 14 Jan 2020 23:20:40 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 14 Jan 2020 23:20:56 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 14 Jan 2020 23:20:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jan 2020 23:20:56 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 14 Jan 2020 23:20:57 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Tue, 14 Jan 2020 23:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Jan 2020 23:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2020 23:20:58 GMT
EXPOSE 3306 33060
# Tue, 14 Jan 2020 23:20:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e039ec97e84719d8db3f9fca23d0c0379d383a3ceebca9a971c7f4eab76f201c`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda57f041c16e944779513e0f3b4bc66c4a9a66bf3b301dbb9448f1cb0791ad`  
		Last Modified: Tue, 14 Jan 2020 23:22:26 GMT  
		Size: 96.2 MB (96236435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70ca9049b7732c6f077c6eaef767e2748ce0e1bfb0ccc07da5334d9571de52f`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ecde006e59b693a1be957615d07dab57f923d53cfd498936134e5be822e038`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7def2a4ede73aa23dec74a6d99501a9f7737610e5ecb5c14b4c53ed1ac8b2984`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:f1df505c4c6e8eae599a0482e3bde3e761cd700c00cbc371a8161648a26817c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:0b2b26a2eefaf5bd0951a4a37e158f4728db3cc53c02926535ba6618c1fcc8df
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136675781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5e53f6328162f8d8bc70131658a721e8e7dcf7495f2fae7cfe4febdbcfefbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jan 2020 23:20:39 GMT
ENV MYSQL_VERSION=8.0.19-1debian9
# Tue, 14 Jan 2020 23:20:40 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 14 Jan 2020 23:20:56 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 14 Jan 2020 23:20:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jan 2020 23:20:56 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 14 Jan 2020 23:20:57 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Tue, 14 Jan 2020 23:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Jan 2020 23:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2020 23:20:58 GMT
EXPOSE 3306 33060
# Tue, 14 Jan 2020 23:20:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e039ec97e84719d8db3f9fca23d0c0379d383a3ceebca9a971c7f4eab76f201c`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda57f041c16e944779513e0f3b4bc66c4a9a66bf3b301dbb9448f1cb0791ad`  
		Last Modified: Tue, 14 Jan 2020 23:22:26 GMT  
		Size: 96.2 MB (96236435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70ca9049b7732c6f077c6eaef767e2748ce0e1bfb0ccc07da5334d9571de52f`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ecde006e59b693a1be957615d07dab57f923d53cfd498936134e5be822e038`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7def2a4ede73aa23dec74a6d99501a9f7737610e5ecb5c14b4c53ed1ac8b2984`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.19`

```console
$ docker pull mysql@sha256:f1df505c4c6e8eae599a0482e3bde3e761cd700c00cbc371a8161648a26817c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.19` - linux; amd64

```console
$ docker pull mysql@sha256:0b2b26a2eefaf5bd0951a4a37e158f4728db3cc53c02926535ba6618c1fcc8df
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136675781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5e53f6328162f8d8bc70131658a721e8e7dcf7495f2fae7cfe4febdbcfefbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jan 2020 23:20:39 GMT
ENV MYSQL_VERSION=8.0.19-1debian9
# Tue, 14 Jan 2020 23:20:40 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 14 Jan 2020 23:20:56 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 14 Jan 2020 23:20:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jan 2020 23:20:56 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 14 Jan 2020 23:20:57 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Tue, 14 Jan 2020 23:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Jan 2020 23:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2020 23:20:58 GMT
EXPOSE 3306 33060
# Tue, 14 Jan 2020 23:20:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e039ec97e84719d8db3f9fca23d0c0379d383a3ceebca9a971c7f4eab76f201c`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda57f041c16e944779513e0f3b4bc66c4a9a66bf3b301dbb9448f1cb0791ad`  
		Last Modified: Tue, 14 Jan 2020 23:22:26 GMT  
		Size: 96.2 MB (96236435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70ca9049b7732c6f077c6eaef767e2748ce0e1bfb0ccc07da5334d9571de52f`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ecde006e59b693a1be957615d07dab57f923d53cfd498936134e5be822e038`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7def2a4ede73aa23dec74a6d99501a9f7737610e5ecb5c14b4c53ed1ac8b2984`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:f1df505c4c6e8eae599a0482e3bde3e761cd700c00cbc371a8161648a26817c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:0b2b26a2eefaf5bd0951a4a37e158f4728db3cc53c02926535ba6618c1fcc8df
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136675781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5e53f6328162f8d8bc70131658a721e8e7dcf7495f2fae7cfe4febdbcfefbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jan 2020 23:20:39 GMT
ENV MYSQL_VERSION=8.0.19-1debian9
# Tue, 14 Jan 2020 23:20:40 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 14 Jan 2020 23:20:56 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 14 Jan 2020 23:20:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jan 2020 23:20:56 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 14 Jan 2020 23:20:57 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Tue, 14 Jan 2020 23:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Jan 2020 23:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jan 2020 23:20:58 GMT
EXPOSE 3306 33060
# Tue, 14 Jan 2020 23:20:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e039ec97e84719d8db3f9fca23d0c0379d383a3ceebca9a971c7f4eab76f201c`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda57f041c16e944779513e0f3b4bc66c4a9a66bf3b301dbb9448f1cb0791ad`  
		Last Modified: Tue, 14 Jan 2020 23:22:26 GMT  
		Size: 96.2 MB (96236435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70ca9049b7732c6f077c6eaef767e2748ce0e1bfb0ccc07da5334d9571de52f`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ecde006e59b693a1be957615d07dab57f923d53cfd498936134e5be822e038`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7def2a4ede73aa23dec74a6d99501a9f7737610e5ecb5c14b4c53ed1ac8b2984`  
		Last Modified: Tue, 14 Jan 2020 23:22:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
