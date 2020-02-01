## `mysql:latest`

```console
$ docker pull mysql@sha256:6d0741319b6a2ae22c384a97f4bbee411b01e75f6284af0cce339fee83d7e314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:283caa87ee6a3997b32beaff33e75974fd689edfd2df0084a45e300d8a001c91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136675903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791b6e40940cd550af522eb4ffe995226798204504fe495743445b900e417a51`
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
# Sat, 01 Feb 2020 18:05:29 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 01 Feb 2020 18:05:30 GMT
ENV MYSQL_VERSION=8.0.19-1debian9
# Sat, 01 Feb 2020 18:05:31 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 01 Feb 2020 18:05:58 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Sat, 01 Feb 2020 18:05:58 GMT
VOLUME [/var/lib/mysql]
# Sat, 01 Feb 2020 18:05:58 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Sat, 01 Feb 2020 18:05:59 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 01 Feb 2020 18:06:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 01 Feb 2020 18:06:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 01 Feb 2020 18:06:01 GMT
EXPOSE 3306 33060
# Sat, 01 Feb 2020 18:06:01 GMT
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
	-	`sha256:f18efbfd8d762328a60333c4c29d2f5db3968ef3ecff4aaf56471ff65fd7f046`  
		Last Modified: Sat, 01 Feb 2020 18:07:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012b302865d12ccfe20948b63764422e03fd4b08590b8c351bd368874d1e243b`  
		Last Modified: Sat, 01 Feb 2020 18:08:26 GMT  
		Size: 96.2 MB (96236360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe16fd240f59f8bdc9971638966d1074826e4af16b6b4bf91b85fabfc574b134`  
		Last Modified: Sat, 01 Feb 2020 18:07:59 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3e793e545e1d356fb2697657776d4b3de1598566b62d88363df9b9a890cf0a`  
		Last Modified: Sat, 01 Feb 2020 18:07:59 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d0f2cb26105bfba2f7c9181187279c3f2744561ba56bda0496af63046c8658`  
		Last Modified: Sat, 01 Feb 2020 18:07:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
