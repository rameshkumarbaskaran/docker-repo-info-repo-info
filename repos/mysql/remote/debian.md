## `mysql:debian`

```console
$ docker pull mysql@sha256:c26ffcfefadf3698514de6e8e8b3566cd0da5b8a9ee3543ea0eb44bc5faab6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:2f7872dbcb701e16397e23e368148ee9411027cd4baf5905d0622ccccc35092e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177766717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88e52842dfbc5faff99e03317eb17892293cd424cd745e74ec04408ba255207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 08:16:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 01 Mar 2023 08:16:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:16:56 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Mar 2023 08:17:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 08:17:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 01 Mar 2023 08:17:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:17:11 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 01 Mar 2023 08:17:12 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 Mar 2023 08:17:12 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Wed, 01 Mar 2023 08:17:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 01 Mar 2023 08:17:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 01 Mar 2023 08:17:28 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Mar 2023 08:17:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 01 Mar 2023 08:17:28 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Mar 2023 08:17:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 08:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 08:17:29 GMT
EXPOSE 3306 33060
# Wed, 01 Mar 2023 08:17:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f99c7c3059a32499d51cb02152df032fc466298a3e2b7e600029b9b91f4ea`  
		Last Modified: Wed, 01 Mar 2023 08:18:54 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d20338c318a65cc44a3e0a1a60cb9c690d286ff757ea0b3a976bf24748a0316`  
		Last Modified: Wed, 01 Mar 2023 08:18:54 GMT  
		Size: 4.4 MB (4414965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e92be7428ec909fce6a3b308505a95430380d7b319e454a1eb04c11f33522f7`  
		Last Modified: Wed, 01 Mar 2023 08:18:52 GMT  
		Size: 1.5 MB (1471440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c491527f8245e4dc5378618790c15c6885747848d85b17bcb6dce84ad2ff88`  
		Last Modified: Wed, 01 Mar 2023 08:18:51 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab5d3f904fbf665f9b72bfad9092bce3e58555608293d61f421931eaf99f80`  
		Last Modified: Wed, 01 Mar 2023 08:18:54 GMT  
		Size: 12.7 MB (12661962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0764a75d4948f4bc90025d5a92b44e3ff0372e8798b456860ee310dd9bb3e52f`  
		Last Modified: Wed, 01 Mar 2023 08:18:51 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abceaa621503b0635e2b0e9740dfe37f20b0c42d1d17615caebdc44f5f05949f`  
		Last Modified: Wed, 01 Mar 2023 08:18:50 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a8f23f9143940d284a3ff2c1767c607db5bfe4652eb720a811f902a4188707`  
		Last Modified: Wed, 01 Mar 2023 08:19:09 GMT  
		Size: 127.8 MB (127795909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad9bee7b38020e4c875fff67ed05f30ab2e771c0db576fe03213199b20dec0`  
		Last Modified: Wed, 01 Mar 2023 08:18:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdbfd558513023768b43219f0840d9f390b92f42e0249e9051a7dd596965f7b`  
		Last Modified: Wed, 01 Mar 2023 08:18:50 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6b54fce3b52f5381a599e59836f8faf08f2c8077888bdc30eb2b217a96dbbe`  
		Last Modified: Wed, 01 Mar 2023 08:18:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
