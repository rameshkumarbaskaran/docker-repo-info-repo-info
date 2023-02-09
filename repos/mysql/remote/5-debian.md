## `mysql:5-debian`

```console
$ docker pull mysql@sha256:6476de3ab220f0c20f01d7d730c019988ec68a82e993f578dafc1a3b94895fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b6dc77221a0b35c7aa40f4cc1e284c119d6ad33f12c9a0526164142217336462
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162697144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f99a3d9960fe8b2191dfa28727117aa725c2075afd787cfb02a69ec0bf88e9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:26:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 09 Feb 2023 10:26:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:26:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 10:27:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 09 Feb 2023 10:27:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 09 Feb 2023 10:27:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:27:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 09 Feb 2023 10:27:09 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 09 Feb 2023 10:27:09 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Thu, 09 Feb 2023 10:27:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 09 Feb 2023 10:27:28 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 09 Feb 2023 10:27:28 GMT
VOLUME [/var/lib/mysql]
# Thu, 09 Feb 2023 10:27:28 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 09 Feb 2023 10:27:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 10:27:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 10:27:29 GMT
EXPOSE 3306 33060
# Thu, 09 Feb 2023 10:27:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32964b27b18a9ee810264517aca8110893e509b330e12acdbabb0975acec9cf4`  
		Last Modified: Thu, 09 Feb 2023 10:28:36 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cb395a9ad2806c234c69205fb53c2285af2123149583db57d29cda565922c6`  
		Last Modified: Thu, 09 Feb 2023 10:28:35 GMT  
		Size: 4.2 MB (4182329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8a15ae9a5ff8db2b3cccd825da0959ad97e9311c7663ee2f099615dc781998`  
		Last Modified: Thu, 09 Feb 2023 10:28:34 GMT  
		Size: 1.4 MB (1441767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4750b84b045a6e1a710e75bd26ec9047126c079dcdcb1f7422f28effed77adbd`  
		Last Modified: Thu, 09 Feb 2023 10:28:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c585ef195068cd6a1da8f2c3ae3ac9610098c7a1a1979ea49cb55a77cbc57a5`  
		Last Modified: Thu, 09 Feb 2023 10:28:37 GMT  
		Size: 14.1 MB (14089423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226c572bc1e666f11e709fea2c27b2f3bb017430c15f5aef0e6d579ad70c1b54`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07d69ec5a2f74b7e950bdbb989d92ea7d3f801c4e7234305d280ee560161af5`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d3a0b1a65202d1cafb287fb738ced57cbf69568854e8a495916472c8bfb76d`  
		Last Modified: Thu, 09 Feb 2023 10:28:48 GMT  
		Size: 115.8 MB (115832901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681eb1ae9d85d3e3b4581b8eae20c8cfc147b0c018ec0836272ec80f23a4ff93`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841305cd41e20dfdf326d7fec6ab8a2b9dc69a9bca203c0230dc197905adc0e7`  
		Last Modified: Thu, 09 Feb 2023 10:28:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
