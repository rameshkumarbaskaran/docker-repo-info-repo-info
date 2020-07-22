## `mysql:latest`

```console
$ docker pull mysql@sha256:fb6a6a26111ba75f9e8487db639bc5721d4431beba4cd668a4e922b8f8b14acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:f1f10a8a6014bda907889c2f649d7b832398432b6eb4849331818f01533db293
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158635718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fcc9e1cc046c92cfcea0d66cdb00fcb7747e87dde96dfc958bd80be37af117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:14:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 22 Jul 2020 20:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 22 Jul 2020 20:14:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 22 Jul 2020 20:14:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 22 Jul 2020 20:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:14:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Jul 2020 20:14:47 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Wed, 22 Jul 2020 20:14:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 22 Jul 2020 20:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 22 Jul 2020 20:15:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jul 2020 20:15:14 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 22 Jul 2020 20:15:14 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Wed, 22 Jul 2020 20:15:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 20:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 20:15:16 GMT
EXPOSE 3306 33060
# Wed, 22 Jul 2020 20:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e5de89054c0184901d7b361aa53939eb417f6b02b94490952e7493af5b856`  
		Last Modified: Wed, 22 Jul 2020 20:17:34 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ccb86eb40398cc3c7f679c1b60a0587089c03c940e03fdeb1b8b3415f8441`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 4.2 MB (4178108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ee78841235274ca62885510d6aebeee2cb8e28df2fe98e9b08972b8c4ad005`  
		Last Modified: Wed, 22 Jul 2020 20:17:35 GMT  
		Size: 1.4 MB (1419246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd86ccee5651597918eceb86d6ddffab7218f346d3de86b7f2278cff761c04`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bea0594a440e1fdbb7284c54cbf62a79c066e430b8c52ec7d1c97c81427de8`  
		Last Modified: Wed, 22 Jul 2020 20:17:39 GMT  
		Size: 13.4 MB (13443184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f529ae895c9062642dd43724d2e001dfd8fc5401e852e407da7b314e71cf`  
		Last Modified: Wed, 22 Jul 2020 20:17:33 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0fc09f046d2387586aaef133cd264733e33597645aa48407b88f090e01e3cb`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccd5b05a8f634497cebc0350e74799d0ca0e046361bb280bcf787ac382fd01e`  
		Last Modified: Wed, 22 Jul 2020 20:18:04 GMT  
		Size: 112.5 MB (112486062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d29d8de5d4bfcd07f7157f4f3b47c3c7400e250fd09c7c43064533c0f2a88f`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8077a91f5d16cf6c6a03a1a5e7ae43d1c5b8d059374b2ca2ec2e447d08a04959`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922753e827ecc1cb20cbd2d608d772223378eac55724852d23d3d1473da185a4`  
		Last Modified: Wed, 22 Jul 2020 20:17:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
