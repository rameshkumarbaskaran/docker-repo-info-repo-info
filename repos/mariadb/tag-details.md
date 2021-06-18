<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.38`](#mariadb10238)
-	[`mariadb:10.2.38-bionic`](#mariadb10238-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.29`](#mariadb10329)
-	[`mariadb:10.3.29-focal`](#mariadb10329-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.19`](#mariadb10419)
-	[`mariadb:10.4.19-focal`](#mariadb10419-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.10`](#mariadb10510)
-	[`mariadb:10.5.10-focal`](#mariadb10510-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.1`](#mariadb1061)
-	[`mariadb:10.6.1-focal`](#mariadb1061-focal)
-	[`mariadb:beta`](#mariadbbeta)
-	[`mariadb:beta-focal`](#mariadbbeta-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:dadddd5cafc1b961e7eaf0e63b03ddea89962ae9a1ea4f7bb82d57c21b8bbbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:157b7dfff69497562abc03082d031ac2f043567d87f6ae877bb8ccc067fdb614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff629089685eb7051a239d4217f334580c09e557a9ecfeb2d562a1229d10e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:31:43 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:03 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34793730ad6f7322af1b69c65471c25adb2e7739d954894435d02a82a58d87b`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1925a0d7347a97b60fede940e8d3e2d5f761015eb37cea3dce2b8c9f0d5095`  
		Last Modified: Tue, 25 May 2021 01:35:42 GMT  
		Size: 86.9 MB (86940364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72904fb5fd0bc88de81123be54f24d16fd5024961fde989b9501a4a66ee48580`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a76a8f43b61d45782ffa134b51b80c7e10c81d34b7fbcb1d4afc13dc02be5966
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d789912dc9b6b5d3b3c3ec0af513eabb3b6fced34f588afeb58ac6c069c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:25:12 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:25:17 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:25:33 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:29:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:29:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:29:43 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:29:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:30:16 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:30:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7e38f200818e3b4dec6bc9e27f260a59371cac67cb36b9a360361bd7b0b74`  
		Last Modified: Tue, 25 May 2021 01:46:53 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3189ef563ff0a2133db70e0ecb9f0f2d7a31f76d38f7869633550a4259fbb`  
		Last Modified: Tue, 25 May 2021 01:47:13 GMT  
		Size: 91.3 MB (91324471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f2195dfcfba5e84626d5cfe648a32dfd22d44e0b33603ada234778f777f3cc`  
		Last Modified: Tue, 25 May 2021 01:46:55 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:dadddd5cafc1b961e7eaf0e63b03ddea89962ae9a1ea4f7bb82d57c21b8bbbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:157b7dfff69497562abc03082d031ac2f043567d87f6ae877bb8ccc067fdb614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff629089685eb7051a239d4217f334580c09e557a9ecfeb2d562a1229d10e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:31:43 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:03 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34793730ad6f7322af1b69c65471c25adb2e7739d954894435d02a82a58d87b`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1925a0d7347a97b60fede940e8d3e2d5f761015eb37cea3dce2b8c9f0d5095`  
		Last Modified: Tue, 25 May 2021 01:35:42 GMT  
		Size: 86.9 MB (86940364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72904fb5fd0bc88de81123be54f24d16fd5024961fde989b9501a4a66ee48580`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a76a8f43b61d45782ffa134b51b80c7e10c81d34b7fbcb1d4afc13dc02be5966
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d789912dc9b6b5d3b3c3ec0af513eabb3b6fced34f588afeb58ac6c069c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:25:12 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:25:17 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:25:33 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:29:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:29:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:29:43 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:29:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:30:16 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:30:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7e38f200818e3b4dec6bc9e27f260a59371cac67cb36b9a360361bd7b0b74`  
		Last Modified: Tue, 25 May 2021 01:46:53 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3189ef563ff0a2133db70e0ecb9f0f2d7a31f76d38f7869633550a4259fbb`  
		Last Modified: Tue, 25 May 2021 01:47:13 GMT  
		Size: 91.3 MB (91324471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f2195dfcfba5e84626d5cfe648a32dfd22d44e0b33603ada234778f777f3cc`  
		Last Modified: Tue, 25 May 2021 01:46:55 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:89450c3eb4e5ce56757d457921b072b94103696bb9f515b9546d60ea859de4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:bee50fb05a059e01e497ed216f3fd4f31a8055af3495b6853a0078f2d28a6558
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109322323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2ea028c60fba566eae08f44b4061bd4b6b180c5c47d94c7dbc85aacee6333c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:16:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 19 May 2021 21:17:02 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:17:02 GMT
ENV GOSU_VERSION=1.12
# Wed, 19 May 2021 21:17:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 19 May 2021 21:17:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:33:33 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:33:33 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:33:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:33:35 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 25 May 2021 01:33:35 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Tue, 25 May 2021 01:33:36 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:34:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:34:18 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:34:18 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:34:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:34:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:34:19 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:34:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1dfb5a3a8a14fa0b8885b004ae0f7bbb4e200f629b785498e5f5ab59c8816`  
		Last Modified: Wed, 19 May 2021 21:18:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110983ce135e409849baa8502f1bf7ab71dcc565f2d100f74dd0f2fea426931c`  
		Last Modified: Wed, 19 May 2021 21:18:52 GMT  
		Size: 4.8 MB (4813926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5eb372f8a3a8ee5d8bad73e88d3d21dfe9949cd17c9e6ea45bdeefeed9b6d7e`  
		Last Modified: Wed, 19 May 2021 21:18:52 GMT  
		Size: 3.6 MB (3586379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7c66a48e8a6b008e5f3f456a42102768740b9d2c9127e34f267d6e70cc93ca`  
		Last Modified: Wed, 19 May 2021 21:18:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870fe65935ae113fc93f839e7d295d5dcafe949f5b64eec7b769ab56f6934032`  
		Last Modified: Tue, 25 May 2021 01:37:17 GMT  
		Size: 1.6 MB (1586468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2deb6acdc9879f6b6e8e97e416ca94feebe417d8b6117c5084dd5bc44f369a5c`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18707aab25330444bd4f554311e4d9ae032fbd535dea333583f436471e9c2633`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51f9d50210aa5365d4c760c76ed203d348864300f385000c1ab0d8a28f5773`  
		Last Modified: Tue, 25 May 2021 01:37:26 GMT  
		Size: 72.6 MB (72624999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39d977c406fa05c079114f794b50d38a1c3544abbc6cda519d30a79924c917a`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a845c2885103e16b5726ce3d3ba972a89e7a6a7376f439eb16372f527d497058`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7b1a1ff4e326f56971555cfcbf4db5c1e4b23bec5507c855edbb2852d4e662e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104332994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291bcc00a47b79f17b38d111e9999ddf5ba59c0b6cf38c532f21673df3a638a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:50 GMT
ADD file:1c098d4ee63884766899c72e542e107525f0b7ade5528de87642587389864bcc in / 
# Thu, 17 Jun 2021 23:53:51 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:48:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:49:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:06 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:49:20 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:49:28 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:49:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:49:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 00:49:30 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 00:49:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:49:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:49:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:49:55 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:49:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:49:56 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:49:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:55c604a74c4b0b41ef666f811f5e160693236be8ea130c6df723480f59cbb9b8`  
		Last Modified: Thu, 17 Jun 2021 23:55:41 GMT  
		Size: 23.7 MB (23728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d37d33072a857afa7a7c06848aba6896f13885f8f60b3288503be9131f7d1`  
		Last Modified: Fri, 18 Jun 2021 00:54:00 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5240ac600f4c5cb6f6e1e67752ff54f6ea68150858733712e557f7769cf0ec94`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 4.4 MB (4395498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e9bdca319f24e8555f3cc5cb0acb5431f17160b3f7d1ace9bc0d7d2dd080c`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 3.2 MB (3247122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae8ab6f6a79453a733f4e0dd53ce34be50da7dff4919815b2649f1b095974e`  
		Last Modified: Fri, 18 Jun 2021 00:53:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ebc4960024e7df847b1995a4d1e11c2f81ae4edbead7f68449c74383fa911`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 1.5 MB (1532347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8c8f439f7efa7e04a46f45243abad39666469cb385e0299cb542a9bbdd56b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99574e259d6718e436f1f0ab6d909f8c69bcce6b13b1bde103af2271daa9007b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad85a7503ad56c12cdfcd667090e916b05f1d668c267105cb26d70634ff6f7e5`  
		Last Modified: Fri, 18 Jun 2021 00:54:07 GMT  
		Size: 71.4 MB (71416655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfea2eb314ce55b831611e3d40eb0a1362e0ef0346342a907d4f29763b214`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbce75f791185b5361c4bec16b7d33a7ec64fac370f69625c3e5322dfe53ae6`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd95f3463d3def9b9fa09be15f88a461b6fecee449bddce8f2cf45fb4f797fd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117655942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6592490997094f5b9c7736fd3562add4485104163bfdbdfcd86371133dd0cd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:49:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 20 May 2021 00:50:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:50:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 20 May 2021 00:52:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 20 May 2021 00:52:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:40:10 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:40:15 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:40:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:41:08 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 25 May 2021 01:41:15 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Tue, 25 May 2021 01:41:25 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:44:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:45:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:45:02 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:45:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:45:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:45:20 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d19b891bf132a7b6aa310f5617a87fa08e1b94367c7f6755a4ff4013768dc3`  
		Last Modified: Thu, 20 May 2021 00:58:06 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c05f12ee491186689d4774c7f9d3e472b4fb47c44c0cfd6860fd0995ca8e3c1`  
		Last Modified: Thu, 20 May 2021 00:58:04 GMT  
		Size: 5.6 MB (5630352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d772ef21443ef27cef5b031577c3f930f79d3459c7c2c56f495bf6739369c982`  
		Last Modified: Thu, 20 May 2021 00:58:04 GMT  
		Size: 3.6 MB (3584718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db00c9ac6804d1181113666f195efdd11f03120c7e4f87775e527877d64fd39`  
		Last Modified: Thu, 20 May 2021 00:58:02 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b841648f8337b04336ddfd10faade511a579672ea0adcc3ec6e8f62dc298468`  
		Last Modified: Tue, 25 May 2021 01:49:03 GMT  
		Size: 1.9 MB (1938643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1b298b55b81a1d81b5a6c82e1018fcbca6350e76f43e7f35ea443a9361485e`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d17f823c69f687d127c559f946d51328b0091a2f18cd20b69684ff8f18a8a1`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3b7e2b349b4735c00e176e2d28746422aba34d6c87cd6741d45f1edc9d574`  
		Last Modified: Tue, 25 May 2021 01:49:16 GMT  
		Size: 76.1 MB (76080814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0b8d305e30385b5647214533b0747f0ba72fb58929f03e5aba5e4aef15fb4f`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f1b71ef6c7fd1dc09068bddde0e22382ffec0ff76488103697927760912c6b`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:89450c3eb4e5ce56757d457921b072b94103696bb9f515b9546d60ea859de4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:bee50fb05a059e01e497ed216f3fd4f31a8055af3495b6853a0078f2d28a6558
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109322323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2ea028c60fba566eae08f44b4061bd4b6b180c5c47d94c7dbc85aacee6333c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:16:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 19 May 2021 21:17:02 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:17:02 GMT
ENV GOSU_VERSION=1.12
# Wed, 19 May 2021 21:17:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 19 May 2021 21:17:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:33:33 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:33:33 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:33:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:33:35 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 25 May 2021 01:33:35 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Tue, 25 May 2021 01:33:36 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:34:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:34:18 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:34:18 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:34:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:34:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:34:19 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:34:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1dfb5a3a8a14fa0b8885b004ae0f7bbb4e200f629b785498e5f5ab59c8816`  
		Last Modified: Wed, 19 May 2021 21:18:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110983ce135e409849baa8502f1bf7ab71dcc565f2d100f74dd0f2fea426931c`  
		Last Modified: Wed, 19 May 2021 21:18:52 GMT  
		Size: 4.8 MB (4813926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5eb372f8a3a8ee5d8bad73e88d3d21dfe9949cd17c9e6ea45bdeefeed9b6d7e`  
		Last Modified: Wed, 19 May 2021 21:18:52 GMT  
		Size: 3.6 MB (3586379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7c66a48e8a6b008e5f3f456a42102768740b9d2c9127e34f267d6e70cc93ca`  
		Last Modified: Wed, 19 May 2021 21:18:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870fe65935ae113fc93f839e7d295d5dcafe949f5b64eec7b769ab56f6934032`  
		Last Modified: Tue, 25 May 2021 01:37:17 GMT  
		Size: 1.6 MB (1586468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2deb6acdc9879f6b6e8e97e416ca94feebe417d8b6117c5084dd5bc44f369a5c`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18707aab25330444bd4f554311e4d9ae032fbd535dea333583f436471e9c2633`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51f9d50210aa5365d4c760c76ed203d348864300f385000c1ab0d8a28f5773`  
		Last Modified: Tue, 25 May 2021 01:37:26 GMT  
		Size: 72.6 MB (72624999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39d977c406fa05c079114f794b50d38a1c3544abbc6cda519d30a79924c917a`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a845c2885103e16b5726ce3d3ba972a89e7a6a7376f439eb16372f527d497058`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7b1a1ff4e326f56971555cfcbf4db5c1e4b23bec5507c855edbb2852d4e662e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104332994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291bcc00a47b79f17b38d111e9999ddf5ba59c0b6cf38c532f21673df3a638a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:50 GMT
ADD file:1c098d4ee63884766899c72e542e107525f0b7ade5528de87642587389864bcc in / 
# Thu, 17 Jun 2021 23:53:51 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:48:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:49:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:06 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:49:20 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:49:28 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:49:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:49:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 00:49:30 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 00:49:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:49:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:49:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:49:55 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:49:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:49:56 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:49:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:55c604a74c4b0b41ef666f811f5e160693236be8ea130c6df723480f59cbb9b8`  
		Last Modified: Thu, 17 Jun 2021 23:55:41 GMT  
		Size: 23.7 MB (23728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d37d33072a857afa7a7c06848aba6896f13885f8f60b3288503be9131f7d1`  
		Last Modified: Fri, 18 Jun 2021 00:54:00 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5240ac600f4c5cb6f6e1e67752ff54f6ea68150858733712e557f7769cf0ec94`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 4.4 MB (4395498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e9bdca319f24e8555f3cc5cb0acb5431f17160b3f7d1ace9bc0d7d2dd080c`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 3.2 MB (3247122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae8ab6f6a79453a733f4e0dd53ce34be50da7dff4919815b2649f1b095974e`  
		Last Modified: Fri, 18 Jun 2021 00:53:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ebc4960024e7df847b1995a4d1e11c2f81ae4edbead7f68449c74383fa911`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 1.5 MB (1532347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8c8f439f7efa7e04a46f45243abad39666469cb385e0299cb542a9bbdd56b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99574e259d6718e436f1f0ab6d909f8c69bcce6b13b1bde103af2271daa9007b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad85a7503ad56c12cdfcd667090e916b05f1d668c267105cb26d70634ff6f7e5`  
		Last Modified: Fri, 18 Jun 2021 00:54:07 GMT  
		Size: 71.4 MB (71416655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfea2eb314ce55b831611e3d40eb0a1362e0ef0346342a907d4f29763b214`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbce75f791185b5361c4bec16b7d33a7ec64fac370f69625c3e5322dfe53ae6`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd95f3463d3def9b9fa09be15f88a461b6fecee449bddce8f2cf45fb4f797fd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117655942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6592490997094f5b9c7736fd3562add4485104163bfdbdfcd86371133dd0cd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:49:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 20 May 2021 00:50:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:50:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 20 May 2021 00:52:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 20 May 2021 00:52:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:40:10 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:40:15 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:40:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:41:08 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 25 May 2021 01:41:15 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Tue, 25 May 2021 01:41:25 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:44:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:45:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:45:02 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:45:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:45:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:45:20 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d19b891bf132a7b6aa310f5617a87fa08e1b94367c7f6755a4ff4013768dc3`  
		Last Modified: Thu, 20 May 2021 00:58:06 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c05f12ee491186689d4774c7f9d3e472b4fb47c44c0cfd6860fd0995ca8e3c1`  
		Last Modified: Thu, 20 May 2021 00:58:04 GMT  
		Size: 5.6 MB (5630352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d772ef21443ef27cef5b031577c3f930f79d3459c7c2c56f495bf6739369c982`  
		Last Modified: Thu, 20 May 2021 00:58:04 GMT  
		Size: 3.6 MB (3584718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db00c9ac6804d1181113666f195efdd11f03120c7e4f87775e527877d64fd39`  
		Last Modified: Thu, 20 May 2021 00:58:02 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b841648f8337b04336ddfd10faade511a579672ea0adcc3ec6e8f62dc298468`  
		Last Modified: Tue, 25 May 2021 01:49:03 GMT  
		Size: 1.9 MB (1938643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1b298b55b81a1d81b5a6c82e1018fcbca6350e76f43e7f35ea443a9361485e`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d17f823c69f687d127c559f946d51328b0091a2f18cd20b69684ff8f18a8a1`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3b7e2b349b4735c00e176e2d28746422aba34d6c87cd6741d45f1edc9d574`  
		Last Modified: Tue, 25 May 2021 01:49:16 GMT  
		Size: 76.1 MB (76080814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0b8d305e30385b5647214533b0747f0ba72fb58929f03e5aba5e4aef15fb4f`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f1b71ef6c7fd1dc09068bddde0e22382ffec0ff76488103697927760912c6b`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.38`

```console
$ docker pull mariadb@sha256:89450c3eb4e5ce56757d457921b072b94103696bb9f515b9546d60ea859de4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.38` - linux; amd64

```console
$ docker pull mariadb@sha256:bee50fb05a059e01e497ed216f3fd4f31a8055af3495b6853a0078f2d28a6558
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109322323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2ea028c60fba566eae08f44b4061bd4b6b180c5c47d94c7dbc85aacee6333c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:16:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 19 May 2021 21:17:02 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:17:02 GMT
ENV GOSU_VERSION=1.12
# Wed, 19 May 2021 21:17:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 19 May 2021 21:17:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:33:33 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:33:33 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:33:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:33:35 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 25 May 2021 01:33:35 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Tue, 25 May 2021 01:33:36 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:34:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:34:18 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:34:18 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:34:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:34:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:34:19 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:34:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1dfb5a3a8a14fa0b8885b004ae0f7bbb4e200f629b785498e5f5ab59c8816`  
		Last Modified: Wed, 19 May 2021 21:18:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110983ce135e409849baa8502f1bf7ab71dcc565f2d100f74dd0f2fea426931c`  
		Last Modified: Wed, 19 May 2021 21:18:52 GMT  
		Size: 4.8 MB (4813926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5eb372f8a3a8ee5d8bad73e88d3d21dfe9949cd17c9e6ea45bdeefeed9b6d7e`  
		Last Modified: Wed, 19 May 2021 21:18:52 GMT  
		Size: 3.6 MB (3586379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7c66a48e8a6b008e5f3f456a42102768740b9d2c9127e34f267d6e70cc93ca`  
		Last Modified: Wed, 19 May 2021 21:18:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870fe65935ae113fc93f839e7d295d5dcafe949f5b64eec7b769ab56f6934032`  
		Last Modified: Tue, 25 May 2021 01:37:17 GMT  
		Size: 1.6 MB (1586468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2deb6acdc9879f6b6e8e97e416ca94feebe417d8b6117c5084dd5bc44f369a5c`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18707aab25330444bd4f554311e4d9ae032fbd535dea333583f436471e9c2633`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51f9d50210aa5365d4c760c76ed203d348864300f385000c1ab0d8a28f5773`  
		Last Modified: Tue, 25 May 2021 01:37:26 GMT  
		Size: 72.6 MB (72624999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39d977c406fa05c079114f794b50d38a1c3544abbc6cda519d30a79924c917a`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a845c2885103e16b5726ce3d3ba972a89e7a6a7376f439eb16372f527d497058`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.38` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7b1a1ff4e326f56971555cfcbf4db5c1e4b23bec5507c855edbb2852d4e662e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104332994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291bcc00a47b79f17b38d111e9999ddf5ba59c0b6cf38c532f21673df3a638a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:50 GMT
ADD file:1c098d4ee63884766899c72e542e107525f0b7ade5528de87642587389864bcc in / 
# Thu, 17 Jun 2021 23:53:51 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:48:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:49:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:06 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:49:20 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:49:28 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:49:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:49:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 00:49:30 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 00:49:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:49:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:49:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:49:55 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:49:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:49:56 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:49:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:55c604a74c4b0b41ef666f811f5e160693236be8ea130c6df723480f59cbb9b8`  
		Last Modified: Thu, 17 Jun 2021 23:55:41 GMT  
		Size: 23.7 MB (23728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d37d33072a857afa7a7c06848aba6896f13885f8f60b3288503be9131f7d1`  
		Last Modified: Fri, 18 Jun 2021 00:54:00 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5240ac600f4c5cb6f6e1e67752ff54f6ea68150858733712e557f7769cf0ec94`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 4.4 MB (4395498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e9bdca319f24e8555f3cc5cb0acb5431f17160b3f7d1ace9bc0d7d2dd080c`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 3.2 MB (3247122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae8ab6f6a79453a733f4e0dd53ce34be50da7dff4919815b2649f1b095974e`  
		Last Modified: Fri, 18 Jun 2021 00:53:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ebc4960024e7df847b1995a4d1e11c2f81ae4edbead7f68449c74383fa911`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 1.5 MB (1532347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8c8f439f7efa7e04a46f45243abad39666469cb385e0299cb542a9bbdd56b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99574e259d6718e436f1f0ab6d909f8c69bcce6b13b1bde103af2271daa9007b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad85a7503ad56c12cdfcd667090e916b05f1d668c267105cb26d70634ff6f7e5`  
		Last Modified: Fri, 18 Jun 2021 00:54:07 GMT  
		Size: 71.4 MB (71416655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfea2eb314ce55b831611e3d40eb0a1362e0ef0346342a907d4f29763b214`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbce75f791185b5361c4bec16b7d33a7ec64fac370f69625c3e5322dfe53ae6`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.38` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd95f3463d3def9b9fa09be15f88a461b6fecee449bddce8f2cf45fb4f797fd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117655942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6592490997094f5b9c7736fd3562add4485104163bfdbdfcd86371133dd0cd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:49:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 20 May 2021 00:50:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:50:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 20 May 2021 00:52:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 20 May 2021 00:52:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:40:10 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:40:15 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:40:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:41:08 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 25 May 2021 01:41:15 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Tue, 25 May 2021 01:41:25 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:44:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:45:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:45:02 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:45:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:45:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:45:20 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d19b891bf132a7b6aa310f5617a87fa08e1b94367c7f6755a4ff4013768dc3`  
		Last Modified: Thu, 20 May 2021 00:58:06 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c05f12ee491186689d4774c7f9d3e472b4fb47c44c0cfd6860fd0995ca8e3c1`  
		Last Modified: Thu, 20 May 2021 00:58:04 GMT  
		Size: 5.6 MB (5630352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d772ef21443ef27cef5b031577c3f930f79d3459c7c2c56f495bf6739369c982`  
		Last Modified: Thu, 20 May 2021 00:58:04 GMT  
		Size: 3.6 MB (3584718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db00c9ac6804d1181113666f195efdd11f03120c7e4f87775e527877d64fd39`  
		Last Modified: Thu, 20 May 2021 00:58:02 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b841648f8337b04336ddfd10faade511a579672ea0adcc3ec6e8f62dc298468`  
		Last Modified: Tue, 25 May 2021 01:49:03 GMT  
		Size: 1.9 MB (1938643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1b298b55b81a1d81b5a6c82e1018fcbca6350e76f43e7f35ea443a9361485e`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d17f823c69f687d127c559f946d51328b0091a2f18cd20b69684ff8f18a8a1`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3b7e2b349b4735c00e176e2d28746422aba34d6c87cd6741d45f1edc9d574`  
		Last Modified: Tue, 25 May 2021 01:49:16 GMT  
		Size: 76.1 MB (76080814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0b8d305e30385b5647214533b0747f0ba72fb58929f03e5aba5e4aef15fb4f`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f1b71ef6c7fd1dc09068bddde0e22382ffec0ff76488103697927760912c6b`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.38-bionic`

```console
$ docker pull mariadb@sha256:89450c3eb4e5ce56757d457921b072b94103696bb9f515b9546d60ea859de4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.38-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:bee50fb05a059e01e497ed216f3fd4f31a8055af3495b6853a0078f2d28a6558
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109322323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2ea028c60fba566eae08f44b4061bd4b6b180c5c47d94c7dbc85aacee6333c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:16:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 19 May 2021 21:17:02 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:17:02 GMT
ENV GOSU_VERSION=1.12
# Wed, 19 May 2021 21:17:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 19 May 2021 21:17:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:33:33 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:33:33 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:33:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:33:35 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 25 May 2021 01:33:35 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Tue, 25 May 2021 01:33:36 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:34:17 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:34:18 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:34:18 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:34:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:34:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:34:19 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:34:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1dfb5a3a8a14fa0b8885b004ae0f7bbb4e200f629b785498e5f5ab59c8816`  
		Last Modified: Wed, 19 May 2021 21:18:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110983ce135e409849baa8502f1bf7ab71dcc565f2d100f74dd0f2fea426931c`  
		Last Modified: Wed, 19 May 2021 21:18:52 GMT  
		Size: 4.8 MB (4813926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5eb372f8a3a8ee5d8bad73e88d3d21dfe9949cd17c9e6ea45bdeefeed9b6d7e`  
		Last Modified: Wed, 19 May 2021 21:18:52 GMT  
		Size: 3.6 MB (3586379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7c66a48e8a6b008e5f3f456a42102768740b9d2c9127e34f267d6e70cc93ca`  
		Last Modified: Wed, 19 May 2021 21:18:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870fe65935ae113fc93f839e7d295d5dcafe949f5b64eec7b769ab56f6934032`  
		Last Modified: Tue, 25 May 2021 01:37:17 GMT  
		Size: 1.6 MB (1586468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2deb6acdc9879f6b6e8e97e416ca94feebe417d8b6117c5084dd5bc44f369a5c`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18707aab25330444bd4f554311e4d9ae032fbd535dea333583f436471e9c2633`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51f9d50210aa5365d4c760c76ed203d348864300f385000c1ab0d8a28f5773`  
		Last Modified: Tue, 25 May 2021 01:37:26 GMT  
		Size: 72.6 MB (72624999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39d977c406fa05c079114f794b50d38a1c3544abbc6cda519d30a79924c917a`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a845c2885103e16b5726ce3d3ba972a89e7a6a7376f439eb16372f527d497058`  
		Last Modified: Tue, 25 May 2021 01:37:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.38-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7b1a1ff4e326f56971555cfcbf4db5c1e4b23bec5507c855edbb2852d4e662e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104332994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291bcc00a47b79f17b38d111e9999ddf5ba59c0b6cf38c532f21673df3a638a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:50 GMT
ADD file:1c098d4ee63884766899c72e542e107525f0b7ade5528de87642587389864bcc in / 
# Thu, 17 Jun 2021 23:53:51 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:48:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:49:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:06 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:49:20 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:49:28 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:49:28 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:49:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:49:29 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 18 Jun 2021 00:49:30 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Fri, 18 Jun 2021 00:49:30 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:49:54 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:49:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:49:55 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:49:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:49:56 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:49:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:55c604a74c4b0b41ef666f811f5e160693236be8ea130c6df723480f59cbb9b8`  
		Last Modified: Thu, 17 Jun 2021 23:55:41 GMT  
		Size: 23.7 MB (23728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d37d33072a857afa7a7c06848aba6896f13885f8f60b3288503be9131f7d1`  
		Last Modified: Fri, 18 Jun 2021 00:54:00 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5240ac600f4c5cb6f6e1e67752ff54f6ea68150858733712e557f7769cf0ec94`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 4.4 MB (4395498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e9bdca319f24e8555f3cc5cb0acb5431f17160b3f7d1ace9bc0d7d2dd080c`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 3.2 MB (3247122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae8ab6f6a79453a733f4e0dd53ce34be50da7dff4919815b2649f1b095974e`  
		Last Modified: Fri, 18 Jun 2021 00:53:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ebc4960024e7df847b1995a4d1e11c2f81ae4edbead7f68449c74383fa911`  
		Last Modified: Fri, 18 Jun 2021 00:53:58 GMT  
		Size: 1.5 MB (1532347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8c8f439f7efa7e04a46f45243abad39666469cb385e0299cb542a9bbdd56b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99574e259d6718e436f1f0ab6d909f8c69bcce6b13b1bde103af2271daa9007b`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad85a7503ad56c12cdfcd667090e916b05f1d668c267105cb26d70634ff6f7e5`  
		Last Modified: Fri, 18 Jun 2021 00:54:07 GMT  
		Size: 71.4 MB (71416655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfea2eb314ce55b831611e3d40eb0a1362e0ef0346342a907d4f29763b214`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbce75f791185b5361c4bec16b7d33a7ec64fac370f69625c3e5322dfe53ae6`  
		Last Modified: Fri, 18 Jun 2021 00:53:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.38-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd95f3463d3def9b9fa09be15f88a461b6fecee449bddce8f2cf45fb4f797fd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117655942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6592490997094f5b9c7736fd3562add4485104163bfdbdfcd86371133dd0cd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:49:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 20 May 2021 00:50:41 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:50:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 20 May 2021 00:52:11 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 20 May 2021 00:52:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:40:10 GMT
RUN set -ex; 	apt-get update; 	if [ bionic = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:40:15 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:40:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:41:08 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 25 May 2021 01:41:15 GMT
ENV MARIADB_VERSION=1:10.2.38+maria~bionic
# Tue, 25 May 2021 01:41:25 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu bionic main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:44:51 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:45:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:45:02 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:45:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:45:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:45:20 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d19b891bf132a7b6aa310f5617a87fa08e1b94367c7f6755a4ff4013768dc3`  
		Last Modified: Thu, 20 May 2021 00:58:06 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c05f12ee491186689d4774c7f9d3e472b4fb47c44c0cfd6860fd0995ca8e3c1`  
		Last Modified: Thu, 20 May 2021 00:58:04 GMT  
		Size: 5.6 MB (5630352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d772ef21443ef27cef5b031577c3f930f79d3459c7c2c56f495bf6739369c982`  
		Last Modified: Thu, 20 May 2021 00:58:04 GMT  
		Size: 3.6 MB (3584718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db00c9ac6804d1181113666f195efdd11f03120c7e4f87775e527877d64fd39`  
		Last Modified: Thu, 20 May 2021 00:58:02 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b841648f8337b04336ddfd10faade511a579672ea0adcc3ec6e8f62dc298468`  
		Last Modified: Tue, 25 May 2021 01:49:03 GMT  
		Size: 1.9 MB (1938643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1b298b55b81a1d81b5a6c82e1018fcbca6350e76f43e7f35ea443a9361485e`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d17f823c69f687d127c559f946d51328b0091a2f18cd20b69684ff8f18a8a1`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3b7e2b349b4735c00e176e2d28746422aba34d6c87cd6741d45f1edc9d574`  
		Last Modified: Tue, 25 May 2021 01:49:16 GMT  
		Size: 76.1 MB (76080814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0b8d305e30385b5647214533b0747f0ba72fb58929f03e5aba5e4aef15fb4f`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f1b71ef6c7fd1dc09068bddde0e22382ffec0ff76488103697927760912c6b`  
		Last Modified: Tue, 25 May 2021 01:49:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:f22b35ecb385fbdc24d0c16be3b43590371001e719d93577e59f977a8359bf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:9994a483f0f967258775179dd836f867df403c86efd1d06bac85130f811b63b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120014228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3f053c5c9dd33e5cfa0a50aae9c8646711dd61bcd42d8b16a29bacd215f6e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:32:38 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 May 2021 01:32:38 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Tue, 25 May 2021 01:32:39 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:33:00 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:33:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:33:01 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:33:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:33:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:33:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e723e7328aec7affcad64c32dbd45bd7489d7aa742f52898168a2203c724773`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f340a8a42326dc82e656af12ed02de8193b5568eb53976fac190be6c6a4af2fe`  
		Last Modified: Tue, 25 May 2021 01:36:56 GMT  
		Size: 80.1 MB (80081134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90981dc33f98d1defaec2ae7b99701c59ec94da5cc78d5a0a1df4b18073f8289`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548c402ac4db6b034cd30b399daaa6273d21084fa7a17f9cec96127f7ff65414`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:05ff2732c1990967a3395d6930deb04235372e724c7da356267c3118603ed9b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117617654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276bab2fb248e858dae13121ec7aa60d159c923acd2a52744ba4f039b589e808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 00:48:23 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:47 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760c30d6dbfa45dc14eb4a99ce6717ff04fce410c9df6b19e2316c24e3c0277`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf847301ed0bae6f944b6b36e057cb9bd51224a86f5a2b76935bbb73e5078cbe`  
		Last Modified: Fri, 18 Jun 2021 00:53:35 GMT  
		Size: 79.4 MB (79380839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015aaec3f93fb58e45b19e5781020acfa46c5f58f9225473dfdbdde9ebf9ff61`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163dd26927d877159c8477b3ea75082a5271c65a1c50861d1463690100d7541e`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ee8fe886927447891069eb04a0702bcd9409b75415490da3281dba5262d5f9a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130880832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fee4e104c2b5ba1f97a2a2cfc618f80eed9a32b98077e2fed8b3b47916f4dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:35:36 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 May 2021 01:35:40 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Tue, 25 May 2021 01:35:54 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:38:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:38:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:38:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:39:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:39:13 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:39:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e84ce88592de31fef534576d86e8bb8a11abcf1e12c8bb30cfabf62d40a7cd`  
		Last Modified: Tue, 25 May 2021 01:48:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf7bac3e4431aba6c0cffae3cd5fa1b6e5596309fa36b50f86ff6e9492df702`  
		Last Modified: Tue, 25 May 2021 01:48:38 GMT  
		Size: 84.7 MB (84650446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58880c7d225873a6dc3cc7fa7b11d91b5e99bba45780053d6c5acb50d513159b`  
		Last Modified: Tue, 25 May 2021 01:48:18 GMT  
		Size: 5.6 KB (5553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ecc2ed32d3b4e50cbef7de135dfdf0f49653776fbca655065fdcbbb98e330`  
		Last Modified: Tue, 25 May 2021 01:48:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:f22b35ecb385fbdc24d0c16be3b43590371001e719d93577e59f977a8359bf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:9994a483f0f967258775179dd836f867df403c86efd1d06bac85130f811b63b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120014228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3f053c5c9dd33e5cfa0a50aae9c8646711dd61bcd42d8b16a29bacd215f6e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:32:38 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 May 2021 01:32:38 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Tue, 25 May 2021 01:32:39 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:33:00 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:33:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:33:01 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:33:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:33:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:33:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e723e7328aec7affcad64c32dbd45bd7489d7aa742f52898168a2203c724773`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f340a8a42326dc82e656af12ed02de8193b5568eb53976fac190be6c6a4af2fe`  
		Last Modified: Tue, 25 May 2021 01:36:56 GMT  
		Size: 80.1 MB (80081134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90981dc33f98d1defaec2ae7b99701c59ec94da5cc78d5a0a1df4b18073f8289`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548c402ac4db6b034cd30b399daaa6273d21084fa7a17f9cec96127f7ff65414`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:05ff2732c1990967a3395d6930deb04235372e724c7da356267c3118603ed9b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117617654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276bab2fb248e858dae13121ec7aa60d159c923acd2a52744ba4f039b589e808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 00:48:23 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:47 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760c30d6dbfa45dc14eb4a99ce6717ff04fce410c9df6b19e2316c24e3c0277`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf847301ed0bae6f944b6b36e057cb9bd51224a86f5a2b76935bbb73e5078cbe`  
		Last Modified: Fri, 18 Jun 2021 00:53:35 GMT  
		Size: 79.4 MB (79380839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015aaec3f93fb58e45b19e5781020acfa46c5f58f9225473dfdbdde9ebf9ff61`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163dd26927d877159c8477b3ea75082a5271c65a1c50861d1463690100d7541e`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ee8fe886927447891069eb04a0702bcd9409b75415490da3281dba5262d5f9a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130880832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fee4e104c2b5ba1f97a2a2cfc618f80eed9a32b98077e2fed8b3b47916f4dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:35:36 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 May 2021 01:35:40 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Tue, 25 May 2021 01:35:54 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:38:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:38:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:38:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:39:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:39:13 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:39:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e84ce88592de31fef534576d86e8bb8a11abcf1e12c8bb30cfabf62d40a7cd`  
		Last Modified: Tue, 25 May 2021 01:48:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf7bac3e4431aba6c0cffae3cd5fa1b6e5596309fa36b50f86ff6e9492df702`  
		Last Modified: Tue, 25 May 2021 01:48:38 GMT  
		Size: 84.7 MB (84650446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58880c7d225873a6dc3cc7fa7b11d91b5e99bba45780053d6c5acb50d513159b`  
		Last Modified: Tue, 25 May 2021 01:48:18 GMT  
		Size: 5.6 KB (5553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ecc2ed32d3b4e50cbef7de135dfdf0f49653776fbca655065fdcbbb98e330`  
		Last Modified: Tue, 25 May 2021 01:48:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.29`

```console
$ docker pull mariadb@sha256:f22b35ecb385fbdc24d0c16be3b43590371001e719d93577e59f977a8359bf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.29` - linux; amd64

```console
$ docker pull mariadb@sha256:9994a483f0f967258775179dd836f867df403c86efd1d06bac85130f811b63b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120014228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3f053c5c9dd33e5cfa0a50aae9c8646711dd61bcd42d8b16a29bacd215f6e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:32:38 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 May 2021 01:32:38 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Tue, 25 May 2021 01:32:39 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:33:00 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:33:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:33:01 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:33:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:33:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:33:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e723e7328aec7affcad64c32dbd45bd7489d7aa742f52898168a2203c724773`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f340a8a42326dc82e656af12ed02de8193b5568eb53976fac190be6c6a4af2fe`  
		Last Modified: Tue, 25 May 2021 01:36:56 GMT  
		Size: 80.1 MB (80081134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90981dc33f98d1defaec2ae7b99701c59ec94da5cc78d5a0a1df4b18073f8289`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548c402ac4db6b034cd30b399daaa6273d21084fa7a17f9cec96127f7ff65414`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.29` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:05ff2732c1990967a3395d6930deb04235372e724c7da356267c3118603ed9b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117617654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276bab2fb248e858dae13121ec7aa60d159c923acd2a52744ba4f039b589e808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 00:48:23 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:47 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760c30d6dbfa45dc14eb4a99ce6717ff04fce410c9df6b19e2316c24e3c0277`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf847301ed0bae6f944b6b36e057cb9bd51224a86f5a2b76935bbb73e5078cbe`  
		Last Modified: Fri, 18 Jun 2021 00:53:35 GMT  
		Size: 79.4 MB (79380839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015aaec3f93fb58e45b19e5781020acfa46c5f58f9225473dfdbdde9ebf9ff61`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163dd26927d877159c8477b3ea75082a5271c65a1c50861d1463690100d7541e`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.29` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ee8fe886927447891069eb04a0702bcd9409b75415490da3281dba5262d5f9a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130880832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fee4e104c2b5ba1f97a2a2cfc618f80eed9a32b98077e2fed8b3b47916f4dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:35:36 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 May 2021 01:35:40 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Tue, 25 May 2021 01:35:54 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:38:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:38:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:38:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:39:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:39:13 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:39:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e84ce88592de31fef534576d86e8bb8a11abcf1e12c8bb30cfabf62d40a7cd`  
		Last Modified: Tue, 25 May 2021 01:48:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf7bac3e4431aba6c0cffae3cd5fa1b6e5596309fa36b50f86ff6e9492df702`  
		Last Modified: Tue, 25 May 2021 01:48:38 GMT  
		Size: 84.7 MB (84650446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58880c7d225873a6dc3cc7fa7b11d91b5e99bba45780053d6c5acb50d513159b`  
		Last Modified: Tue, 25 May 2021 01:48:18 GMT  
		Size: 5.6 KB (5553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ecc2ed32d3b4e50cbef7de135dfdf0f49653776fbca655065fdcbbb98e330`  
		Last Modified: Tue, 25 May 2021 01:48:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.29-focal`

```console
$ docker pull mariadb@sha256:f22b35ecb385fbdc24d0c16be3b43590371001e719d93577e59f977a8359bf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.29-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:9994a483f0f967258775179dd836f867df403c86efd1d06bac85130f811b63b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120014228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3f053c5c9dd33e5cfa0a50aae9c8646711dd61bcd42d8b16a29bacd215f6e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:32:38 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 May 2021 01:32:38 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Tue, 25 May 2021 01:32:39 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:33:00 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:33:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:33:01 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:33:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:33:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:33:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e723e7328aec7affcad64c32dbd45bd7489d7aa742f52898168a2203c724773`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f340a8a42326dc82e656af12ed02de8193b5568eb53976fac190be6c6a4af2fe`  
		Last Modified: Tue, 25 May 2021 01:36:56 GMT  
		Size: 80.1 MB (80081134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90981dc33f98d1defaec2ae7b99701c59ec94da5cc78d5a0a1df4b18073f8289`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548c402ac4db6b034cd30b399daaa6273d21084fa7a17f9cec96127f7ff65414`  
		Last Modified: Tue, 25 May 2021 01:36:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.29-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:05ff2732c1990967a3395d6930deb04235372e724c7da356267c3118603ed9b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117617654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276bab2fb248e858dae13121ec7aa60d159c923acd2a52744ba4f039b589e808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 18 Jun 2021 00:48:22 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Fri, 18 Jun 2021 00:48:23 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:46 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:47 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:49 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760c30d6dbfa45dc14eb4a99ce6717ff04fce410c9df6b19e2316c24e3c0277`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf847301ed0bae6f944b6b36e057cb9bd51224a86f5a2b76935bbb73e5078cbe`  
		Last Modified: Fri, 18 Jun 2021 00:53:35 GMT  
		Size: 79.4 MB (79380839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015aaec3f93fb58e45b19e5781020acfa46c5f58f9225473dfdbdde9ebf9ff61`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163dd26927d877159c8477b3ea75082a5271c65a1c50861d1463690100d7541e`  
		Last Modified: Fri, 18 Jun 2021 00:53:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.29-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ee8fe886927447891069eb04a0702bcd9409b75415490da3281dba5262d5f9a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130880832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fee4e104c2b5ba1f97a2a2cfc618f80eed9a32b98077e2fed8b3b47916f4dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:35:36 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 May 2021 01:35:40 GMT
ENV MARIADB_VERSION=1:10.3.29+maria~focal
# Tue, 25 May 2021 01:35:54 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:38:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:38:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:38:45 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:39:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:39:13 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:39:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e84ce88592de31fef534576d86e8bb8a11abcf1e12c8bb30cfabf62d40a7cd`  
		Last Modified: Tue, 25 May 2021 01:48:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf7bac3e4431aba6c0cffae3cd5fa1b6e5596309fa36b50f86ff6e9492df702`  
		Last Modified: Tue, 25 May 2021 01:48:38 GMT  
		Size: 84.7 MB (84650446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58880c7d225873a6dc3cc7fa7b11d91b5e99bba45780053d6c5acb50d513159b`  
		Last Modified: Tue, 25 May 2021 01:48:18 GMT  
		Size: 5.6 KB (5553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ecc2ed32d3b4e50cbef7de135dfdf0f49653776fbca655065fdcbbb98e330`  
		Last Modified: Tue, 25 May 2021 01:48:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:928473e1ff097384ee18cec4d575ec0e7f6a77624680f7d1a1173806f3749620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:275d39863006dda76b789416371b29a20c07f813757d5ff6fe5a7f589a95ddbc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124696202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d43eebb5dc67189ef4002d62c8832fe741072fb9a2ff192c6a4510297bd2124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:32:08 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 May 2021 01:32:08 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Tue, 25 May 2021 01:32:09 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:32 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ee0e9d235e101dc935c62412bd102e1d755dde7fce5763d226f026552f8655`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce620aed7bb3037346d75f048d23885d5bb803a21e1e55ec34e4cc3d0f1c2192`  
		Last Modified: Tue, 25 May 2021 01:36:25 GMT  
		Size: 84.8 MB (84763111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70651d0d1cfe57e4df1130d8bb28038e63c2455eed5b6db43972c74daad8686`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebd67bda7bab9468c0e67aae78a33c8e8a62de1b8667edef54026c143f1ba09`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e19adfc2335a54d0ffe2fb525d2777923fc2d71620f6d3130db9ea821d2b7c82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122225628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0305fc9557048568c4565579e95dd3507804bf10c123db402334da91c82209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 00:47:56 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 00:47:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:15 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:16 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c30f3e876b59214b89a16eaf140ef175bfd090b6420a808ff095a385d7d792`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b6168d649c8cd42a6cd59b90b0da9f35a12e25c6834b36f10b2e06292c428`  
		Last Modified: Fri, 18 Jun 2021 00:52:57 GMT  
		Size: 84.0 MB (83988817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9324009e782ea65db1057a9534d407c4d034db9363bfbc499a06f692b1a5f7`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff93debfa336b5bbd05bb6f7b7258d1641d98cec22f79d3c4fb4bf0e0aa59a6b`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9142245eb106781c06e372df5cc359d58afd1c6156dd7f270b3df4157fe85ce5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135459575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58d6d0bc1da4ae25e0b6b9340fbaa5d2e00e5a0d75b4f8cc8f4475b82495053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:39 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 May 2021 01:30:43 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Tue, 25 May 2021 01:31:00 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:34:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:34:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:34:59 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:35:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:35:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:35:20 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:35:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4b2f9bea375bc392ce4079b353e96b2a9c75d00242a2b32618e3fb1d4f3b84`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f54e4906fb47302470ab68459e5897e41913620346de177f2f53c3f4c69d27c`  
		Last Modified: Tue, 25 May 2021 01:48:00 GMT  
		Size: 89.2 MB (89229189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f361d137a165fa8650608e8d736df357998ba1a066cd533c2d1d85286aa6b8`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 5.6 KB (5553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431e45653a1adfb372f7a0298d5067e039a89875074a299cd0c12ac383462405`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:928473e1ff097384ee18cec4d575ec0e7f6a77624680f7d1a1173806f3749620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:275d39863006dda76b789416371b29a20c07f813757d5ff6fe5a7f589a95ddbc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124696202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d43eebb5dc67189ef4002d62c8832fe741072fb9a2ff192c6a4510297bd2124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:32:08 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 May 2021 01:32:08 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Tue, 25 May 2021 01:32:09 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:32 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ee0e9d235e101dc935c62412bd102e1d755dde7fce5763d226f026552f8655`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce620aed7bb3037346d75f048d23885d5bb803a21e1e55ec34e4cc3d0f1c2192`  
		Last Modified: Tue, 25 May 2021 01:36:25 GMT  
		Size: 84.8 MB (84763111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70651d0d1cfe57e4df1130d8bb28038e63c2455eed5b6db43972c74daad8686`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebd67bda7bab9468c0e67aae78a33c8e8a62de1b8667edef54026c143f1ba09`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e19adfc2335a54d0ffe2fb525d2777923fc2d71620f6d3130db9ea821d2b7c82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122225628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0305fc9557048568c4565579e95dd3507804bf10c123db402334da91c82209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 00:47:56 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 00:47:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:15 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:16 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c30f3e876b59214b89a16eaf140ef175bfd090b6420a808ff095a385d7d792`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b6168d649c8cd42a6cd59b90b0da9f35a12e25c6834b36f10b2e06292c428`  
		Last Modified: Fri, 18 Jun 2021 00:52:57 GMT  
		Size: 84.0 MB (83988817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9324009e782ea65db1057a9534d407c4d034db9363bfbc499a06f692b1a5f7`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff93debfa336b5bbd05bb6f7b7258d1641d98cec22f79d3c4fb4bf0e0aa59a6b`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9142245eb106781c06e372df5cc359d58afd1c6156dd7f270b3df4157fe85ce5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135459575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58d6d0bc1da4ae25e0b6b9340fbaa5d2e00e5a0d75b4f8cc8f4475b82495053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:39 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 May 2021 01:30:43 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Tue, 25 May 2021 01:31:00 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:34:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:34:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:34:59 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:35:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:35:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:35:20 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:35:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4b2f9bea375bc392ce4079b353e96b2a9c75d00242a2b32618e3fb1d4f3b84`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f54e4906fb47302470ab68459e5897e41913620346de177f2f53c3f4c69d27c`  
		Last Modified: Tue, 25 May 2021 01:48:00 GMT  
		Size: 89.2 MB (89229189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f361d137a165fa8650608e8d736df357998ba1a066cd533c2d1d85286aa6b8`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 5.6 KB (5553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431e45653a1adfb372f7a0298d5067e039a89875074a299cd0c12ac383462405`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.19`

```console
$ docker pull mariadb@sha256:928473e1ff097384ee18cec4d575ec0e7f6a77624680f7d1a1173806f3749620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.19` - linux; amd64

```console
$ docker pull mariadb@sha256:275d39863006dda76b789416371b29a20c07f813757d5ff6fe5a7f589a95ddbc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124696202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d43eebb5dc67189ef4002d62c8832fe741072fb9a2ff192c6a4510297bd2124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:32:08 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 May 2021 01:32:08 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Tue, 25 May 2021 01:32:09 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:32 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ee0e9d235e101dc935c62412bd102e1d755dde7fce5763d226f026552f8655`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce620aed7bb3037346d75f048d23885d5bb803a21e1e55ec34e4cc3d0f1c2192`  
		Last Modified: Tue, 25 May 2021 01:36:25 GMT  
		Size: 84.8 MB (84763111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70651d0d1cfe57e4df1130d8bb28038e63c2455eed5b6db43972c74daad8686`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebd67bda7bab9468c0e67aae78a33c8e8a62de1b8667edef54026c143f1ba09`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.19` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e19adfc2335a54d0ffe2fb525d2777923fc2d71620f6d3130db9ea821d2b7c82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122225628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0305fc9557048568c4565579e95dd3507804bf10c123db402334da91c82209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 00:47:56 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 00:47:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:15 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:16 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c30f3e876b59214b89a16eaf140ef175bfd090b6420a808ff095a385d7d792`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b6168d649c8cd42a6cd59b90b0da9f35a12e25c6834b36f10b2e06292c428`  
		Last Modified: Fri, 18 Jun 2021 00:52:57 GMT  
		Size: 84.0 MB (83988817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9324009e782ea65db1057a9534d407c4d034db9363bfbc499a06f692b1a5f7`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff93debfa336b5bbd05bb6f7b7258d1641d98cec22f79d3c4fb4bf0e0aa59a6b`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.19` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9142245eb106781c06e372df5cc359d58afd1c6156dd7f270b3df4157fe85ce5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135459575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58d6d0bc1da4ae25e0b6b9340fbaa5d2e00e5a0d75b4f8cc8f4475b82495053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:39 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 May 2021 01:30:43 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Tue, 25 May 2021 01:31:00 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:34:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:34:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:34:59 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:35:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:35:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:35:20 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:35:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4b2f9bea375bc392ce4079b353e96b2a9c75d00242a2b32618e3fb1d4f3b84`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f54e4906fb47302470ab68459e5897e41913620346de177f2f53c3f4c69d27c`  
		Last Modified: Tue, 25 May 2021 01:48:00 GMT  
		Size: 89.2 MB (89229189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f361d137a165fa8650608e8d736df357998ba1a066cd533c2d1d85286aa6b8`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 5.6 KB (5553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431e45653a1adfb372f7a0298d5067e039a89875074a299cd0c12ac383462405`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.19-focal`

```console
$ docker pull mariadb@sha256:928473e1ff097384ee18cec4d575ec0e7f6a77624680f7d1a1173806f3749620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.19-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:275d39863006dda76b789416371b29a20c07f813757d5ff6fe5a7f589a95ddbc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124696202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d43eebb5dc67189ef4002d62c8832fe741072fb9a2ff192c6a4510297bd2124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:32:08 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 May 2021 01:32:08 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Tue, 25 May 2021 01:32:09 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:32 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ee0e9d235e101dc935c62412bd102e1d755dde7fce5763d226f026552f8655`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce620aed7bb3037346d75f048d23885d5bb803a21e1e55ec34e4cc3d0f1c2192`  
		Last Modified: Tue, 25 May 2021 01:36:25 GMT  
		Size: 84.8 MB (84763111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70651d0d1cfe57e4df1130d8bb28038e63c2455eed5b6db43972c74daad8686`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebd67bda7bab9468c0e67aae78a33c8e8a62de1b8667edef54026c143f1ba09`  
		Last Modified: Tue, 25 May 2021 01:36:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.19-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e19adfc2335a54d0ffe2fb525d2777923fc2d71620f6d3130db9ea821d2b7c82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122225628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0305fc9557048568c4565579e95dd3507804bf10c123db402334da91c82209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:55 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 18 Jun 2021 00:47:56 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Fri, 18 Jun 2021 00:47:56 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:48:14 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:48:14 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:48:15 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:48:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 18 Jun 2021 00:48:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:48:16 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:48:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c30f3e876b59214b89a16eaf140ef175bfd090b6420a808ff095a385d7d792`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75b6168d649c8cd42a6cd59b90b0da9f35a12e25c6834b36f10b2e06292c428`  
		Last Modified: Fri, 18 Jun 2021 00:52:57 GMT  
		Size: 84.0 MB (83988817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9324009e782ea65db1057a9534d407c4d034db9363bfbc499a06f692b1a5f7`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff93debfa336b5bbd05bb6f7b7258d1641d98cec22f79d3c4fb4bf0e0aa59a6b`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.19-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9142245eb106781c06e372df5cc359d58afd1c6156dd7f270b3df4157fe85ce5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135459575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58d6d0bc1da4ae25e0b6b9340fbaa5d2e00e5a0d75b4f8cc8f4475b82495053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:39 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 May 2021 01:30:43 GMT
ENV MARIADB_VERSION=1:10.4.19+maria~focal
# Tue, 25 May 2021 01:31:00 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:34:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:34:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:34:59 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:35:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 May 2021 01:35:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:35:20 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:35:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4b2f9bea375bc392ce4079b353e96b2a9c75d00242a2b32618e3fb1d4f3b84`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f54e4906fb47302470ab68459e5897e41913620346de177f2f53c3f4c69d27c`  
		Last Modified: Tue, 25 May 2021 01:48:00 GMT  
		Size: 89.2 MB (89229189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f361d137a165fa8650608e8d736df357998ba1a066cd533c2d1d85286aa6b8`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 5.6 KB (5553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431e45653a1adfb372f7a0298d5067e039a89875074a299cd0c12ac383462405`  
		Last Modified: Tue, 25 May 2021 01:47:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:dadddd5cafc1b961e7eaf0e63b03ddea89962ae9a1ea4f7bb82d57c21b8bbbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:157b7dfff69497562abc03082d031ac2f043567d87f6ae877bb8ccc067fdb614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff629089685eb7051a239d4217f334580c09e557a9ecfeb2d562a1229d10e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:31:43 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:03 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34793730ad6f7322af1b69c65471c25adb2e7739d954894435d02a82a58d87b`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1925a0d7347a97b60fede940e8d3e2d5f761015eb37cea3dce2b8c9f0d5095`  
		Last Modified: Tue, 25 May 2021 01:35:42 GMT  
		Size: 86.9 MB (86940364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72904fb5fd0bc88de81123be54f24d16fd5024961fde989b9501a4a66ee48580`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a76a8f43b61d45782ffa134b51b80c7e10c81d34b7fbcb1d4afc13dc02be5966
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d789912dc9b6b5d3b3c3ec0af513eabb3b6fced34f588afeb58ac6c069c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:25:12 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:25:17 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:25:33 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:29:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:29:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:29:43 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:29:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:30:16 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:30:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7e38f200818e3b4dec6bc9e27f260a59371cac67cb36b9a360361bd7b0b74`  
		Last Modified: Tue, 25 May 2021 01:46:53 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3189ef563ff0a2133db70e0ecb9f0f2d7a31f76d38f7869633550a4259fbb`  
		Last Modified: Tue, 25 May 2021 01:47:13 GMT  
		Size: 91.3 MB (91324471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f2195dfcfba5e84626d5cfe648a32dfd22d44e0b33603ada234778f777f3cc`  
		Last Modified: Tue, 25 May 2021 01:46:55 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:dadddd5cafc1b961e7eaf0e63b03ddea89962ae9a1ea4f7bb82d57c21b8bbbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:157b7dfff69497562abc03082d031ac2f043567d87f6ae877bb8ccc067fdb614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff629089685eb7051a239d4217f334580c09e557a9ecfeb2d562a1229d10e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:31:43 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:03 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34793730ad6f7322af1b69c65471c25adb2e7739d954894435d02a82a58d87b`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1925a0d7347a97b60fede940e8d3e2d5f761015eb37cea3dce2b8c9f0d5095`  
		Last Modified: Tue, 25 May 2021 01:35:42 GMT  
		Size: 86.9 MB (86940364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72904fb5fd0bc88de81123be54f24d16fd5024961fde989b9501a4a66ee48580`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a76a8f43b61d45782ffa134b51b80c7e10c81d34b7fbcb1d4afc13dc02be5966
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d789912dc9b6b5d3b3c3ec0af513eabb3b6fced34f588afeb58ac6c069c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:25:12 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:25:17 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:25:33 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:29:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:29:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:29:43 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:29:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:30:16 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:30:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7e38f200818e3b4dec6bc9e27f260a59371cac67cb36b9a360361bd7b0b74`  
		Last Modified: Tue, 25 May 2021 01:46:53 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3189ef563ff0a2133db70e0ecb9f0f2d7a31f76d38f7869633550a4259fbb`  
		Last Modified: Tue, 25 May 2021 01:47:13 GMT  
		Size: 91.3 MB (91324471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f2195dfcfba5e84626d5cfe648a32dfd22d44e0b33603ada234778f777f3cc`  
		Last Modified: Tue, 25 May 2021 01:46:55 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.10`

```console
$ docker pull mariadb@sha256:dadddd5cafc1b961e7eaf0e63b03ddea89962ae9a1ea4f7bb82d57c21b8bbbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.10` - linux; amd64

```console
$ docker pull mariadb@sha256:157b7dfff69497562abc03082d031ac2f043567d87f6ae877bb8ccc067fdb614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff629089685eb7051a239d4217f334580c09e557a9ecfeb2d562a1229d10e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:31:43 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:03 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34793730ad6f7322af1b69c65471c25adb2e7739d954894435d02a82a58d87b`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1925a0d7347a97b60fede940e8d3e2d5f761015eb37cea3dce2b8c9f0d5095`  
		Last Modified: Tue, 25 May 2021 01:35:42 GMT  
		Size: 86.9 MB (86940364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72904fb5fd0bc88de81123be54f24d16fd5024961fde989b9501a4a66ee48580`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a76a8f43b61d45782ffa134b51b80c7e10c81d34b7fbcb1d4afc13dc02be5966
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d789912dc9b6b5d3b3c3ec0af513eabb3b6fced34f588afeb58ac6c069c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:25:12 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:25:17 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:25:33 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:29:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:29:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:29:43 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:29:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:30:16 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:30:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7e38f200818e3b4dec6bc9e27f260a59371cac67cb36b9a360361bd7b0b74`  
		Last Modified: Tue, 25 May 2021 01:46:53 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3189ef563ff0a2133db70e0ecb9f0f2d7a31f76d38f7869633550a4259fbb`  
		Last Modified: Tue, 25 May 2021 01:47:13 GMT  
		Size: 91.3 MB (91324471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f2195dfcfba5e84626d5cfe648a32dfd22d44e0b33603ada234778f777f3cc`  
		Last Modified: Tue, 25 May 2021 01:46:55 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.10-focal`

```console
$ docker pull mariadb@sha256:dadddd5cafc1b961e7eaf0e63b03ddea89962ae9a1ea4f7bb82d57c21b8bbbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:157b7dfff69497562abc03082d031ac2f043567d87f6ae877bb8ccc067fdb614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff629089685eb7051a239d4217f334580c09e557a9ecfeb2d562a1229d10e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:31:43 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:03 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34793730ad6f7322af1b69c65471c25adb2e7739d954894435d02a82a58d87b`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1925a0d7347a97b60fede940e8d3e2d5f761015eb37cea3dce2b8c9f0d5095`  
		Last Modified: Tue, 25 May 2021 01:35:42 GMT  
		Size: 86.9 MB (86940364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72904fb5fd0bc88de81123be54f24d16fd5024961fde989b9501a4a66ee48580`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a76a8f43b61d45782ffa134b51b80c7e10c81d34b7fbcb1d4afc13dc02be5966
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d789912dc9b6b5d3b3c3ec0af513eabb3b6fced34f588afeb58ac6c069c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:25:12 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:25:17 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:25:33 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:29:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:29:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:29:43 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:29:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:30:16 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:30:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7e38f200818e3b4dec6bc9e27f260a59371cac67cb36b9a360361bd7b0b74`  
		Last Modified: Tue, 25 May 2021 01:46:53 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3189ef563ff0a2133db70e0ecb9f0f2d7a31f76d38f7869633550a4259fbb`  
		Last Modified: Tue, 25 May 2021 01:47:13 GMT  
		Size: 91.3 MB (91324471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f2195dfcfba5e84626d5cfe648a32dfd22d44e0b33603ada234778f777f3cc`  
		Last Modified: Tue, 25 May 2021 01:46:55 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:4f2e4db786a63c5f3a003247b9d08154d915908a147494e4a71f039229a03e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:61219a7650b0eba10bd58c8d6a432220a070065117d1022b1b18a112cf046a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127044905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e0714b4fb9b7627577ee9d48cf363c047159094bbda4ba97d9d59a323df5c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:30:50 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:31:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:31:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:31:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:31:31 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b5204365a9ca7c95da5efb67af20026e76148387b57554879ff4f345f4b4cb`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b478f14e56810db0ddbe484a00dd40ff0b7b7099743d491002fa98d5aac7b602`  
		Last Modified: Tue, 25 May 2021 01:35:03 GMT  
		Size: 87.1 MB (87111933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906c1430d7ac95f9fe39c317c6a1f8216876cf5bad49ff6ed4c6f7e451aa485`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f6e2677233797addbf7011c36bd44f302f77dd6c74063f9cdcce3c08026539a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137541780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a18541b2448bcb6d551a2776d940c512e4db40e41b7d1c7294937f2a7f05c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:18:20 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:18:26 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:18:37 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:24:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:24:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:24:27 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:24:44 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:24:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a163a3566cc659c28afa0ae329856e9991fdccbd330a817acb937d7e1ba0f273`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf30a21e01587f4f084b4871856a8862c3f8ec639627c8dbe7dba05111013a0`  
		Last Modified: Tue, 25 May 2021 01:46:30 GMT  
		Size: 91.3 MB (91311514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3f371fa50f5a20b5b7db4b920ba6d6c0a6bfa8a4316a8c65c38a6763b7c13`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:4f2e4db786a63c5f3a003247b9d08154d915908a147494e4a71f039229a03e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:61219a7650b0eba10bd58c8d6a432220a070065117d1022b1b18a112cf046a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127044905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e0714b4fb9b7627577ee9d48cf363c047159094bbda4ba97d9d59a323df5c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:30:50 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:31:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:31:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:31:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:31:31 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b5204365a9ca7c95da5efb67af20026e76148387b57554879ff4f345f4b4cb`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b478f14e56810db0ddbe484a00dd40ff0b7b7099743d491002fa98d5aac7b602`  
		Last Modified: Tue, 25 May 2021 01:35:03 GMT  
		Size: 87.1 MB (87111933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906c1430d7ac95f9fe39c317c6a1f8216876cf5bad49ff6ed4c6f7e451aa485`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f6e2677233797addbf7011c36bd44f302f77dd6c74063f9cdcce3c08026539a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137541780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a18541b2448bcb6d551a2776d940c512e4db40e41b7d1c7294937f2a7f05c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:18:20 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:18:26 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:18:37 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:24:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:24:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:24:27 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:24:44 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:24:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a163a3566cc659c28afa0ae329856e9991fdccbd330a817acb937d7e1ba0f273`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf30a21e01587f4f084b4871856a8862c3f8ec639627c8dbe7dba05111013a0`  
		Last Modified: Tue, 25 May 2021 01:46:30 GMT  
		Size: 91.3 MB (91311514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3f371fa50f5a20b5b7db4b920ba6d6c0a6bfa8a4316a8c65c38a6763b7c13`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.1`

```console
$ docker pull mariadb@sha256:4f2e4db786a63c5f3a003247b9d08154d915908a147494e4a71f039229a03e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.1` - linux; amd64

```console
$ docker pull mariadb@sha256:61219a7650b0eba10bd58c8d6a432220a070065117d1022b1b18a112cf046a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127044905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e0714b4fb9b7627577ee9d48cf363c047159094bbda4ba97d9d59a323df5c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:30:50 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:31:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:31:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:31:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:31:31 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b5204365a9ca7c95da5efb67af20026e76148387b57554879ff4f345f4b4cb`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b478f14e56810db0ddbe484a00dd40ff0b7b7099743d491002fa98d5aac7b602`  
		Last Modified: Tue, 25 May 2021 01:35:03 GMT  
		Size: 87.1 MB (87111933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906c1430d7ac95f9fe39c317c6a1f8216876cf5bad49ff6ed4c6f7e451aa485`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f6e2677233797addbf7011c36bd44f302f77dd6c74063f9cdcce3c08026539a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137541780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a18541b2448bcb6d551a2776d940c512e4db40e41b7d1c7294937f2a7f05c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:18:20 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:18:26 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:18:37 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:24:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:24:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:24:27 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:24:44 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:24:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a163a3566cc659c28afa0ae329856e9991fdccbd330a817acb937d7e1ba0f273`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf30a21e01587f4f084b4871856a8862c3f8ec639627c8dbe7dba05111013a0`  
		Last Modified: Tue, 25 May 2021 01:46:30 GMT  
		Size: 91.3 MB (91311514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3f371fa50f5a20b5b7db4b920ba6d6c0a6bfa8a4316a8c65c38a6763b7c13`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.1-focal`

```console
$ docker pull mariadb@sha256:4f2e4db786a63c5f3a003247b9d08154d915908a147494e4a71f039229a03e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.1-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:61219a7650b0eba10bd58c8d6a432220a070065117d1022b1b18a112cf046a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127044905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e0714b4fb9b7627577ee9d48cf363c047159094bbda4ba97d9d59a323df5c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:30:50 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:31:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:31:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:31:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:31:31 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b5204365a9ca7c95da5efb67af20026e76148387b57554879ff4f345f4b4cb`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b478f14e56810db0ddbe484a00dd40ff0b7b7099743d491002fa98d5aac7b602`  
		Last Modified: Tue, 25 May 2021 01:35:03 GMT  
		Size: 87.1 MB (87111933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906c1430d7ac95f9fe39c317c6a1f8216876cf5bad49ff6ed4c6f7e451aa485`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.1-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.1-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f6e2677233797addbf7011c36bd44f302f77dd6c74063f9cdcce3c08026539a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137541780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a18541b2448bcb6d551a2776d940c512e4db40e41b7d1c7294937f2a7f05c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:18:20 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:18:26 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:18:37 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:24:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:24:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:24:27 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:24:44 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:24:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a163a3566cc659c28afa0ae329856e9991fdccbd330a817acb937d7e1ba0f273`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf30a21e01587f4f084b4871856a8862c3f8ec639627c8dbe7dba05111013a0`  
		Last Modified: Tue, 25 May 2021 01:46:30 GMT  
		Size: 91.3 MB (91311514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3f371fa50f5a20b5b7db4b920ba6d6c0a6bfa8a4316a8c65c38a6763b7c13`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:beta`

```console
$ docker pull mariadb@sha256:4f2e4db786a63c5f3a003247b9d08154d915908a147494e4a71f039229a03e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:beta` - linux; amd64

```console
$ docker pull mariadb@sha256:61219a7650b0eba10bd58c8d6a432220a070065117d1022b1b18a112cf046a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127044905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e0714b4fb9b7627577ee9d48cf363c047159094bbda4ba97d9d59a323df5c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:30:50 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:31:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:31:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:31:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:31:31 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b5204365a9ca7c95da5efb67af20026e76148387b57554879ff4f345f4b4cb`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b478f14e56810db0ddbe484a00dd40ff0b7b7099743d491002fa98d5aac7b602`  
		Last Modified: Tue, 25 May 2021 01:35:03 GMT  
		Size: 87.1 MB (87111933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906c1430d7ac95f9fe39c317c6a1f8216876cf5bad49ff6ed4c6f7e451aa485`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f6e2677233797addbf7011c36bd44f302f77dd6c74063f9cdcce3c08026539a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137541780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a18541b2448bcb6d551a2776d940c512e4db40e41b7d1c7294937f2a7f05c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:18:20 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:18:26 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:18:37 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:24:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:24:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:24:27 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:24:44 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:24:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a163a3566cc659c28afa0ae329856e9991fdccbd330a817acb937d7e1ba0f273`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf30a21e01587f4f084b4871856a8862c3f8ec639627c8dbe7dba05111013a0`  
		Last Modified: Tue, 25 May 2021 01:46:30 GMT  
		Size: 91.3 MB (91311514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3f371fa50f5a20b5b7db4b920ba6d6c0a6bfa8a4316a8c65c38a6763b7c13`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:beta-focal`

```console
$ docker pull mariadb@sha256:4f2e4db786a63c5f3a003247b9d08154d915908a147494e4a71f039229a03e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:beta-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:61219a7650b0eba10bd58c8d6a432220a070065117d1022b1b18a112cf046a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127044905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e0714b4fb9b7627577ee9d48cf363c047159094bbda4ba97d9d59a323df5c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:30:49 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:30:50 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:31:30 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:31:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:31:31 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:31:31 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:31:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b5204365a9ca7c95da5efb67af20026e76148387b57554879ff4f345f4b4cb`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b478f14e56810db0ddbe484a00dd40ff0b7b7099743d491002fa98d5aac7b602`  
		Last Modified: Tue, 25 May 2021 01:35:03 GMT  
		Size: 87.1 MB (87111933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906c1430d7ac95f9fe39c317c6a1f8216876cf5bad49ff6ed4c6f7e451aa485`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 5.6 KB (5552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c3bd5ecd8eceaec62d6b3e0fcc67834deeec3e7c3f44008d090fce5655c1ac7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6aed3eece7753e7e29884d157824d324e5c5d8e14e5af94ae0a4f3ff1bc56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 18 Jun 2021 00:46:40 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Fri, 18 Jun 2021 00:46:40 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:13 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:13 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:13 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:14 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb511928dd3ccf44ab0b0a64c949c979646c5276383436ef92c35ea7f2682385`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb643dc9a71b23adeb8ba5abf5f3a4ddeb9b26e85d3473fd45f292f5a3bf7d`  
		Last Modified: Fri, 18 Jun 2021 00:51:20 GMT  
		Size: 86.1 MB (86080508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7f191c9736c124776de5eb233fb682826b0ae489f5907590f8ccedbfc157d5`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 5.5 KB (5550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:beta-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f6e2677233797addbf7011c36bd44f302f77dd6c74063f9cdcce3c08026539a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137541780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a18541b2448bcb6d551a2776d940c512e4db40e41b7d1c7294937f2a7f05c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:18:20 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 May 2021 01:18:26 GMT
ENV MARIADB_VERSION=1:10.6.1+maria~focal
# Tue, 25 May 2021 01:18:37 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:24:12 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:24:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:24:27 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:24:44 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:24:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a163a3566cc659c28afa0ae329856e9991fdccbd330a817acb937d7e1ba0f273`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf30a21e01587f4f084b4871856a8862c3f8ec639627c8dbe7dba05111013a0`  
		Last Modified: Tue, 25 May 2021 01:46:30 GMT  
		Size: 91.3 MB (91311514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3f371fa50f5a20b5b7db4b920ba6d6c0a6bfa8a4316a8c65c38a6763b7c13`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:dadddd5cafc1b961e7eaf0e63b03ddea89962ae9a1ea4f7bb82d57c21b8bbbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:157b7dfff69497562abc03082d031ac2f043567d87f6ae877bb8ccc067fdb614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff629089685eb7051a239d4217f334580c09e557a9ecfeb2d562a1229d10e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:31:43 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:03 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34793730ad6f7322af1b69c65471c25adb2e7739d954894435d02a82a58d87b`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1925a0d7347a97b60fede940e8d3e2d5f761015eb37cea3dce2b8c9f0d5095`  
		Last Modified: Tue, 25 May 2021 01:35:42 GMT  
		Size: 86.9 MB (86940364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72904fb5fd0bc88de81123be54f24d16fd5024961fde989b9501a4a66ee48580`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a76a8f43b61d45782ffa134b51b80c7e10c81d34b7fbcb1d4afc13dc02be5966
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d789912dc9b6b5d3b3c3ec0af513eabb3b6fced34f588afeb58ac6c069c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:25:12 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:25:17 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:25:33 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:29:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:29:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:29:43 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:29:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:30:16 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:30:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7e38f200818e3b4dec6bc9e27f260a59371cac67cb36b9a360361bd7b0b74`  
		Last Modified: Tue, 25 May 2021 01:46:53 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3189ef563ff0a2133db70e0ecb9f0f2d7a31f76d38f7869633550a4259fbb`  
		Last Modified: Tue, 25 May 2021 01:47:13 GMT  
		Size: 91.3 MB (91324471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f2195dfcfba5e84626d5cfe648a32dfd22d44e0b33603ada234778f777f3cc`  
		Last Modified: Tue, 25 May 2021 01:46:55 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:dadddd5cafc1b961e7eaf0e63b03ddea89962ae9a1ea4f7bb82d57c21b8bbbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:157b7dfff69497562abc03082d031ac2f043567d87f6ae877bb8ccc067fdb614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff629089685eb7051a239d4217f334580c09e557a9ecfeb2d562a1229d10e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:31:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 00:31:55 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:31:55 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:20:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:30:47 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:30:47 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:30:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:31:42 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:31:43 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:32:02 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:32:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:32:03 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:32:03 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:32:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d512e2ff7788e9e77850c0a2830d054527a099b682ed31eadb5331161f96559`  
		Last Modified: Sat, 24 Apr 2021 00:36:36 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1a7dc2af94808125e8bd4d5ddfe0d556ff280e6897a9cef8276e1f6225f20`  
		Last Modified: Sat, 24 Apr 2021 00:36:37 GMT  
		Size: 5.5 MB (5490249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846f4f4774a636a7aaabb0485956e0f518f82813f475c9d300620f18684244a`  
		Last Modified: Thu, 29 Apr 2021 01:22:01 GMT  
		Size: 3.6 MB (3616543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66409f940bd2a845698f5b79a42c83cef49da0695a1c10dca09f100bb23ff58b`  
		Last Modified: Thu, 29 Apr 2021 01:22:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8723e99d8ec9e44569b502fa4b5dec4b7b78c632f980e408a67a485bf12d2`  
		Last Modified: Tue, 25 May 2021 01:34:50 GMT  
		Size: 2.3 MB (2275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edbf0f673ef71cf25dc7add611a29f750ac996d30465f92a9f1bf9b5c74e80`  
		Last Modified: Tue, 25 May 2021 01:34:49 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34793730ad6f7322af1b69c65471c25adb2e7739d954894435d02a82a58d87b`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1925a0d7347a97b60fede940e8d3e2d5f761015eb37cea3dce2b8c9f0d5095`  
		Last Modified: Tue, 25 May 2021 01:35:42 GMT  
		Size: 86.9 MB (86940364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72904fb5fd0bc88de81123be54f24d16fd5024961fde989b9501a4a66ee48580`  
		Last Modified: Tue, 25 May 2021 01:35:28 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3fe13f0508189db8cd6f48c53f1da1fe797e73a641e9e73c5dcace26c9b360e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124317601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f81ceae48a813d1b74901836a80bdec5895ad2282acb072de95b803afdaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:46:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Jun 2021 00:46:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:18 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:46:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:46:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:46:38 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:46:38 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 18 Jun 2021 00:46:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:47:21 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 18 Jun 2021 00:47:22 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Fri, 18 Jun 2021 00:47:22 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 18 Jun 2021 00:47:45 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 18 Jun 2021 00:47:46 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Jun 2021 00:47:46 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:47:47 GMT
EXPOSE 3306
# Fri, 18 Jun 2021 00:47:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2fb22009549c382a13f19944b1f677fbd86342fb82606d2d32e270f103554`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd425bf20e5a7b2f63ecc734c73ed6a0c78454e5db14f76a86cd5c725df84f42`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 5.5 MB (5455206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a1c12283e615cc52b8120fdf6b5790c90d118fa8f81ee02ec0eaef891fa69`  
		Last Modified: Fri, 18 Jun 2021 00:51:08 GMT  
		Size: 3.4 MB (3408886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aacdc09bed9ec05785f9401269330f831c51a52299e1e3f31d12b6ea17dab5f`  
		Last Modified: Fri, 18 Jun 2021 00:51:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb12dd133a39e5a4eacefab7d93cd33fcda892e3d2b632bc49051ac306ac43b`  
		Last Modified: Fri, 18 Jun 2021 00:51:05 GMT  
		Size: 2.2 MB (2203529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728725e0e7ee5f4e0df959349b452d9873bd8d7dbd72cc41fc76cb7610f8bc0`  
		Last Modified: Fri, 18 Jun 2021 00:51:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8250062aba98191628f6fd4e2796dc123e4b2e3ecfcbb04561cc61020f4071f`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aec5a7d68cd711e3bc620fa6494f3371b3dee98ea53e12eda3279d35cb8ea5`  
		Last Modified: Fri, 18 Jun 2021 00:52:02 GMT  
		Size: 86.1 MB (86080910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0e8f8dfa86306e199b6c0fc2fa7266020cbf2f2616a038d85db601a4a9268`  
		Last Modified: Fri, 18 Jun 2021 00:51:47 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a76a8f43b61d45782ffa134b51b80c7e10c81d34b7fbcb1d4afc13dc02be5966
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d789912dc9b6b5d3b3c3ec0af513eabb3b6fced34f588afeb58ac6c069c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:50:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 24 Apr 2021 01:51:59 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:52:04 GMT
ENV GOSU_VERSION=1.12
# Thu, 29 Apr 2021 01:18:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 29 Apr 2021 01:19:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 May 2021 01:17:53 GMT
RUN set -ex; 	apt-get update; 	if [ focal = focal ]; then JEMALLOC=libjemalloc2 ; else JEMALLOC=libjemalloc1 ; fi ; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		$JEMALLOC 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 May 2021 01:18:01 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 May 2021 01:18:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 25 May 2021 01:25:12 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 May 2021 01:25:17 GMT
ENV MARIADB_VERSION=1:10.5.10+maria~focal
# Tue, 25 May 2021 01:25:33 GMT
RUN set -e;	echo "deb https://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 May 2021 01:29:31 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 25 May 2021 01:29:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 May 2021 01:29:43 GMT
COPY file:faea8ed16a21bd1f33736424a74ad1147c62b6a1617716b4141cfd286e85fbba in /usr/local/bin/ 
# Tue, 25 May 2021 01:29:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:30:16 GMT
EXPOSE 3306
# Tue, 25 May 2021 01:30:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d305ff3127f29761eb61cc5752ae35b85fd17887d052bca1af891821908bf`  
		Last Modified: Sat, 24 Apr 2021 02:16:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a124c3f9fa2a98515fcfb8511b8ca6ae72304bb9d12506f7a0293357b7761e`  
		Last Modified: Sat, 24 Apr 2021 02:16:19 GMT  
		Size: 6.7 MB (6668282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e7011b7e217c2f9fbc460d0f0098e274bd2e6d466778b66f27d6a792e1ea0`  
		Last Modified: Thu, 29 Apr 2021 01:33:27 GMT  
		Size: 3.7 MB (3725366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bef0d6b3bcbd541db395ae2dfc35fea92e8630019777cc5e43bc0b3132a2b49`  
		Last Modified: Thu, 29 Apr 2021 01:33:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ccc32193568427ee0735e75c70dea161ad17d53477b427f00089a11271c5c`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.6 MB (2569910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67235b23fb562cbcaec9fca8ece4ec5b3c8b87dd0b35c54c2db7def4c1eecac6`  
		Last Modified: Tue, 25 May 2021 01:46:11 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7e38f200818e3b4dec6bc9e27f260a59371cac67cb36b9a360361bd7b0b74`  
		Last Modified: Tue, 25 May 2021 01:46:53 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3189ef563ff0a2133db70e0ecb9f0f2d7a31f76d38f7869633550a4259fbb`  
		Last Modified: Tue, 25 May 2021 01:47:13 GMT  
		Size: 91.3 MB (91324471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f2195dfcfba5e84626d5cfe648a32dfd22d44e0b33603ada234778f777f3cc`  
		Last Modified: Tue, 25 May 2021 01:46:55 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
