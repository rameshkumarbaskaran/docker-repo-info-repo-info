## `mysql:8-debian`

```console
$ docker pull mysql@sha256:fc77d54cacef90ad3d75964837fad0f2a9a368b69e7d799665a3f4e90e600c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e9fee3e714fd69cd2ccfa0c6a141fac0a60f2a02f72d43c0e7055601aaf481b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154586725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9f23df82a3e5efabd1574b862a94c0657c73a6179efec07d5cf9ae5a307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Wed, 20 Apr 2022 10:04:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Apr 2022 10:05:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Apr 2022 10:05:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Apr 2022 10:05:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Apr 2022 10:05:08 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 20 Apr 2022 10:05:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Apr 2022 10:05:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Apr 2022 10:05:08 GMT
EXPOSE 3306 33060
# Wed, 20 Apr 2022 10:05:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654aa78d12d6394284595971c9c2def73c48b58ed70ca2765fd738766f959eb7`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1a07a253d4c7cfa839c93e5be7f0ba6112ab55dc6293c0b32fa434df05803`  
		Last Modified: Wed, 20 Apr 2022 10:06:23 GMT  
		Size: 107.8 MB (107805015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32905dc9e58b246414b41a053d048bdc4e50eec1622ed5712a6a855bce811a9`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152d41026e4402a612b991b4b3f98ea0f40aa8cb85a610261ed5409174b801c2`  
		Last Modified: Wed, 20 Apr 2022 10:06:06 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e0f73ebe3204c8da1391c8439d7fb5474569556972fa43583060abec3f7a9b`  
		Last Modified: Wed, 20 Apr 2022 10:06:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
