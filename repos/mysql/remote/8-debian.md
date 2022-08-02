## `mysql:8-debian`

```console
$ docker pull mysql@sha256:25685dab065bbd127542768e3a697eefbaebb697d29b704d902af3f9930e55cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:36ba3720adcbd75f00da7680b25266ff480c6ce18265c9fc33daf8ff3886b48f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157835919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764b78482e3abe4d1ff03a987aee2f8293bd316233b0edaa2513ef582171a9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:49:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 04:49:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:07 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 04:49:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 04:49:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 04:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:23 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 02 Aug 2022 04:49:24 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 02 Aug 2022 04:49:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 02 Aug 2022 04:49:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 04:49:39 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 02 Aug 2022 04:49:39 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 02 Aug 2022 04:49:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 04:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:49:40 GMT
EXPOSE 3306 33060
# Tue, 02 Aug 2022 04:49:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b7d57630bf155b31f64dda3d9aad39f813d2fc58a320a985daebf3b14f3049`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012051d8478ee1090757968629c2716309d45c2643a5621613c61ab3a03d76c5`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 4.4 MB (4414798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716ee4adc59fd6c63c76aee408f7e4da30281cd45d17e5a5719856fe1a23f1f`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 1.4 MB (1418429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be18bdc82a7cee346550f6df75908c04732f1cacc71c8c7f62f9e12f8cedeb`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704a769d13c18019727a01026cade3dbe37e10958126203da9485c5b5ef5395`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 12.7 MB (12661885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23293c50f7a9d512dc7ebeb4a7c6ad2d0986578db082bac560b47f82f20cff13`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3321eeac21f74670a9c57774978f68de3eddd58873a14f2d6f670c4e34de9936`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08665c1f84bc1a553e1a74920208eb162f6a5f64d5cd874481a001360597920`  
		Last Modified: Tue, 02 Aug 2022 04:51:22 GMT  
		Size: 108.0 MB (107963250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04746e5f66aad7d8339336c409d924f925fa570241ec1c3b39c33bce9df68350`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25aec94921556ff0c94b5dc9bbc84c66e1c842d69e2948bc88ea5e4e76892e6`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 5.2 KB (5154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5f8572eba5ce08d6c92d90d8786c70833d8b03af10f67de7363d307e9e0a7`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
