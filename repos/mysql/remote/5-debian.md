## `mysql:5-debian`

```console
$ docker pull mysql@sha256:36002a394b549b6d293d7f76de854e69399f0c093e6b1f16baefdafe5ea21ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:ef2398ea6c295c668cf3e969c28ae7088845b07beb07b96792698c3f80c69c8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162694168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e50dddd01b351b398beff0bb34172b2edcb046f290ff29ea946b92f7c60cfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 08:17:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 01 Mar 2023 08:17:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:17:48 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Mar 2023 08:17:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 08:17:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 01 Mar 2023 08:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:18:04 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 01 Mar 2023 08:18:04 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Mar 2023 08:18:04 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Wed, 01 Mar 2023 08:18:05 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 01 Mar 2023 08:18:23 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 01 Mar 2023 08:18:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Mar 2023 08:18:24 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Mar 2023 08:18:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 08:18:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 08:18:25 GMT
EXPOSE 3306 33060
# Wed, 01 Mar 2023 08:18:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19bdbefd94aa10eb97a97f00a8597a423524a8ee1ac0481ee949550aab103d4`  
		Last Modified: Wed, 01 Mar 2023 08:19:28 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925e2a505f95d645bf606d89d712e36892cf107ac2734f53a99d73d957828dbd`  
		Last Modified: Wed, 01 Mar 2023 08:19:28 GMT  
		Size: 4.2 MB (4182352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615b524b079671c0807d23d7b6165c051d3e057cf337dc79c4692eff7f2a1754`  
		Last Modified: Wed, 01 Mar 2023 08:19:27 GMT  
		Size: 1.4 MB (1441782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23269a497e1054aa28f4f235d816862f2a9cff683f19dc248bb57d0c9bdbc544`  
		Last Modified: Wed, 01 Mar 2023 08:19:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034fd6f00cfd596d0fc2e2a26ac97b0a306501ee99bff82b16a26dcf1e06b21b`  
		Last Modified: Wed, 01 Mar 2023 08:19:29 GMT  
		Size: 14.1 MB (14087009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1c4f6ce4b763cc7098b8bb50e2063925a87b37b938873fb8721773fdc77891`  
		Last Modified: Wed, 01 Mar 2023 08:19:25 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a74551e5bdd8aa6103cb0145f16fd744127eb8e2076d188e3bdae8e304ffb0b`  
		Last Modified: Wed, 01 Mar 2023 08:19:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a3a8bb0579b93926aafefcf6a0f480e7eef4bdd55faebd8c23c3dc84748743`  
		Last Modified: Wed, 01 Mar 2023 08:19:39 GMT  
		Size: 115.8 MB (115832956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfbfd35c59124cb5b9f9562b11ab90a3f11e8634febc4bf66e0d75231f98c5b`  
		Last Modified: Wed, 01 Mar 2023 08:19:25 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9277a314e7f20aba5d30ad70cfb9c6fc26283bc49c06199e1285d04a31b4cb`  
		Last Modified: Wed, 01 Mar 2023 08:19:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
