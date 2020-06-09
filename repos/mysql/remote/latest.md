## `mysql:latest`

```console
$ docker pull mysql@sha256:8b7b328a7ff6de46ef96bcf83af048cb00a1c86282bfca0cb119c84568b4caf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:0ba38ea9c478d1e98b2f0bc0cee5a62345c9f06f78c4b48123bdc70d8d224686
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157635446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0dbf01a0f3f46fc8c88b67696e74e7005c3e16d9071032fa0cd89773771576`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:20:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 Jun 2020 07:20:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:20:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Jun 2020 07:20:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Jun 2020 07:20:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Jun 2020 07:20:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:20:32 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 09 Jun 2020 07:20:32 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 09 Jun 2020 07:20:32 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Tue, 09 Jun 2020 07:20:33 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 09 Jun 2020 07:20:49 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 09 Jun 2020 07:20:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 09 Jun 2020 07:20:50 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 09 Jun 2020 07:20:50 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:20:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 07:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:20:51 GMT
EXPOSE 3306 33060
# Tue, 09 Jun 2020 07:20:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51ce1c2e5758ad66758028c37b3224bff94ee2cdb716215a91dde7b754443f3`  
		Last Modified: Tue, 09 Jun 2020 07:22:27 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2344adc4858d61b5c9424d49320703bec8d5e1044378a83cae39dbdc49acba7`  
		Last Modified: Tue, 09 Jun 2020 07:22:28 GMT  
		Size: 4.2 MB (4178032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf3ceff18fca19f16c7108d4c0dfcacc194f1762f80712e854c16ec164733aa`  
		Last Modified: Tue, 09 Jun 2020 07:22:26 GMT  
		Size: 1.4 MB (1419203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16da0c38dc5bad1047f9912514e8232bf9d4d40c3790e94e9c25d5f48ac39ffd`  
		Last Modified: Tue, 09 Jun 2020 07:22:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b905d1797e97cbecb5a12655cab5c3df92736805574af0f96477c98d7a27411c`  
		Last Modified: Tue, 09 Jun 2020 07:22:30 GMT  
		Size: 13.4 MB (13442691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b50d1c6b05cfc51651f145028c85c8eb3a5c8c02b0c4537aad065ad3083150d`  
		Last Modified: Tue, 09 Jun 2020 07:22:25 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75914a65ca227bf8a305dcc9e91a46cf9ac85098e6136f052121370d2ba02c2`  
		Last Modified: Tue, 09 Jun 2020 07:22:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae8042bdd096b7a5e2e85ca88e744eb2d61896749e1643411ff1af2b1929aef`  
		Last Modified: Tue, 09 Jun 2020 07:22:45 GMT  
		Size: 111.5 MB (111486634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453ac13c00a353d3106bf14a375cab7f6661ec7c4854528091ff3cc20184c3bd`  
		Last Modified: Tue, 09 Jun 2020 07:22:24 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e680cd72f08cd6cb9db395c62485983f6892234f83bbf35a27f5f80f1f6e568`  
		Last Modified: Tue, 09 Jun 2020 07:22:24 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b5dc864b6c283cb3dc29c66714099ef6103a1f5de7923a5c1ea63e6d597279`  
		Last Modified: Tue, 09 Jun 2020 07:22:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
