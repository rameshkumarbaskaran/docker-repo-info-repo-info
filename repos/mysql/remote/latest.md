## `mysql:latest`

```console
$ docker pull mysql@sha256:bed914af3f2dea400c4bc83136d6b3a8cf7edcf96f5c08bbbdec8a10cc021a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:a05245c2b031387e07f86aeb6f9d7e35a771e1dfc85458c8aa3b02f67085fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968083d5be3605e3b447838e3688ba43cfc297f9a6dec9c708389cfcfc36a080`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Thu, 23 Jun 2022 04:05:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Jun 2022 04:06:08 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:09 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed38840e96e53752528926957e0067dd594eb1021be26a59e7f519bc0790a3`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a172dc2c4c7d38fada39395a5db52f0ca112b6ee2b5ab72c31c6b82e706606e`  
		Last Modified: Thu, 23 Jun 2022 04:07:23 GMT  
		Size: 109.1 MB (109103673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800b83bd0240f41f2cb8352909a3dd8ea177d095b5fdad170483865dc625b42`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e07df03fa936c6c54593ecf95be53bd632d767fad30e398c7b79b0ef2d1c1`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ad187ab64aadaf3bc6ceeb8c41dbedb2bf541f4e257c5214bdc7d1fbe098`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
