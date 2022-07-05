## `mysql:debian`

```console
$ docker pull mysql@sha256:59ffc15bb9ff6c45728942f5782d63802c0b365ff0570a6461755b043c24c5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:a64df27bf8864ca04823b2a3bed3e663a323317617e6ad3cbf44656b0fe49e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157623333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0429521d998bf30471f57c7996e62ff4a5fa1a02c2a38f9719b3b3530e5886e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Tue, 05 Jul 2022 18:49:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Jul 2022 18:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:12 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 18:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 18:49:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 18:49:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 18:49:28 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 18:49:29 GMT
ENV MYSQL_VERSION=8.0.29-1debian11
# Tue, 05 Jul 2022 18:49:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 05 Jul 2022 18:49:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 05 Jul 2022 18:49:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 18:49:44 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 05 Jul 2022 18:49:44 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 18:49:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Jul 2022 18:49:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 18:49:45 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 18:49:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb421c0470dcc46febaa73c93d783d0e73d6ffc27390165ad0c6c05240d229`  
		Last Modified: Tue, 05 Jul 2022 18:50:38 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8913f7af8789b7c5e495708ebcb5bc717e72e314ff1c75e2f33f8b2291b28c4`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 4.6 MB (4644195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b5a0749b5b0e1ca4d21aa28341fe395d1b1f4bcef393a08ddffda67387ce26`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 1.4 MB (1418566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c1e6766449721ee016dc3a8915e1c0223455ca68a7d8cbc98bc3ee1c8ce6b`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d053cd43ebdcbc601b661e1310dfa0f0a3ffa3270727a54211d556578bdb7e1f`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 12.7 MB (12662096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c8f03894adcd4e3de9c8daa388adcd2d8b0f20bf560c9808b7313879153561`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6680724c36114e984b67e921ae9e4438aae29a220be32f3c09aab36e688259`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1360acd4b871d5886f29dfa0f7c17ed71269ce40ca12ebb1f629f109586a56`  
		Last Modified: Tue, 05 Jul 2022 18:50:50 GMT  
		Size: 107.5 MB (107508256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94f90c6b4a5d2709d28586f57c8e0f7348441a795adec5a0f8b7e3469968483`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b1f20b352596d8b7ee0bdc29fd584261942d04d6c9190ec1975316b567c44`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398113cf1a18167e2bd9462511531bd2c98fdafefdb3317fef5ebc18e01fdafa`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
