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
