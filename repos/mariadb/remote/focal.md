## `mariadb:focal`

```console
$ docker pull mariadb@sha256:3ce8368efbf25059a1b7d2ff1df9f1cdb52fcd272eb2b906599e8613971379bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:b0fe725e9008b651ee0577383887728879986580d1e0a809dc263a04d1c40907
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c9d63e23e3408f9615c5519ef1a540874e867460268af29993862155376a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:23:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:23:54 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:23:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:24:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:24:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:24:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:24:11 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:24:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:25:02 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:25:03 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:25:22 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:25:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:25:23 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:25:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:25:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:25:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95055cb8335894c3fabf02a904c12b90e7094e3627fcbb5631501b7e958e4287`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e31373a05022078fcb09f0a1d3e4fea6a8c88e529d00fc599af935b5722494`  
		Last Modified: Fri, 12 Jun 2020 18:26:23 GMT  
		Size: 5.5 MB (5489816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e79b86f5e7cdb29805f606987eafae747b3da63512b9b469a772d74571f1c`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 1.3 MB (1322554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710b48e9f329e6bb99182358e4bc435de590fc2bd13d57f6356a2611c85f6e`  
		Last Modified: Fri, 12 Jun 2020 18:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfd17df805b72b4a878fb86967777aa86cae5bdf091c7258a32821a11d4e6`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 1.3 MB (1264394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423646bf79d8324ab8c55c8ca28af6ec1548f741632bb73926b9fba128e45cf1`  
		Last Modified: Fri, 12 Jun 2020 18:26:21 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075a6a30ab84cd85dbfe7ff6b7ff4b1da51420bb6502fbbcd165a6362314d89`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d12c1b8c73e8aaa38978b59b62c4a6d88faaf072f8dd8170cc20c995ea6182`  
		Last Modified: Fri, 12 Jun 2020 18:27:01 GMT  
		Size: 86.9 MB (86868588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10938405ff505cbefc2abf93e72607642d6d13d611bf1df914c7ccc62f2010fa`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656315d96d9326a97929d688679e34d594759499e9f6e6652ce44a70d285c64`  
		Last Modified: Fri, 12 Jun 2020 18:26:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c7b8ef0282a747aa0e686f5c2d3b68f050f8d5aebc51884681057f3d6bab5af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121139407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227094abd47e39aba82a11a0d4aff3492e3733207529c4fb90f4d1fa8299d10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:53:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:53:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:53:46 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:54:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:54:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:54:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:54:14 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:54:17 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:55:26 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:55:28 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 18:56:18 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 18:56:20 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 18:56:21 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 18:56:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 18:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 18:56:24 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 18:56:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959e86d4d132b0e91456f1d1ecc3b1d6518d720b7ee82926559fd34800d7b53`  
		Last Modified: Fri, 12 Jun 2020 18:58:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f37953089cdddf8b409b61f0f30de595d96483dd0ce38463384dd5d201b70f`  
		Last Modified: Fri, 12 Jun 2020 18:58:19 GMT  
		Size: 5.5 MB (5456917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7a5713dbb2830a805d0b68dae96ce4dd827b086473a3d785f76b37d885fe1`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 1.3 MB (1258973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0614221a0d602714b38672c572d4071df43a41223dab9b1c81ab45ea5bc9c9`  
		Last Modified: Fri, 12 Jun 2020 18:58:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e232435757d992d57a40890acb9528958726ef62b7f400e4ef7c3b7d97c234c`  
		Last Modified: Fri, 12 Jun 2020 18:58:16 GMT  
		Size: 1.3 MB (1263367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb430a3947464ff3d178d412e9047e4b67e2cc3a09923dd4b84596fa57403d66`  
		Last Modified: Fri, 12 Jun 2020 18:58:15 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366377b87f5bd2fac450a70e60f1eb72d08d295b001fe3744ab2ce6aba51c50`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2724d7dec4121bbe85b94aa2443356afd739e9b04e6adfc6f42b6b6e905a95f7`  
		Last Modified: Fri, 12 Jun 2020 18:59:19 GMT  
		Size: 86.0 MB (85958453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c46e43e925893ef88759184e58a70d17f45392e6524dfddf0d68becb6077b9`  
		Last Modified: Fri, 12 Jun 2020 18:58:52 GMT  
		Size: 4.9 KB (4851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77187f1fde12afc91b5b14093343ab71bc1d97ed7e79c60e4722d5c39ea0ca`  
		Last Modified: Fri, 12 Jun 2020 18:58:53 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a1705f7fecaefda698c2cf024327bca91cb8f66f2103614ae4d050f3ae194a4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133498155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d3057995bde70b21d4b3cf61e8df037115877ab7f95cdf5326e78e3c2020c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Apr 2020 20:45:24 GMT
ADD file:728be6ecddae6cfcc0b26f9ac98bbd7785141f023f3214748baf1b406583252e in / 
# Thu, 23 Apr 2020 20:45:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:45:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:45:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:45:46 GMT
CMD ["/bin/bash"]
# Fri, 12 Jun 2020 18:39:48 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 12 Jun 2020 18:43:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:43:48 GMT
ENV GOSU_VERSION=1.12
# Fri, 12 Jun 2020 18:47:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 12 Jun 2020 18:47:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Jun 2020 18:48:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		pwgen 		tzdata 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jun 2020 18:48:45 GMT
ENV GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 12 Jun 2020 18:49:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 12 Jun 2020 18:56:35 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 12 Jun 2020 18:56:46 GMT
ENV MARIADB_VERSION=1:10.4.13+maria~focal
# Fri, 12 Jun 2020 18:57:04 GMT
RUN set -e;	echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/ubuntu focal main" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 12 Jun 2020 19:02:53 GMT
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 	echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 12 Jun 2020 19:03:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 12 Jun 2020 19:03:18 GMT
COPY file:6d72a099e459fcc49252d2b0b35e8e28c9532e6d1ee1ec58d5781d2927de9fce in /usr/local/bin/ 
# Fri, 12 Jun 2020 19:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Jun 2020 19:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2020 19:04:08 GMT
EXPOSE 3306
# Fri, 12 Jun 2020 19:04:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ff4968e997bb90ab6c0b4cf753dd47a75adaae1ee06e1432096aba5475961e6`  
		Last Modified: Thu, 23 Apr 2020 20:50:07 GMT  
		Size: 33.3 MB (33278465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fac37502fee9b155891309da6d4ca7fb440465c7052671eaa9ce0ba754991d`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 32.2 KB (32154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dc4beee9352c457765d08eb16e82a7577df5c64b1eaba16b65aecdb63c7a51`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3051bd1f129e3b40bcda29bf66a6737e648569c90efb7de72518f9f07218b`  
		Last Modified: Thu, 23 Apr 2020 20:49:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431b0a8f934209f8d148ba16c9edcf421558e97d46130a4ac469349ea1b04ac`  
		Last Modified: Fri, 12 Jun 2020 19:13:22 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4efc2727182d1e55593344e2be654a48edf0d39d0924ac2f7822a19268d90`  
		Last Modified: Fri, 12 Jun 2020 19:13:23 GMT  
		Size: 6.7 MB (6671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9a8497b9ff967fdd0d1f0151a675edb8189e3b1f8c890b3848d94204d7643f`  
		Last Modified: Fri, 12 Jun 2020 19:13:20 GMT  
		Size: 1.2 MB (1242299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1151e4f33e285363966a4f276477f93629b675bd177c6a9ca61d97dafc9349`  
		Last Modified: Fri, 12 Jun 2020 19:13:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae27ebb1029bf8984a3b7fb97b21a50a91c73b4176f8707cf5089bc04aa9fd`  
		Last Modified: Fri, 12 Jun 2020 19:13:14 GMT  
		Size: 1.3 MB (1275536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5926d706f3725e6b6557d1630b18160883f102b16a6a88258dbd4aae4faf44`  
		Last Modified: Fri, 12 Jun 2020 19:13:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b359a03f81831c2fd57d9416ebc819388fd8574d85ad8898645d72f66c3c7`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09607cc66ed45e59b9ecfd2ed2dde55ce5b8e9b80729c7e1e9afa3c8d8e417ec`  
		Last Modified: Fri, 12 Jun 2020 19:14:23 GMT  
		Size: 91.0 MB (90987667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4bd398a89880ad4c07dbeb3afa3e02a724fbc012f4713549758f5ea6f58a11`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 4.9 KB (4852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfb689374ca4c43f6019d271c2cd0aa592a343710516129428cebb3c3cb9e3`  
		Last Modified: Fri, 12 Jun 2020 19:13:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
