<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.49`](#mysql5649)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.31`](#mysql5731)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.21`](#mysql8021)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:1a83136153b238b659b0887ceb4e08275473af1eab2e67de4c22b37c5f4130cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:55638620c5a206833217dff4685e0715fb297a8458aa07c5fe5d8730cc6c872f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154474159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d589ea3123e06ae2cfb548f3a697fc82986878afb1ef7b4fe1d8a3981d420620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:19:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Aug 2020 23:19:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:26 GMT
ENV GOSU_VERSION=1.12
# Tue, 04 Aug 2020 23:19:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Aug 2020 23:19:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Aug 2020 23:19:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:45 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 04 Aug 2020 23:20:14 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 04 Aug 2020 23:20:14 GMT
ENV MYSQL_VERSION=5.7.31-1debian10
# Tue, 04 Aug 2020 23:20:15 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 04 Sep 2020 19:21:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 04 Sep 2020 19:21:07 GMT
VOLUME [/var/lib/mysql]
# Fri, 04 Sep 2020 19:21:07 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Fri, 04 Sep 2020 19:21:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 04 Sep 2020 19:21:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:21:08 GMT
EXPOSE 3306 33060
# Fri, 04 Sep 2020 19:21:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254623a9871b825936fce675bd714b26e4291b14f382b88d36ae9d85e304ed4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938e3e06dac451f904a36d49c72fb11a2366176eb3b9bd7e8a71153028a9cfd3`  
		Last Modified: Tue, 04 Aug 2020 23:21:51 GMT  
		Size: 4.2 MB (4178123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea28ebf28884e64ac7e9d560727639795015425e5ea74f69a2101f6e16a43826`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.4 MB (1419232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cef38785c27cc0ccfd16a582f888fa88b0a31e390a0b99b432478370b176e4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f9792565ae2b3bbf93a31e6370772714c1a63d40b5636bb1a8c8491e564fb`  
		Last Modified: Tue, 04 Aug 2020 23:21:53 GMT  
		Size: 13.4 MB (13446959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a57523420f36ec3d5a5fff355c7b1424481c745e2a88eb5cffd9ff340c835`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 2.4 KB (2388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f09bf1d31c1ccc04b380ab4dbe9d709958e8e6e1426ad0a37b3167c3a202f10`  
		Last Modified: Tue, 04 Aug 2020 23:22:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1591b28581e8f818847f699828a7fb9f6ee47ba5db7ca256742c502175c9c9b2`  
		Last Modified: Fri, 04 Sep 2020 19:22:27 GMT  
		Size: 108.3 MB (108327994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ef942f7603d02b8f7459de372deda1181ace772e091d30f592fa3603ee5e28`  
		Last Modified: Fri, 04 Sep 2020 19:22:10 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e009731422ea6b7ff9366fac9977a8bc1fe11765f1895122ab83b7c17e963fd`  
		Last Modified: Fri, 04 Sep 2020 19:22:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:7181be78faa3c325bf45d4387271de8d5fe4bb034c277e24545eca6d809e595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:1905a452211275c9ec3df3846b0791155f043ae6b5193c16e308cea6ae513f52
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102930093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2241380b7c9279534c375c24bf33cab66fc78b79228b78ae10fca36460f970ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:20:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Aug 2020 23:20:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:20:54 GMT
ENV GOSU_VERSION=1.12
# Tue, 04 Aug 2020 23:21:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Aug 2020 23:21:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Aug 2020 23:21:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:21:18 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 04 Aug 2020 23:21:18 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 04 Aug 2020 23:21:18 GMT
ENV MYSQL_VERSION=5.6.49-1debian9
# Tue, 04 Aug 2020 23:21:19 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 04 Sep 2020 19:21:31 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 04 Sep 2020 19:21:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 04 Sep 2020 19:21:31 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Fri, 04 Sep 2020 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 04 Sep 2020 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:21:32 GMT
EXPOSE 3306
# Fri, 04 Sep 2020 19:21:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc75a292689e27cc814ddfee710b59b82ddac5b27532ba541cec812670aa2c`  
		Last Modified: Tue, 04 Aug 2020 23:22:46 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba1844b09a58316ebab76519983bfe7b01779de739fad9cc7ba5af68330c05a`  
		Last Modified: Tue, 04 Aug 2020 23:22:46 GMT  
		Size: 4.5 MB (4502039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927406e4559511f9783afdbb512ec12329112e63cda5eafe1200fefb53ba9f4`  
		Last Modified: Tue, 04 Aug 2020 23:22:45 GMT  
		Size: 1.4 MB (1412097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f2a683960c2eb8b4c29ec450b1dcd7eb66232bd0dca67832aeb5ca217bd82c`  
		Last Modified: Tue, 04 Aug 2020 23:22:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe760d556adc88adfb6878448473d9b9889648bfb2b916093fb5d213b610fba`  
		Last Modified: Tue, 04 Aug 2020 23:22:48 GMT  
		Size: 10.2 MB (10224930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded99153be233624ef4cb4fc93c93d3bd71af690724e46ecd5efc42da1aa1f2e`  
		Last Modified: Tue, 04 Aug 2020 23:22:44 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f80b2192fcccd55ea8a1e07609884d4fe4999899f995ba8f2c30fe186cb4000`  
		Last Modified: Tue, 04 Aug 2020 23:22:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044631b720e475b05a8cd592843b2bd37495ed9d35433623b0a5695ea8e6ecdb`  
		Last Modified: Fri, 04 Sep 2020 19:22:43 GMT  
		Size: 64.2 MB (64233058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27721112bc71c9c86ace139416ebfd0e37be59fd73c332ae770bb2ce61e754f`  
		Last Modified: Fri, 04 Sep 2020 19:22:32 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69f00841d0d3d060deb14c06e12e2a49b35cffbbba69b5b1d4f01e613088a03`  
		Last Modified: Fri, 04 Sep 2020 19:22:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.49`

```console
$ docker pull mysql@sha256:7181be78faa3c325bf45d4387271de8d5fe4bb034c277e24545eca6d809e595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.49` - linux; amd64

```console
$ docker pull mysql@sha256:1905a452211275c9ec3df3846b0791155f043ae6b5193c16e308cea6ae513f52
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102930093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2241380b7c9279534c375c24bf33cab66fc78b79228b78ae10fca36460f970ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:20:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Aug 2020 23:20:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:20:54 GMT
ENV GOSU_VERSION=1.12
# Tue, 04 Aug 2020 23:21:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Aug 2020 23:21:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Aug 2020 23:21:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:21:18 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 04 Aug 2020 23:21:18 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 04 Aug 2020 23:21:18 GMT
ENV MYSQL_VERSION=5.6.49-1debian9
# Tue, 04 Aug 2020 23:21:19 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 04 Sep 2020 19:21:31 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 04 Sep 2020 19:21:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 04 Sep 2020 19:21:31 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Fri, 04 Sep 2020 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 04 Sep 2020 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:21:32 GMT
EXPOSE 3306
# Fri, 04 Sep 2020 19:21:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdc75a292689e27cc814ddfee710b59b82ddac5b27532ba541cec812670aa2c`  
		Last Modified: Tue, 04 Aug 2020 23:22:46 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba1844b09a58316ebab76519983bfe7b01779de739fad9cc7ba5af68330c05a`  
		Last Modified: Tue, 04 Aug 2020 23:22:46 GMT  
		Size: 4.5 MB (4502039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927406e4559511f9783afdbb512ec12329112e63cda5eafe1200fefb53ba9f4`  
		Last Modified: Tue, 04 Aug 2020 23:22:45 GMT  
		Size: 1.4 MB (1412097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f2a683960c2eb8b4c29ec450b1dcd7eb66232bd0dca67832aeb5ca217bd82c`  
		Last Modified: Tue, 04 Aug 2020 23:22:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe760d556adc88adfb6878448473d9b9889648bfb2b916093fb5d213b610fba`  
		Last Modified: Tue, 04 Aug 2020 23:22:48 GMT  
		Size: 10.2 MB (10224930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded99153be233624ef4cb4fc93c93d3bd71af690724e46ecd5efc42da1aa1f2e`  
		Last Modified: Tue, 04 Aug 2020 23:22:44 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f80b2192fcccd55ea8a1e07609884d4fe4999899f995ba8f2c30fe186cb4000`  
		Last Modified: Tue, 04 Aug 2020 23:22:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044631b720e475b05a8cd592843b2bd37495ed9d35433623b0a5695ea8e6ecdb`  
		Last Modified: Fri, 04 Sep 2020 19:22:43 GMT  
		Size: 64.2 MB (64233058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27721112bc71c9c86ace139416ebfd0e37be59fd73c332ae770bb2ce61e754f`  
		Last Modified: Fri, 04 Sep 2020 19:22:32 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69f00841d0d3d060deb14c06e12e2a49b35cffbbba69b5b1d4f01e613088a03`  
		Last Modified: Fri, 04 Sep 2020 19:22:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:1a83136153b238b659b0887ceb4e08275473af1eab2e67de4c22b37c5f4130cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:55638620c5a206833217dff4685e0715fb297a8458aa07c5fe5d8730cc6c872f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154474159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d589ea3123e06ae2cfb548f3a697fc82986878afb1ef7b4fe1d8a3981d420620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:19:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Aug 2020 23:19:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:26 GMT
ENV GOSU_VERSION=1.12
# Tue, 04 Aug 2020 23:19:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Aug 2020 23:19:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Aug 2020 23:19:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:45 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 04 Aug 2020 23:20:14 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 04 Aug 2020 23:20:14 GMT
ENV MYSQL_VERSION=5.7.31-1debian10
# Tue, 04 Aug 2020 23:20:15 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 04 Sep 2020 19:21:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 04 Sep 2020 19:21:07 GMT
VOLUME [/var/lib/mysql]
# Fri, 04 Sep 2020 19:21:07 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Fri, 04 Sep 2020 19:21:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 04 Sep 2020 19:21:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:21:08 GMT
EXPOSE 3306 33060
# Fri, 04 Sep 2020 19:21:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254623a9871b825936fce675bd714b26e4291b14f382b88d36ae9d85e304ed4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938e3e06dac451f904a36d49c72fb11a2366176eb3b9bd7e8a71153028a9cfd3`  
		Last Modified: Tue, 04 Aug 2020 23:21:51 GMT  
		Size: 4.2 MB (4178123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea28ebf28884e64ac7e9d560727639795015425e5ea74f69a2101f6e16a43826`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.4 MB (1419232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cef38785c27cc0ccfd16a582f888fa88b0a31e390a0b99b432478370b176e4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f9792565ae2b3bbf93a31e6370772714c1a63d40b5636bb1a8c8491e564fb`  
		Last Modified: Tue, 04 Aug 2020 23:21:53 GMT  
		Size: 13.4 MB (13446959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a57523420f36ec3d5a5fff355c7b1424481c745e2a88eb5cffd9ff340c835`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 2.4 KB (2388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f09bf1d31c1ccc04b380ab4dbe9d709958e8e6e1426ad0a37b3167c3a202f10`  
		Last Modified: Tue, 04 Aug 2020 23:22:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1591b28581e8f818847f699828a7fb9f6ee47ba5db7ca256742c502175c9c9b2`  
		Last Modified: Fri, 04 Sep 2020 19:22:27 GMT  
		Size: 108.3 MB (108327994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ef942f7603d02b8f7459de372deda1181ace772e091d30f592fa3603ee5e28`  
		Last Modified: Fri, 04 Sep 2020 19:22:10 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e009731422ea6b7ff9366fac9977a8bc1fe11765f1895122ab83b7c17e963fd`  
		Last Modified: Fri, 04 Sep 2020 19:22:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.31`

```console
$ docker pull mysql@sha256:1a83136153b238b659b0887ceb4e08275473af1eab2e67de4c22b37c5f4130cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.31` - linux; amd64

```console
$ docker pull mysql@sha256:55638620c5a206833217dff4685e0715fb297a8458aa07c5fe5d8730cc6c872f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154474159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d589ea3123e06ae2cfb548f3a697fc82986878afb1ef7b4fe1d8a3981d420620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:19:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Aug 2020 23:19:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:26 GMT
ENV GOSU_VERSION=1.12
# Tue, 04 Aug 2020 23:19:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Aug 2020 23:19:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Aug 2020 23:19:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:45 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 04 Aug 2020 23:20:14 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 04 Aug 2020 23:20:14 GMT
ENV MYSQL_VERSION=5.7.31-1debian10
# Tue, 04 Aug 2020 23:20:15 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 04 Sep 2020 19:21:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 04 Sep 2020 19:21:07 GMT
VOLUME [/var/lib/mysql]
# Fri, 04 Sep 2020 19:21:07 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Fri, 04 Sep 2020 19:21:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 04 Sep 2020 19:21:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:21:08 GMT
EXPOSE 3306 33060
# Fri, 04 Sep 2020 19:21:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254623a9871b825936fce675bd714b26e4291b14f382b88d36ae9d85e304ed4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938e3e06dac451f904a36d49c72fb11a2366176eb3b9bd7e8a71153028a9cfd3`  
		Last Modified: Tue, 04 Aug 2020 23:21:51 GMT  
		Size: 4.2 MB (4178123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea28ebf28884e64ac7e9d560727639795015425e5ea74f69a2101f6e16a43826`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.4 MB (1419232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cef38785c27cc0ccfd16a582f888fa88b0a31e390a0b99b432478370b176e4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f9792565ae2b3bbf93a31e6370772714c1a63d40b5636bb1a8c8491e564fb`  
		Last Modified: Tue, 04 Aug 2020 23:21:53 GMT  
		Size: 13.4 MB (13446959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a57523420f36ec3d5a5fff355c7b1424481c745e2a88eb5cffd9ff340c835`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 2.4 KB (2388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f09bf1d31c1ccc04b380ab4dbe9d709958e8e6e1426ad0a37b3167c3a202f10`  
		Last Modified: Tue, 04 Aug 2020 23:22:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1591b28581e8f818847f699828a7fb9f6ee47ba5db7ca256742c502175c9c9b2`  
		Last Modified: Fri, 04 Sep 2020 19:22:27 GMT  
		Size: 108.3 MB (108327994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ef942f7603d02b8f7459de372deda1181ace772e091d30f592fa3603ee5e28`  
		Last Modified: Fri, 04 Sep 2020 19:22:10 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e009731422ea6b7ff9366fac9977a8bc1fe11765f1895122ab83b7c17e963fd`  
		Last Modified: Fri, 04 Sep 2020 19:22:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:6ded54eb1e5d048d8310321ba7b92587e9eadc83b519165b70bbe47e4046e76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:2a366f244b7445b00c8374435716e370b37317addfceb3d832712f775f9482cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158633271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3646af3dc14aa17367bce05b955d29783c394d751c3d9e85eb34bd60f0d76624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:19:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Aug 2020 23:19:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:26 GMT
ENV GOSU_VERSION=1.12
# Tue, 04 Aug 2020 23:19:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Aug 2020 23:19:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Aug 2020 23:19:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:45 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 04 Aug 2020 23:19:45 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 04 Aug 2020 23:19:45 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Tue, 04 Aug 2020 23:19:46 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 04 Sep 2020 19:20:40 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 04 Sep 2020 19:20:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 04 Sep 2020 19:20:41 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 04 Sep 2020 19:20:41 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Fri, 04 Sep 2020 19:20:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 04 Sep 2020 19:20:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:20:42 GMT
EXPOSE 3306 33060
# Fri, 04 Sep 2020 19:20:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254623a9871b825936fce675bd714b26e4291b14f382b88d36ae9d85e304ed4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938e3e06dac451f904a36d49c72fb11a2366176eb3b9bd7e8a71153028a9cfd3`  
		Last Modified: Tue, 04 Aug 2020 23:21:51 GMT  
		Size: 4.2 MB (4178123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea28ebf28884e64ac7e9d560727639795015425e5ea74f69a2101f6e16a43826`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.4 MB (1419232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cef38785c27cc0ccfd16a582f888fa88b0a31e390a0b99b432478370b176e4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f9792565ae2b3bbf93a31e6370772714c1a63d40b5636bb1a8c8491e564fb`  
		Last Modified: Tue, 04 Aug 2020 23:21:53 GMT  
		Size: 13.4 MB (13446959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a57523420f36ec3d5a5fff355c7b1424481c745e2a88eb5cffd9ff340c835`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 2.4 KB (2388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c676912929ff9a4e5de0447f551251488ed2e45d3490ac396a5226c7508093b`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdd8ff735c9a5ec1230531c13d486d58341257cc55df08e3bb65bfaf0729062`  
		Last Modified: Fri, 04 Sep 2020 19:22:03 GMT  
		Size: 112.5 MB (112486260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70cbe51682d91bebdd258e27c05751b8daeee68c2538fec0f7dd9ee1a61f45`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21cf0cb4dc3804fcdb57dbf691fa77cc761972e7f06454dde97aa4938b192ad`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c36cd3abccc031046811bfca297be0bfdbcbcf05a77b623513d21b674cd493`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:6ded54eb1e5d048d8310321ba7b92587e9eadc83b519165b70bbe47e4046e76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:2a366f244b7445b00c8374435716e370b37317addfceb3d832712f775f9482cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158633271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3646af3dc14aa17367bce05b955d29783c394d751c3d9e85eb34bd60f0d76624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:19:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Aug 2020 23:19:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:26 GMT
ENV GOSU_VERSION=1.12
# Tue, 04 Aug 2020 23:19:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Aug 2020 23:19:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Aug 2020 23:19:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:45 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 04 Aug 2020 23:19:45 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 04 Aug 2020 23:19:45 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Tue, 04 Aug 2020 23:19:46 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 04 Sep 2020 19:20:40 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 04 Sep 2020 19:20:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 04 Sep 2020 19:20:41 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 04 Sep 2020 19:20:41 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Fri, 04 Sep 2020 19:20:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 04 Sep 2020 19:20:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:20:42 GMT
EXPOSE 3306 33060
# Fri, 04 Sep 2020 19:20:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254623a9871b825936fce675bd714b26e4291b14f382b88d36ae9d85e304ed4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938e3e06dac451f904a36d49c72fb11a2366176eb3b9bd7e8a71153028a9cfd3`  
		Last Modified: Tue, 04 Aug 2020 23:21:51 GMT  
		Size: 4.2 MB (4178123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea28ebf28884e64ac7e9d560727639795015425e5ea74f69a2101f6e16a43826`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.4 MB (1419232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cef38785c27cc0ccfd16a582f888fa88b0a31e390a0b99b432478370b176e4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f9792565ae2b3bbf93a31e6370772714c1a63d40b5636bb1a8c8491e564fb`  
		Last Modified: Tue, 04 Aug 2020 23:21:53 GMT  
		Size: 13.4 MB (13446959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a57523420f36ec3d5a5fff355c7b1424481c745e2a88eb5cffd9ff340c835`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 2.4 KB (2388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c676912929ff9a4e5de0447f551251488ed2e45d3490ac396a5226c7508093b`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdd8ff735c9a5ec1230531c13d486d58341257cc55df08e3bb65bfaf0729062`  
		Last Modified: Fri, 04 Sep 2020 19:22:03 GMT  
		Size: 112.5 MB (112486260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70cbe51682d91bebdd258e27c05751b8daeee68c2538fec0f7dd9ee1a61f45`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21cf0cb4dc3804fcdb57dbf691fa77cc761972e7f06454dde97aa4938b192ad`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c36cd3abccc031046811bfca297be0bfdbcbcf05a77b623513d21b674cd493`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.21`

```console
$ docker pull mysql@sha256:6ded54eb1e5d048d8310321ba7b92587e9eadc83b519165b70bbe47e4046e76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.21` - linux; amd64

```console
$ docker pull mysql@sha256:2a366f244b7445b00c8374435716e370b37317addfceb3d832712f775f9482cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158633271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3646af3dc14aa17367bce05b955d29783c394d751c3d9e85eb34bd60f0d76624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:19:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Aug 2020 23:19:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:26 GMT
ENV GOSU_VERSION=1.12
# Tue, 04 Aug 2020 23:19:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Aug 2020 23:19:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Aug 2020 23:19:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:45 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 04 Aug 2020 23:19:45 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 04 Aug 2020 23:19:45 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Tue, 04 Aug 2020 23:19:46 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 04 Sep 2020 19:20:40 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 04 Sep 2020 19:20:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 04 Sep 2020 19:20:41 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 04 Sep 2020 19:20:41 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Fri, 04 Sep 2020 19:20:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 04 Sep 2020 19:20:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:20:42 GMT
EXPOSE 3306 33060
# Fri, 04 Sep 2020 19:20:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254623a9871b825936fce675bd714b26e4291b14f382b88d36ae9d85e304ed4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938e3e06dac451f904a36d49c72fb11a2366176eb3b9bd7e8a71153028a9cfd3`  
		Last Modified: Tue, 04 Aug 2020 23:21:51 GMT  
		Size: 4.2 MB (4178123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea28ebf28884e64ac7e9d560727639795015425e5ea74f69a2101f6e16a43826`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.4 MB (1419232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cef38785c27cc0ccfd16a582f888fa88b0a31e390a0b99b432478370b176e4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f9792565ae2b3bbf93a31e6370772714c1a63d40b5636bb1a8c8491e564fb`  
		Last Modified: Tue, 04 Aug 2020 23:21:53 GMT  
		Size: 13.4 MB (13446959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a57523420f36ec3d5a5fff355c7b1424481c745e2a88eb5cffd9ff340c835`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 2.4 KB (2388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c676912929ff9a4e5de0447f551251488ed2e45d3490ac396a5226c7508093b`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdd8ff735c9a5ec1230531c13d486d58341257cc55df08e3bb65bfaf0729062`  
		Last Modified: Fri, 04 Sep 2020 19:22:03 GMT  
		Size: 112.5 MB (112486260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70cbe51682d91bebdd258e27c05751b8daeee68c2538fec0f7dd9ee1a61f45`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21cf0cb4dc3804fcdb57dbf691fa77cc761972e7f06454dde97aa4938b192ad`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c36cd3abccc031046811bfca297be0bfdbcbcf05a77b623513d21b674cd493`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:6ded54eb1e5d048d8310321ba7b92587e9eadc83b519165b70bbe47e4046e76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:2a366f244b7445b00c8374435716e370b37317addfceb3d832712f775f9482cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158633271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3646af3dc14aa17367bce05b955d29783c394d751c3d9e85eb34bd60f0d76624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:19:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Aug 2020 23:19:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:26 GMT
ENV GOSU_VERSION=1.12
# Tue, 04 Aug 2020 23:19:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Aug 2020 23:19:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Aug 2020 23:19:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:19:45 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 04 Aug 2020 23:19:45 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 04 Aug 2020 23:19:45 GMT
ENV MYSQL_VERSION=8.0.21-1debian10
# Tue, 04 Aug 2020 23:19:46 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 04 Sep 2020 19:20:40 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 04 Sep 2020 19:20:41 GMT
VOLUME [/var/lib/mysql]
# Fri, 04 Sep 2020 19:20:41 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 04 Sep 2020 19:20:41 GMT
COPY file:7cbb26bbdb8e71b36aafda38dbac08caa641714a19991b86cde77daf3286ec11 in /usr/local/bin/ 
# Fri, 04 Sep 2020 19:20:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 04 Sep 2020 19:20:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:20:42 GMT
EXPOSE 3306 33060
# Fri, 04 Sep 2020 19:20:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254623a9871b825936fce675bd714b26e4291b14f382b88d36ae9d85e304ed4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938e3e06dac451f904a36d49c72fb11a2366176eb3b9bd7e8a71153028a9cfd3`  
		Last Modified: Tue, 04 Aug 2020 23:21:51 GMT  
		Size: 4.2 MB (4178123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea28ebf28884e64ac7e9d560727639795015425e5ea74f69a2101f6e16a43826`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 1.4 MB (1419232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cef38785c27cc0ccfd16a582f888fa88b0a31e390a0b99b432478370b176e4`  
		Last Modified: Tue, 04 Aug 2020 23:21:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f9792565ae2b3bbf93a31e6370772714c1a63d40b5636bb1a8c8491e564fb`  
		Last Modified: Tue, 04 Aug 2020 23:21:53 GMT  
		Size: 13.4 MB (13446959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a57523420f36ec3d5a5fff355c7b1424481c745e2a88eb5cffd9ff340c835`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 2.4 KB (2388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c676912929ff9a4e5de0447f551251488ed2e45d3490ac396a5226c7508093b`  
		Last Modified: Tue, 04 Aug 2020 23:21:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdd8ff735c9a5ec1230531c13d486d58341257cc55df08e3bb65bfaf0729062`  
		Last Modified: Fri, 04 Sep 2020 19:22:03 GMT  
		Size: 112.5 MB (112486260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70cbe51682d91bebdd258e27c05751b8daeee68c2538fec0f7dd9ee1a61f45`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21cf0cb4dc3804fcdb57dbf691fa77cc761972e7f06454dde97aa4938b192ad`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c36cd3abccc031046811bfca297be0bfdbcbcf05a77b623513d21b674cd493`  
		Last Modified: Fri, 04 Sep 2020 19:21:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
