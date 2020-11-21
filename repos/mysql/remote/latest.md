## `mysql:latest`

```console
$ docker pull mysql@sha256:4bb2e81a40e9d0d59bd8e3dc2ba5e1f2197696f6de39a91e90798dd27299b093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:c8414a9528a0fff5dd44d7c9260e570258dc09c2548766400cd5cfc4dd384991
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158960115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7265748b5dc3211208fb9aa232cef8d3fefd5d9a2a80d87407b8ea649e571c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:15:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 18 Nov 2020 08:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:01 GMT
ENV GOSU_VERSION=1.12
# Wed, 18 Nov 2020 08:16:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 18 Nov 2020 08:16:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 18 Nov 2020 08:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:16:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 18 Nov 2020 08:16:21 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Sat, 21 Nov 2020 01:22:20 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 21 Nov 2020 01:22:35 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 21 Nov 2020 01:22:36 GMT
VOLUME [/var/lib/mysql]
# Sat, 21 Nov 2020 01:22:36 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 21 Nov 2020 01:22:36 GMT
COPY file:f9202f6b715c0e787fa285d215da39f3f4dd7166ae383f965856973633561803 in /usr/local/bin/ 
# Sat, 21 Nov 2020 01:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 21 Nov 2020 01:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:22:38 GMT
EXPOSE 3306 33060
# Sat, 21 Nov 2020 01:22:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29969ddb0ffb0ed3db2ce1f7fa289fb85495125b9e3469057b10f556ef65b8bb`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f41a44c48e6051d436face965bdfc38392fa9c75959c5cbe93cf50e7151ba`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd802543a34a27d237d3aff4faf5875692d521fe92d3accfee437343755da6`  
		Last Modified: Wed, 18 Nov 2020 08:19:18 GMT  
		Size: 1.4 MB (1419210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79b040de953d321965acb3b6f4564f8332dc90b096fef3fefb5513f3658fcab`  
		Last Modified: Wed, 18 Nov 2020 08:19:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c641199690039d482f076e9279d29bfac6b76331b4cfa974f86af8b14d076`  
		Last Modified: Wed, 18 Nov 2020 08:19:23 GMT  
		Size: 13.4 MB (13447061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7689ec51a0d96ba9a32db995a755b690fa76546c97e8ccc3c17a42968a49b363`  
		Last Modified: Wed, 18 Nov 2020 08:19:16 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a880ba7c411fa76cff7c85338d6ec8a2595ba8b9eab771a826011e9a8a517b58`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984f656ec6cade78263fa8887ad717d89ac8479de3826249ea8b679bcdcd5ca3`  
		Last Modified: Sat, 21 Nov 2020 01:24:32 GMT  
		Size: 112.8 MB (112799692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f497bce458aeb6b738fe4d5763b444231390efa450c28361a91fe8c337c5b89`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f97694b93ca77fab22010d3d964c1909cedeab8750a60942c2a5c38f4a1`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f069358dc963e6a16b7891e1002c991fe4f9653997ef005f1b570dac4921d9a`  
		Last Modified: Sat, 21 Nov 2020 01:23:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
