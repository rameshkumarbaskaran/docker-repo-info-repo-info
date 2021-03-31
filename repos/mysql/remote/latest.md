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
