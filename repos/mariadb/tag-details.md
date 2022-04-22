<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.43`](#mariadb10243)
-	[`mariadb:10.2.43-bionic`](#mariadb10243-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.34`](#mariadb10334)
-	[`mariadb:10.3.34-focal`](#mariadb10334-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.24`](#mariadb10424)
-	[`mariadb:10.4.24-focal`](#mariadb10424-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.15`](#mariadb10515)
-	[`mariadb:10.5.15-focal`](#mariadb10515-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.7`](#mariadb1067)
-	[`mariadb:10.6.7-focal`](#mariadb1067-focal)
-	[`mariadb:10.7`](#mariadb107)
-	[`mariadb:10.7-focal`](#mariadb107-focal)
-	[`mariadb:10.7.3`](#mariadb1073)
-	[`mariadb:10.7.3-focal`](#mariadb1073-focal)
-	[`mariadb:10.8-rc`](#mariadb108-rc)
-	[`mariadb:10.8-rc-focal`](#mariadb108-rc-focal)
-	[`mariadb:10.8.2-rc`](#mariadb1082-rc)
-	[`mariadb:10.8.2-rc-focal`](#mariadb1082-rc-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:fac573c78b2030f062d8582c81d3fa2e30c0922ed0843e0c85c4ac85109868b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:c5cefb5639e0f9360734406cb0f8b7a119c29083705059a1c4509cf31b6f1dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1ace59b072bf4850281c7a3262a76f762ef97d774a38f5a5cddda9514dd811`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:30 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:30 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8f6c64a8fa57732c8eb3db48d751c40e0795aa5ca42f05d27c2e9ab31075bc`  
		Last Modified: Fri, 22 Apr 2022 02:55:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9817bd990fc72a53340f7dfdda9343811b5a6f4cbc914369c092d3994a044a`  
		Last Modified: Fri, 22 Apr 2022 02:55:56 GMT  
		Size: 88.7 MB (88741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14828b87067569c6589bb8a62987321b440e088af17c5e8a0163841f3bba2e26`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233be9bdce04aeae1b3a83158f299fccc9e8ef3535617d5ea40ebe5b9dcac8c6`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:796e80b1be01d8549f5371e79b763d8f1bdb8fb2c37530461322ab5e031ae6dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125720109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beee7eb5f13c4d5c9266d5f791bf31c0ff9e79d90e09676e681da928dd09d2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:00 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:01 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:02 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:37:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:37:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:37:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:37:36 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:37:37 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:37:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd363ec17eba0ec2199c03d0185e2f6c14475cf6ceaed83743eff2f224300830`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25985e8a9660011351be8031303461ef7750186d9ff4c5b1b5a8dea2c855099`  
		Last Modified: Tue, 05 Apr 2022 23:44:29 GMT  
		Size: 87.6 MB (87644090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e720e62a0b31078f92f2b1d0ec407f671a0ff9f556e60f0388dd0b58f49a78f`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a050689af938e8cc8c031932ce64cbfbe13f9f6d5163bb03e5dbb2ba4b412e2`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2dc8d6c759f7bab790ce8cbedf00108435005a6bd5372d6b8402309499bb624b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139538511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421f250d9d97c128e04a281415cbe3e56ea7ba80b2113a776c867ec9c0c91ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:55:13 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:21 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:28 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:34 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:55:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:00:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:00:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:00:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:00:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:00:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:00:38 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:00:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641d6fa031615e90c40a726e13fcfad279784e3095cb5743a622e154a01718eb`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b30ede638c309a8dbf803c86421dce897625fff4aeec32dc718921a25fec337`  
		Last Modified: Wed, 06 Apr 2022 06:27:41 GMT  
		Size: 93.3 MB (93323824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a7b909e1bbdb359c1ae0a294cbeda191102e8cd1149689143b7852ebb6317`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e2336774b01c630d2ec6a19c2c0bddb5ae69fc59869c443b0d4dd7b668127`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; s390x

```console
$ docker pull mariadb@sha256:b2805c726caa7af5fe4e44a3ade5afbbb7f7c780567c147cb36b5c7a363464b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127722709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8b068ba5353d198e5fd7c34100da7ebc6771c257d75e23b80a211925de86aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:21:06 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:06 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:21:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:21:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:21:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:21:57 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:21:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e906a7a4ca515f29ae2f9d042b9d50795a7722dff0e54711609032ab009449`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa65ca376e03fed74f419a6a903362e83d6d4e1e1773ad67ad7183de7bbdf2`  
		Last Modified: Fri, 22 Apr 2022 02:26:26 GMT  
		Size: 89.8 MB (89815355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d48c43c28d400d613cd154b3e3182816a6e8b669d1fd7254e80bd5c51ae5f17`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b5541b27b08286050b0bfd633e5710b2273e67032af256ca1137c955ccbd51`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:fac573c78b2030f062d8582c81d3fa2e30c0922ed0843e0c85c4ac85109868b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:c5cefb5639e0f9360734406cb0f8b7a119c29083705059a1c4509cf31b6f1dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1ace59b072bf4850281c7a3262a76f762ef97d774a38f5a5cddda9514dd811`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:30 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:30 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8f6c64a8fa57732c8eb3db48d751c40e0795aa5ca42f05d27c2e9ab31075bc`  
		Last Modified: Fri, 22 Apr 2022 02:55:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9817bd990fc72a53340f7dfdda9343811b5a6f4cbc914369c092d3994a044a`  
		Last Modified: Fri, 22 Apr 2022 02:55:56 GMT  
		Size: 88.7 MB (88741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14828b87067569c6589bb8a62987321b440e088af17c5e8a0163841f3bba2e26`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233be9bdce04aeae1b3a83158f299fccc9e8ef3535617d5ea40ebe5b9dcac8c6`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:796e80b1be01d8549f5371e79b763d8f1bdb8fb2c37530461322ab5e031ae6dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125720109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beee7eb5f13c4d5c9266d5f791bf31c0ff9e79d90e09676e681da928dd09d2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:00 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:01 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:02 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:37:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:37:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:37:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:37:36 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:37:37 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:37:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd363ec17eba0ec2199c03d0185e2f6c14475cf6ceaed83743eff2f224300830`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25985e8a9660011351be8031303461ef7750186d9ff4c5b1b5a8dea2c855099`  
		Last Modified: Tue, 05 Apr 2022 23:44:29 GMT  
		Size: 87.6 MB (87644090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e720e62a0b31078f92f2b1d0ec407f671a0ff9f556e60f0388dd0b58f49a78f`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a050689af938e8cc8c031932ce64cbfbe13f9f6d5163bb03e5dbb2ba4b412e2`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2dc8d6c759f7bab790ce8cbedf00108435005a6bd5372d6b8402309499bb624b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139538511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421f250d9d97c128e04a281415cbe3e56ea7ba80b2113a776c867ec9c0c91ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:55:13 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:21 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:28 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:34 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:55:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:00:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:00:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:00:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:00:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:00:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:00:38 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:00:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641d6fa031615e90c40a726e13fcfad279784e3095cb5743a622e154a01718eb`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b30ede638c309a8dbf803c86421dce897625fff4aeec32dc718921a25fec337`  
		Last Modified: Wed, 06 Apr 2022 06:27:41 GMT  
		Size: 93.3 MB (93323824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a7b909e1bbdb359c1ae0a294cbeda191102e8cd1149689143b7852ebb6317`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e2336774b01c630d2ec6a19c2c0bddb5ae69fc59869c443b0d4dd7b668127`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:b2805c726caa7af5fe4e44a3ade5afbbb7f7c780567c147cb36b5c7a363464b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127722709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8b068ba5353d198e5fd7c34100da7ebc6771c257d75e23b80a211925de86aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:21:06 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:06 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:21:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:21:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:21:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:21:57 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:21:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e906a7a4ca515f29ae2f9d042b9d50795a7722dff0e54711609032ab009449`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa65ca376e03fed74f419a6a903362e83d6d4e1e1773ad67ad7183de7bbdf2`  
		Last Modified: Fri, 22 Apr 2022 02:26:26 GMT  
		Size: 89.8 MB (89815355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d48c43c28d400d613cd154b3e3182816a6e8b669d1fd7254e80bd5c51ae5f17`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b5541b27b08286050b0bfd633e5710b2273e67032af256ca1137c955ccbd51`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:8e3fc000ca8e9a0f928803c4fe97ae440c370c007e0faf2b8b6cf603096943fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:8fcefbc6900276beaf7355e091c097ef57d2016e710fd202d325caeaae76d0a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109317051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64d2ba5ee25d4a070b1d24ef9e9ff239efce9a68854eef75e6bad1bd14d115`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:53:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:53:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:53:40 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:53:53 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:53:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:54:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:54:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:54:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:54:02 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 22 Apr 2022 02:54:02 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 22 Apr 2022 02:54:02 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 22 Apr 2022 02:54:03 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 22 Apr 2022 02:54:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 22 Apr 2022 02:54:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:54:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:54:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:54:38 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:54:38 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:54:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:54:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:54:38 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:54:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2b6021c87a182e98ffd2863b419bb79abb17cbe79278678bd9fe625af2fdf0`  
		Last Modified: Fri, 22 Apr 2022 02:58:25 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765f601f0e14bf00b76a7c869dda18bb82726fb91ec363e01da58c1c7b443a3c`  
		Last Modified: Fri, 22 Apr 2022 02:58:25 GMT  
		Size: 4.8 MB (4813346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01afffc2780257e621ca877a11e714b4a7c5c410f53d54498085dc40d6bfbc5`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 3.6 MB (3553293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da9b715df5cce68601eb2b10a167f2a0fce8580873de81baa04625b3630777`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a2f060b97f61c909fac29a13ed6566d3582398b8aad97229e9cc5e8ff1b932`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 1.6 MB (1583545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd15d91ff5e8df79d2baef2f494b7a3630ab71ff3873ffa33312779f13c2221`  
		Last Modified: Fri, 22 Apr 2022 02:58:22 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbe407eaad30abd7fa7ea03f254a904ee2124fc3f320b3847677be56343ffb4`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866119df23a1053b37cbcf551ce1817f59f56a5201e1cefe3af83ac98b4fccfd`  
		Last Modified: Fri, 22 Apr 2022 02:58:31 GMT  
		Size: 72.6 MB (72639071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565937cba773bda59caa0bfc5797250dedf1cbf2794053575300e6c8a306ffd`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d560a16832325d66ddca5bcd9b1e7d6026434f572a5965d8f6ff235e17bcdc`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6b018aab576555b6e0bfd1b1b382e6ef1eed43e7c6956456e42bf5acf235c`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:546b977009454a50bc9dc149d895cf457dc65253886126003557842600a94f94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104252302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b64ffbfe4bd5c1b10bb759c1c9cac10c268df9f686896a006938b925e71756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:41:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:41:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:41:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:41:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:41:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:41:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:41:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:41:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:41:48 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 05 Apr 2022 23:41:49 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 05 Apr 2022 23:41:50 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Tue, 05 Apr 2022 23:41:51 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Tue, 05 Apr 2022 23:41:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Tue, 05 Apr 2022 23:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:42:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:42:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:42:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:42:25 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:42:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:42:27 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:42:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72673586b2e69189d31d7da8831b3a811dae1a1ecf1bc1e5844d9f4c75af37cc`  
		Last Modified: Tue, 05 Apr 2022 23:47:17 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275422ea68e1d2f852327ff381450bd62f47ab091a0645332b5ec908f0cb66ee`  
		Last Modified: Tue, 05 Apr 2022 23:47:17 GMT  
		Size: 4.3 MB (4261685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303f7eca3da11200bb9abde989691a0f85cefc51d1b995ab015b45f563cade69`  
		Last Modified: Tue, 05 Apr 2022 23:47:15 GMT  
		Size: 3.2 MB (3207435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3a0ed661f5d8f239fc1bed4d64a8b28af95b97d7627e10f08712389f413135`  
		Last Modified: Tue, 05 Apr 2022 23:47:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f835bac1300fb3863c8091cf677615a65e42ec8c766a04fd5719f2c0e49b63`  
		Last Modified: Tue, 05 Apr 2022 23:47:15 GMT  
		Size: 1.5 MB (1529423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c184d12bc00f2e6c39ffc54b5c013905f06bd80732598a23b80fdd3f94471675`  
		Last Modified: Tue, 05 Apr 2022 23:47:14 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df06d473beaea5845e2e7b690bfe6ae9b78d26b725c0d74f85587f828ebe355`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7f9da975473372f908245afcdedf6367c48d73698f886c0623f29ca125556d`  
		Last Modified: Tue, 05 Apr 2022 23:47:25 GMT  
		Size: 71.5 MB (71505064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafc96aa8516309148366b94e9bcea4c302eb300d786bdfa39948772af5b25b0`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61b702c80a7ed5a00097489bd53c188fa4e3b7c69b9ba38cf5db291186ae7a`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b7ffd8e8253f70b7b64673d2782527ccfc80ee88ed9c6cd88b64a2642a8a0f`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3587fde3c0aa9b3dac2c3990a86643cdfa251aa27ff25cd4fa8328ade5119766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117716558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ac32718efa243370fa6d5ef1143a98a46c7a98b7d7a2ce0c09882f93ceedee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 06:17:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 06:18:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 06:18:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 06:19:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 06:20:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 06:20:43 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 06:20:48 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 06:20:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:21:01 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 06:21:06 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 06:21:10 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 06:21:13 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 06:21:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Wed, 06 Apr 2022 06:21:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:24:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:24:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:24:15 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:24:17 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:24:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:24:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:24:43 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:24:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d968d42b27be6d6074d9fee26ae876b81083d349d3a234e5b7d34e9aa7a9f43`  
		Last Modified: Wed, 06 Apr 2022 06:31:07 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa12bb0b1ac1e7c5b832fcdcdce6c82815fc6fd9837eadecde3df079420f9c0`  
		Last Modified: Wed, 06 Apr 2022 06:31:08 GMT  
		Size: 5.6 MB (5630587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f497e314dca94ec4adfc49662ed8a9450786c77df7b214777e97dcc04f707d97`  
		Last Modified: Wed, 06 Apr 2022 06:31:06 GMT  
		Size: 3.5 MB (3533860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8a3ddb200d1c6cdc1f4927597217a0c0eff2e6eda4b90b2cd3c37b650292d1`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da27643720d53331c21f455c0c546f2406253b18b6760e75998938373252ac4b`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 1.9 MB (1937031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218972a2b7fff3f4edc7a4a01bf4097fd9425c342c1464255f9bf3d851dc79bd`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e638e8a579aa2089f5c76a5ac331880edec9eb62f25731171b8c4a8bf194e5d`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83ce6f7a9a6532bb7566e59118ab9a7c79d05c5b03e29867a2b15c849e65dfb`  
		Last Modified: Wed, 06 Apr 2022 06:31:16 GMT  
		Size: 76.2 MB (76158737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4f9bfe631debda3a92150a70264e0235eebeba2a02ad4bbbe14db2191f6e78`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e69df42851fd7cd877733700fe29c2e69a4a2838759d4e08ad7fcac7df60807`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 6.8 KB (6770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5760c1307ee70f75dc4492a6d87f94af862d9224d6d850dd1114d67fc2418d`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:8e3fc000ca8e9a0f928803c4fe97ae440c370c007e0faf2b8b6cf603096943fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:8fcefbc6900276beaf7355e091c097ef57d2016e710fd202d325caeaae76d0a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109317051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64d2ba5ee25d4a070b1d24ef9e9ff239efce9a68854eef75e6bad1bd14d115`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:53:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:53:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:53:40 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:53:53 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:53:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:54:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:54:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:54:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:54:02 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 22 Apr 2022 02:54:02 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 22 Apr 2022 02:54:02 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 22 Apr 2022 02:54:03 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 22 Apr 2022 02:54:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 22 Apr 2022 02:54:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:54:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:54:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:54:38 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:54:38 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:54:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:54:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:54:38 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:54:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2b6021c87a182e98ffd2863b419bb79abb17cbe79278678bd9fe625af2fdf0`  
		Last Modified: Fri, 22 Apr 2022 02:58:25 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765f601f0e14bf00b76a7c869dda18bb82726fb91ec363e01da58c1c7b443a3c`  
		Last Modified: Fri, 22 Apr 2022 02:58:25 GMT  
		Size: 4.8 MB (4813346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01afffc2780257e621ca877a11e714b4a7c5c410f53d54498085dc40d6bfbc5`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 3.6 MB (3553293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da9b715df5cce68601eb2b10a167f2a0fce8580873de81baa04625b3630777`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a2f060b97f61c909fac29a13ed6566d3582398b8aad97229e9cc5e8ff1b932`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 1.6 MB (1583545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd15d91ff5e8df79d2baef2f494b7a3630ab71ff3873ffa33312779f13c2221`  
		Last Modified: Fri, 22 Apr 2022 02:58:22 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbe407eaad30abd7fa7ea03f254a904ee2124fc3f320b3847677be56343ffb4`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866119df23a1053b37cbcf551ce1817f59f56a5201e1cefe3af83ac98b4fccfd`  
		Last Modified: Fri, 22 Apr 2022 02:58:31 GMT  
		Size: 72.6 MB (72639071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565937cba773bda59caa0bfc5797250dedf1cbf2794053575300e6c8a306ffd`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d560a16832325d66ddca5bcd9b1e7d6026434f572a5965d8f6ff235e17bcdc`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6b018aab576555b6e0bfd1b1b382e6ef1eed43e7c6956456e42bf5acf235c`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:546b977009454a50bc9dc149d895cf457dc65253886126003557842600a94f94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104252302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b64ffbfe4bd5c1b10bb759c1c9cac10c268df9f686896a006938b925e71756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:41:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:41:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:41:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:41:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:41:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:41:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:41:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:41:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:41:48 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 05 Apr 2022 23:41:49 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 05 Apr 2022 23:41:50 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Tue, 05 Apr 2022 23:41:51 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Tue, 05 Apr 2022 23:41:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Tue, 05 Apr 2022 23:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:42:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:42:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:42:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:42:25 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:42:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:42:27 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:42:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72673586b2e69189d31d7da8831b3a811dae1a1ecf1bc1e5844d9f4c75af37cc`  
		Last Modified: Tue, 05 Apr 2022 23:47:17 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275422ea68e1d2f852327ff381450bd62f47ab091a0645332b5ec908f0cb66ee`  
		Last Modified: Tue, 05 Apr 2022 23:47:17 GMT  
		Size: 4.3 MB (4261685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303f7eca3da11200bb9abde989691a0f85cefc51d1b995ab015b45f563cade69`  
		Last Modified: Tue, 05 Apr 2022 23:47:15 GMT  
		Size: 3.2 MB (3207435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3a0ed661f5d8f239fc1bed4d64a8b28af95b97d7627e10f08712389f413135`  
		Last Modified: Tue, 05 Apr 2022 23:47:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f835bac1300fb3863c8091cf677615a65e42ec8c766a04fd5719f2c0e49b63`  
		Last Modified: Tue, 05 Apr 2022 23:47:15 GMT  
		Size: 1.5 MB (1529423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c184d12bc00f2e6c39ffc54b5c013905f06bd80732598a23b80fdd3f94471675`  
		Last Modified: Tue, 05 Apr 2022 23:47:14 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df06d473beaea5845e2e7b690bfe6ae9b78d26b725c0d74f85587f828ebe355`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7f9da975473372f908245afcdedf6367c48d73698f886c0623f29ca125556d`  
		Last Modified: Tue, 05 Apr 2022 23:47:25 GMT  
		Size: 71.5 MB (71505064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafc96aa8516309148366b94e9bcea4c302eb300d786bdfa39948772af5b25b0`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61b702c80a7ed5a00097489bd53c188fa4e3b7c69b9ba38cf5db291186ae7a`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b7ffd8e8253f70b7b64673d2782527ccfc80ee88ed9c6cd88b64a2642a8a0f`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3587fde3c0aa9b3dac2c3990a86643cdfa251aa27ff25cd4fa8328ade5119766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117716558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ac32718efa243370fa6d5ef1143a98a46c7a98b7d7a2ce0c09882f93ceedee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 06:17:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 06:18:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 06:18:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 06:19:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 06:20:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 06:20:43 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 06:20:48 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 06:20:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:21:01 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 06:21:06 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 06:21:10 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 06:21:13 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 06:21:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Wed, 06 Apr 2022 06:21:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:24:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:24:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:24:15 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:24:17 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:24:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:24:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:24:43 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:24:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d968d42b27be6d6074d9fee26ae876b81083d349d3a234e5b7d34e9aa7a9f43`  
		Last Modified: Wed, 06 Apr 2022 06:31:07 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa12bb0b1ac1e7c5b832fcdcdce6c82815fc6fd9837eadecde3df079420f9c0`  
		Last Modified: Wed, 06 Apr 2022 06:31:08 GMT  
		Size: 5.6 MB (5630587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f497e314dca94ec4adfc49662ed8a9450786c77df7b214777e97dcc04f707d97`  
		Last Modified: Wed, 06 Apr 2022 06:31:06 GMT  
		Size: 3.5 MB (3533860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8a3ddb200d1c6cdc1f4927597217a0c0eff2e6eda4b90b2cd3c37b650292d1`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da27643720d53331c21f455c0c546f2406253b18b6760e75998938373252ac4b`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 1.9 MB (1937031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218972a2b7fff3f4edc7a4a01bf4097fd9425c342c1464255f9bf3d851dc79bd`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e638e8a579aa2089f5c76a5ac331880edec9eb62f25731171b8c4a8bf194e5d`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83ce6f7a9a6532bb7566e59118ab9a7c79d05c5b03e29867a2b15c849e65dfb`  
		Last Modified: Wed, 06 Apr 2022 06:31:16 GMT  
		Size: 76.2 MB (76158737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4f9bfe631debda3a92150a70264e0235eebeba2a02ad4bbbe14db2191f6e78`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e69df42851fd7cd877733700fe29c2e69a4a2838759d4e08ad7fcac7df60807`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 6.8 KB (6770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5760c1307ee70f75dc4492a6d87f94af862d9224d6d850dd1114d67fc2418d`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.43`

```console
$ docker pull mariadb@sha256:8e3fc000ca8e9a0f928803c4fe97ae440c370c007e0faf2b8b6cf603096943fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.43` - linux; amd64

```console
$ docker pull mariadb@sha256:8fcefbc6900276beaf7355e091c097ef57d2016e710fd202d325caeaae76d0a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109317051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64d2ba5ee25d4a070b1d24ef9e9ff239efce9a68854eef75e6bad1bd14d115`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:53:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:53:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:53:40 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:53:53 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:53:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:54:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:54:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:54:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:54:02 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 22 Apr 2022 02:54:02 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 22 Apr 2022 02:54:02 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 22 Apr 2022 02:54:03 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 22 Apr 2022 02:54:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 22 Apr 2022 02:54:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:54:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:54:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:54:38 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:54:38 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:54:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:54:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:54:38 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:54:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2b6021c87a182e98ffd2863b419bb79abb17cbe79278678bd9fe625af2fdf0`  
		Last Modified: Fri, 22 Apr 2022 02:58:25 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765f601f0e14bf00b76a7c869dda18bb82726fb91ec363e01da58c1c7b443a3c`  
		Last Modified: Fri, 22 Apr 2022 02:58:25 GMT  
		Size: 4.8 MB (4813346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01afffc2780257e621ca877a11e714b4a7c5c410f53d54498085dc40d6bfbc5`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 3.6 MB (3553293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da9b715df5cce68601eb2b10a167f2a0fce8580873de81baa04625b3630777`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a2f060b97f61c909fac29a13ed6566d3582398b8aad97229e9cc5e8ff1b932`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 1.6 MB (1583545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd15d91ff5e8df79d2baef2f494b7a3630ab71ff3873ffa33312779f13c2221`  
		Last Modified: Fri, 22 Apr 2022 02:58:22 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbe407eaad30abd7fa7ea03f254a904ee2124fc3f320b3847677be56343ffb4`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866119df23a1053b37cbcf551ce1817f59f56a5201e1cefe3af83ac98b4fccfd`  
		Last Modified: Fri, 22 Apr 2022 02:58:31 GMT  
		Size: 72.6 MB (72639071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565937cba773bda59caa0bfc5797250dedf1cbf2794053575300e6c8a306ffd`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d560a16832325d66ddca5bcd9b1e7d6026434f572a5965d8f6ff235e17bcdc`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6b018aab576555b6e0bfd1b1b382e6ef1eed43e7c6956456e42bf5acf235c`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:546b977009454a50bc9dc149d895cf457dc65253886126003557842600a94f94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104252302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b64ffbfe4bd5c1b10bb759c1c9cac10c268df9f686896a006938b925e71756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:41:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:41:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:41:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:41:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:41:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:41:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:41:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:41:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:41:48 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 05 Apr 2022 23:41:49 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 05 Apr 2022 23:41:50 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Tue, 05 Apr 2022 23:41:51 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Tue, 05 Apr 2022 23:41:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Tue, 05 Apr 2022 23:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:42:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:42:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:42:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:42:25 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:42:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:42:27 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:42:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72673586b2e69189d31d7da8831b3a811dae1a1ecf1bc1e5844d9f4c75af37cc`  
		Last Modified: Tue, 05 Apr 2022 23:47:17 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275422ea68e1d2f852327ff381450bd62f47ab091a0645332b5ec908f0cb66ee`  
		Last Modified: Tue, 05 Apr 2022 23:47:17 GMT  
		Size: 4.3 MB (4261685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303f7eca3da11200bb9abde989691a0f85cefc51d1b995ab015b45f563cade69`  
		Last Modified: Tue, 05 Apr 2022 23:47:15 GMT  
		Size: 3.2 MB (3207435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3a0ed661f5d8f239fc1bed4d64a8b28af95b97d7627e10f08712389f413135`  
		Last Modified: Tue, 05 Apr 2022 23:47:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f835bac1300fb3863c8091cf677615a65e42ec8c766a04fd5719f2c0e49b63`  
		Last Modified: Tue, 05 Apr 2022 23:47:15 GMT  
		Size: 1.5 MB (1529423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c184d12bc00f2e6c39ffc54b5c013905f06bd80732598a23b80fdd3f94471675`  
		Last Modified: Tue, 05 Apr 2022 23:47:14 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df06d473beaea5845e2e7b690bfe6ae9b78d26b725c0d74f85587f828ebe355`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7f9da975473372f908245afcdedf6367c48d73698f886c0623f29ca125556d`  
		Last Modified: Tue, 05 Apr 2022 23:47:25 GMT  
		Size: 71.5 MB (71505064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafc96aa8516309148366b94e9bcea4c302eb300d786bdfa39948772af5b25b0`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61b702c80a7ed5a00097489bd53c188fa4e3b7c69b9ba38cf5db291186ae7a`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b7ffd8e8253f70b7b64673d2782527ccfc80ee88ed9c6cd88b64a2642a8a0f`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3587fde3c0aa9b3dac2c3990a86643cdfa251aa27ff25cd4fa8328ade5119766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117716558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ac32718efa243370fa6d5ef1143a98a46c7a98b7d7a2ce0c09882f93ceedee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 06:17:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 06:18:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 06:18:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 06:19:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 06:20:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 06:20:43 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 06:20:48 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 06:20:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:21:01 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 06:21:06 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 06:21:10 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 06:21:13 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 06:21:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Wed, 06 Apr 2022 06:21:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:24:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:24:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:24:15 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:24:17 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:24:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:24:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:24:43 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:24:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d968d42b27be6d6074d9fee26ae876b81083d349d3a234e5b7d34e9aa7a9f43`  
		Last Modified: Wed, 06 Apr 2022 06:31:07 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa12bb0b1ac1e7c5b832fcdcdce6c82815fc6fd9837eadecde3df079420f9c0`  
		Last Modified: Wed, 06 Apr 2022 06:31:08 GMT  
		Size: 5.6 MB (5630587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f497e314dca94ec4adfc49662ed8a9450786c77df7b214777e97dcc04f707d97`  
		Last Modified: Wed, 06 Apr 2022 06:31:06 GMT  
		Size: 3.5 MB (3533860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8a3ddb200d1c6cdc1f4927597217a0c0eff2e6eda4b90b2cd3c37b650292d1`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da27643720d53331c21f455c0c546f2406253b18b6760e75998938373252ac4b`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 1.9 MB (1937031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218972a2b7fff3f4edc7a4a01bf4097fd9425c342c1464255f9bf3d851dc79bd`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e638e8a579aa2089f5c76a5ac331880edec9eb62f25731171b8c4a8bf194e5d`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83ce6f7a9a6532bb7566e59118ab9a7c79d05c5b03e29867a2b15c849e65dfb`  
		Last Modified: Wed, 06 Apr 2022 06:31:16 GMT  
		Size: 76.2 MB (76158737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4f9bfe631debda3a92150a70264e0235eebeba2a02ad4bbbe14db2191f6e78`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e69df42851fd7cd877733700fe29c2e69a4a2838759d4e08ad7fcac7df60807`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 6.8 KB (6770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5760c1307ee70f75dc4492a6d87f94af862d9224d6d850dd1114d67fc2418d`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.43-bionic`

```console
$ docker pull mariadb@sha256:8e3fc000ca8e9a0f928803c4fe97ae440c370c007e0faf2b8b6cf603096943fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.43-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:8fcefbc6900276beaf7355e091c097ef57d2016e710fd202d325caeaae76d0a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109317051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64d2ba5ee25d4a070b1d24ef9e9ff239efce9a68854eef75e6bad1bd14d115`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:53:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:53:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:53:40 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:53:53 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:53:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:54:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:54:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:54:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:54:02 GMT
ARG MARIADB_MAJOR=10.2
# Fri, 22 Apr 2022 02:54:02 GMT
ENV MARIADB_MAJOR=10.2
# Fri, 22 Apr 2022 02:54:02 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 22 Apr 2022 02:54:03 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 22 Apr 2022 02:54:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 22 Apr 2022 02:54:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:54:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:54:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:54:38 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:54:38 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:54:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:54:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:54:38 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:54:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2b6021c87a182e98ffd2863b419bb79abb17cbe79278678bd9fe625af2fdf0`  
		Last Modified: Fri, 22 Apr 2022 02:58:25 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765f601f0e14bf00b76a7c869dda18bb82726fb91ec363e01da58c1c7b443a3c`  
		Last Modified: Fri, 22 Apr 2022 02:58:25 GMT  
		Size: 4.8 MB (4813346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01afffc2780257e621ca877a11e714b4a7c5c410f53d54498085dc40d6bfbc5`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 3.6 MB (3553293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da9b715df5cce68601eb2b10a167f2a0fce8580873de81baa04625b3630777`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a2f060b97f61c909fac29a13ed6566d3582398b8aad97229e9cc5e8ff1b932`  
		Last Modified: Fri, 22 Apr 2022 02:58:23 GMT  
		Size: 1.6 MB (1583545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd15d91ff5e8df79d2baef2f494b7a3630ab71ff3873ffa33312779f13c2221`  
		Last Modified: Fri, 22 Apr 2022 02:58:22 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbe407eaad30abd7fa7ea03f254a904ee2124fc3f320b3847677be56343ffb4`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866119df23a1053b37cbcf551ce1817f59f56a5201e1cefe3af83ac98b4fccfd`  
		Last Modified: Fri, 22 Apr 2022 02:58:31 GMT  
		Size: 72.6 MB (72639071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565937cba773bda59caa0bfc5797250dedf1cbf2794053575300e6c8a306ffd`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d560a16832325d66ddca5bcd9b1e7d6026434f572a5965d8f6ff235e17bcdc`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6b018aab576555b6e0bfd1b1b382e6ef1eed43e7c6956456e42bf5acf235c`  
		Last Modified: Fri, 22 Apr 2022 02:58:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:546b977009454a50bc9dc149d895cf457dc65253886126003557842600a94f94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104252302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b64ffbfe4bd5c1b10bb759c1c9cac10c268df9f686896a006938b925e71756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:41:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:41:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:41:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:41:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:41:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:41:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:41:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:41:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:41:48 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 05 Apr 2022 23:41:49 GMT
ENV MARIADB_MAJOR=10.2
# Tue, 05 Apr 2022 23:41:50 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Tue, 05 Apr 2022 23:41:51 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Tue, 05 Apr 2022 23:41:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Tue, 05 Apr 2022 23:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:42:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:42:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:42:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:42:25 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:42:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:42:27 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:42:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72673586b2e69189d31d7da8831b3a811dae1a1ecf1bc1e5844d9f4c75af37cc`  
		Last Modified: Tue, 05 Apr 2022 23:47:17 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275422ea68e1d2f852327ff381450bd62f47ab091a0645332b5ec908f0cb66ee`  
		Last Modified: Tue, 05 Apr 2022 23:47:17 GMT  
		Size: 4.3 MB (4261685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303f7eca3da11200bb9abde989691a0f85cefc51d1b995ab015b45f563cade69`  
		Last Modified: Tue, 05 Apr 2022 23:47:15 GMT  
		Size: 3.2 MB (3207435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3a0ed661f5d8f239fc1bed4d64a8b28af95b97d7627e10f08712389f413135`  
		Last Modified: Tue, 05 Apr 2022 23:47:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f835bac1300fb3863c8091cf677615a65e42ec8c766a04fd5719f2c0e49b63`  
		Last Modified: Tue, 05 Apr 2022 23:47:15 GMT  
		Size: 1.5 MB (1529423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c184d12bc00f2e6c39ffc54b5c013905f06bd80732598a23b80fdd3f94471675`  
		Last Modified: Tue, 05 Apr 2022 23:47:14 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df06d473beaea5845e2e7b690bfe6ae9b78d26b725c0d74f85587f828ebe355`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7f9da975473372f908245afcdedf6367c48d73698f886c0623f29ca125556d`  
		Last Modified: Tue, 05 Apr 2022 23:47:25 GMT  
		Size: 71.5 MB (71505064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafc96aa8516309148366b94e9bcea4c302eb300d786bdfa39948772af5b25b0`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61b702c80a7ed5a00097489bd53c188fa4e3b7c69b9ba38cf5db291186ae7a`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b7ffd8e8253f70b7b64673d2782527ccfc80ee88ed9c6cd88b64a2642a8a0f`  
		Last Modified: Tue, 05 Apr 2022 23:47:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3587fde3c0aa9b3dac2c3990a86643cdfa251aa27ff25cd4fa8328ade5119766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117716558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ac32718efa243370fa6d5ef1143a98a46c7a98b7d7a2ce0c09882f93ceedee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 06:17:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 06:18:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 06:18:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 06:19:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 06:20:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 06:20:43 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 06:20:48 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 06:20:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:21:01 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 06:21:06 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 06:21:10 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 06:21:13 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 06:21:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Wed, 06 Apr 2022 06:21:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:24:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:24:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:24:15 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:24:17 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:24:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:24:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:24:43 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:24:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d968d42b27be6d6074d9fee26ae876b81083d349d3a234e5b7d34e9aa7a9f43`  
		Last Modified: Wed, 06 Apr 2022 06:31:07 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa12bb0b1ac1e7c5b832fcdcdce6c82815fc6fd9837eadecde3df079420f9c0`  
		Last Modified: Wed, 06 Apr 2022 06:31:08 GMT  
		Size: 5.6 MB (5630587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f497e314dca94ec4adfc49662ed8a9450786c77df7b214777e97dcc04f707d97`  
		Last Modified: Wed, 06 Apr 2022 06:31:06 GMT  
		Size: 3.5 MB (3533860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8a3ddb200d1c6cdc1f4927597217a0c0eff2e6eda4b90b2cd3c37b650292d1`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da27643720d53331c21f455c0c546f2406253b18b6760e75998938373252ac4b`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 1.9 MB (1937031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218972a2b7fff3f4edc7a4a01bf4097fd9425c342c1464255f9bf3d851dc79bd`  
		Last Modified: Wed, 06 Apr 2022 06:31:04 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e638e8a579aa2089f5c76a5ac331880edec9eb62f25731171b8c4a8bf194e5d`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83ce6f7a9a6532bb7566e59118ab9a7c79d05c5b03e29867a2b15c849e65dfb`  
		Last Modified: Wed, 06 Apr 2022 06:31:16 GMT  
		Size: 76.2 MB (76158737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4f9bfe631debda3a92150a70264e0235eebeba2a02ad4bbbe14db2191f6e78`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e69df42851fd7cd877733700fe29c2e69a4a2838759d4e08ad7fcac7df60807`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 6.8 KB (6770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5760c1307ee70f75dc4492a6d87f94af862d9224d6d850dd1114d67fc2418d`  
		Last Modified: Wed, 06 Apr 2022 06:31:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:ae9a2225499abc822206d842e5b3d7ccec2db184e4294e1622a73138a2391c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:3fadf7ebd60b5b879e6f9e2cd46c782e18c64ec78a5e1ddd5e587a779364933d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82643bd90d5e12d8dcc3923c5037bace1b14063504a971ec0498cf5e162bf61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:58 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 22 Apr 2022 02:52:58 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 22 Apr 2022 02:52:59 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 22 Apr 2022 02:52:59 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 22 Apr 2022 02:52:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:53:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:53:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:53:26 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:53:26 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:53:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:53:27 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:53:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7801d5a27d87a0a14725087a02be10adf3637adbacf9636d809795ed70a34ce`  
		Last Modified: Fri, 22 Apr 2022 02:57:52 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7f812281a340552e5374feef34fd9a2563c703d0193aad89c90cf3fe9fe39a`  
		Last Modified: Fri, 22 Apr 2022 02:58:04 GMT  
		Size: 80.2 MB (80191115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0502732e9ee8013217b08ed97cb6199c16b413212459861470162d7a1ea6d`  
		Last Modified: Fri, 22 Apr 2022 02:57:53 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fba0e3193601cd73bca932f9f778413d041e214ebad8a4a0b24f5ce35ec76d`  
		Last Modified: Fri, 22 Apr 2022 02:57:53 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c2c705d6abdc6c36ec9ad28a43a47c9d00d5c2aa196ceee150b34001faaad4`  
		Last Modified: Fri, 22 Apr 2022 02:57:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9122b5d2089a0bef50bd4b4b052de3f767ae02fe103a7f045424bb435327b99c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117606696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9240618029d5e5294d8495ef3d5e12c5bfbbe5e87620139a973baf3b8b38882f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:40:14 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 05 Apr 2022 23:40:15 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 05 Apr 2022 23:40:16 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Tue, 05 Apr 2022 23:40:17 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Tue, 05 Apr 2022 23:40:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:40:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:40:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:40:50 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:40:52 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:40:53 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:40:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:40:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b2722ae7be0ff0cf5eded6aadd56fac0762dd62d9d70fa6adcb8f6d1e49886`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f374683eff0d6a466efc5d34ad429c5036c1844745b7fb5e671acc5c99ffb657`  
		Last Modified: Tue, 05 Apr 2022 23:46:54 GMT  
		Size: 79.5 MB (79530552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f750002a3ec30e22bb20d3239f5fe4fee21e210162ead7e9033696de7dc005`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298341c922e7c6401822293c8117d39f6b522eec9328ad5d99984664597e2fb2`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112a0544dadb51700b587a9eeec1edf0a08ac1b1b1ca7df6fcecd28e29699376`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6557494848c9dc8724c5ac32d3f3fa295fcce12dda0371364715562cd081f7b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131006838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd14ec4762789d1971a8b1ad3cb9d03bdc82b483ee1d4c5c66b9605120fcd1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:13:10 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 06:13:12 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 06:13:16 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 06:13:19 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 06:13:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:13:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:16:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:16:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:16:35 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:16:37 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:16:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:17:00 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:17:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993be47f4edb53a4bc9224b3a08c0670a728c46bb73adc5dffb32eeff91025c4`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e41a173aef92355df92077dca5ab59768b4c200b980900cfc69a48e20196ddd`  
		Last Modified: Wed, 06 Apr 2022 06:30:39 GMT  
		Size: 84.8 MB (84792026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b283ee9b1b9f13c52c92a03aac531e73351ef2696316eef2698abba85917415`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa01cd80c432a54874d465e696da5343cdf4ed623406e7c541306c7fcbee1f7e`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c46a28fa5b9a7e0483f87a59c125d4a7bdc210f72772bb04c8a775be7fae816`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:ae9a2225499abc822206d842e5b3d7ccec2db184e4294e1622a73138a2391c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:3fadf7ebd60b5b879e6f9e2cd46c782e18c64ec78a5e1ddd5e587a779364933d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82643bd90d5e12d8dcc3923c5037bace1b14063504a971ec0498cf5e162bf61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:58 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 22 Apr 2022 02:52:58 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 22 Apr 2022 02:52:59 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 22 Apr 2022 02:52:59 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 22 Apr 2022 02:52:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:53:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:53:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:53:26 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:53:26 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:53:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:53:27 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:53:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7801d5a27d87a0a14725087a02be10adf3637adbacf9636d809795ed70a34ce`  
		Last Modified: Fri, 22 Apr 2022 02:57:52 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7f812281a340552e5374feef34fd9a2563c703d0193aad89c90cf3fe9fe39a`  
		Last Modified: Fri, 22 Apr 2022 02:58:04 GMT  
		Size: 80.2 MB (80191115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0502732e9ee8013217b08ed97cb6199c16b413212459861470162d7a1ea6d`  
		Last Modified: Fri, 22 Apr 2022 02:57:53 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fba0e3193601cd73bca932f9f778413d041e214ebad8a4a0b24f5ce35ec76d`  
		Last Modified: Fri, 22 Apr 2022 02:57:53 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c2c705d6abdc6c36ec9ad28a43a47c9d00d5c2aa196ceee150b34001faaad4`  
		Last Modified: Fri, 22 Apr 2022 02:57:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9122b5d2089a0bef50bd4b4b052de3f767ae02fe103a7f045424bb435327b99c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117606696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9240618029d5e5294d8495ef3d5e12c5bfbbe5e87620139a973baf3b8b38882f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:40:14 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 05 Apr 2022 23:40:15 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 05 Apr 2022 23:40:16 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Tue, 05 Apr 2022 23:40:17 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Tue, 05 Apr 2022 23:40:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:40:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:40:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:40:50 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:40:52 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:40:53 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:40:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:40:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b2722ae7be0ff0cf5eded6aadd56fac0762dd62d9d70fa6adcb8f6d1e49886`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f374683eff0d6a466efc5d34ad429c5036c1844745b7fb5e671acc5c99ffb657`  
		Last Modified: Tue, 05 Apr 2022 23:46:54 GMT  
		Size: 79.5 MB (79530552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f750002a3ec30e22bb20d3239f5fe4fee21e210162ead7e9033696de7dc005`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298341c922e7c6401822293c8117d39f6b522eec9328ad5d99984664597e2fb2`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112a0544dadb51700b587a9eeec1edf0a08ac1b1b1ca7df6fcecd28e29699376`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6557494848c9dc8724c5ac32d3f3fa295fcce12dda0371364715562cd081f7b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131006838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd14ec4762789d1971a8b1ad3cb9d03bdc82b483ee1d4c5c66b9605120fcd1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:13:10 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 06:13:12 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 06:13:16 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 06:13:19 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 06:13:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:13:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:16:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:16:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:16:35 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:16:37 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:16:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:17:00 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:17:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993be47f4edb53a4bc9224b3a08c0670a728c46bb73adc5dffb32eeff91025c4`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e41a173aef92355df92077dca5ab59768b4c200b980900cfc69a48e20196ddd`  
		Last Modified: Wed, 06 Apr 2022 06:30:39 GMT  
		Size: 84.8 MB (84792026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b283ee9b1b9f13c52c92a03aac531e73351ef2696316eef2698abba85917415`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa01cd80c432a54874d465e696da5343cdf4ed623406e7c541306c7fcbee1f7e`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c46a28fa5b9a7e0483f87a59c125d4a7bdc210f72772bb04c8a775be7fae816`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.34`

```console
$ docker pull mariadb@sha256:ae9a2225499abc822206d842e5b3d7ccec2db184e4294e1622a73138a2391c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.34` - linux; amd64

```console
$ docker pull mariadb@sha256:3fadf7ebd60b5b879e6f9e2cd46c782e18c64ec78a5e1ddd5e587a779364933d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82643bd90d5e12d8dcc3923c5037bace1b14063504a971ec0498cf5e162bf61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:58 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 22 Apr 2022 02:52:58 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 22 Apr 2022 02:52:59 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 22 Apr 2022 02:52:59 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 22 Apr 2022 02:52:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:53:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:53:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:53:26 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:53:26 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:53:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:53:27 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:53:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7801d5a27d87a0a14725087a02be10adf3637adbacf9636d809795ed70a34ce`  
		Last Modified: Fri, 22 Apr 2022 02:57:52 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7f812281a340552e5374feef34fd9a2563c703d0193aad89c90cf3fe9fe39a`  
		Last Modified: Fri, 22 Apr 2022 02:58:04 GMT  
		Size: 80.2 MB (80191115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0502732e9ee8013217b08ed97cb6199c16b413212459861470162d7a1ea6d`  
		Last Modified: Fri, 22 Apr 2022 02:57:53 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fba0e3193601cd73bca932f9f778413d041e214ebad8a4a0b24f5ce35ec76d`  
		Last Modified: Fri, 22 Apr 2022 02:57:53 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c2c705d6abdc6c36ec9ad28a43a47c9d00d5c2aa196ceee150b34001faaad4`  
		Last Modified: Fri, 22 Apr 2022 02:57:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9122b5d2089a0bef50bd4b4b052de3f767ae02fe103a7f045424bb435327b99c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117606696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9240618029d5e5294d8495ef3d5e12c5bfbbe5e87620139a973baf3b8b38882f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:40:14 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 05 Apr 2022 23:40:15 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 05 Apr 2022 23:40:16 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Tue, 05 Apr 2022 23:40:17 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Tue, 05 Apr 2022 23:40:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:40:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:40:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:40:50 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:40:52 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:40:53 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:40:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:40:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b2722ae7be0ff0cf5eded6aadd56fac0762dd62d9d70fa6adcb8f6d1e49886`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f374683eff0d6a466efc5d34ad429c5036c1844745b7fb5e671acc5c99ffb657`  
		Last Modified: Tue, 05 Apr 2022 23:46:54 GMT  
		Size: 79.5 MB (79530552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f750002a3ec30e22bb20d3239f5fe4fee21e210162ead7e9033696de7dc005`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298341c922e7c6401822293c8117d39f6b522eec9328ad5d99984664597e2fb2`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112a0544dadb51700b587a9eeec1edf0a08ac1b1b1ca7df6fcecd28e29699376`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6557494848c9dc8724c5ac32d3f3fa295fcce12dda0371364715562cd081f7b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131006838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd14ec4762789d1971a8b1ad3cb9d03bdc82b483ee1d4c5c66b9605120fcd1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:13:10 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 06:13:12 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 06:13:16 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 06:13:19 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 06:13:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:13:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:16:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:16:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:16:35 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:16:37 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:16:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:17:00 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:17:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993be47f4edb53a4bc9224b3a08c0670a728c46bb73adc5dffb32eeff91025c4`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e41a173aef92355df92077dca5ab59768b4c200b980900cfc69a48e20196ddd`  
		Last Modified: Wed, 06 Apr 2022 06:30:39 GMT  
		Size: 84.8 MB (84792026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b283ee9b1b9f13c52c92a03aac531e73351ef2696316eef2698abba85917415`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa01cd80c432a54874d465e696da5343cdf4ed623406e7c541306c7fcbee1f7e`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c46a28fa5b9a7e0483f87a59c125d4a7bdc210f72772bb04c8a775be7fae816`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.34-focal`

```console
$ docker pull mariadb@sha256:ae9a2225499abc822206d842e5b3d7ccec2db184e4294e1622a73138a2391c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.34-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:3fadf7ebd60b5b879e6f9e2cd46c782e18c64ec78a5e1ddd5e587a779364933d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82643bd90d5e12d8dcc3923c5037bace1b14063504a971ec0498cf5e162bf61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:58 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 22 Apr 2022 02:52:58 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 22 Apr 2022 02:52:59 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 22 Apr 2022 02:52:59 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 22 Apr 2022 02:52:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:53:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:53:26 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:53:26 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:53:26 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:53:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:53:27 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:53:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7801d5a27d87a0a14725087a02be10adf3637adbacf9636d809795ed70a34ce`  
		Last Modified: Fri, 22 Apr 2022 02:57:52 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7f812281a340552e5374feef34fd9a2563c703d0193aad89c90cf3fe9fe39a`  
		Last Modified: Fri, 22 Apr 2022 02:58:04 GMT  
		Size: 80.2 MB (80191115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0502732e9ee8013217b08ed97cb6199c16b413212459861470162d7a1ea6d`  
		Last Modified: Fri, 22 Apr 2022 02:57:53 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fba0e3193601cd73bca932f9f778413d041e214ebad8a4a0b24f5ce35ec76d`  
		Last Modified: Fri, 22 Apr 2022 02:57:53 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c2c705d6abdc6c36ec9ad28a43a47c9d00d5c2aa196ceee150b34001faaad4`  
		Last Modified: Fri, 22 Apr 2022 02:57:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9122b5d2089a0bef50bd4b4b052de3f767ae02fe103a7f045424bb435327b99c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117606696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9240618029d5e5294d8495ef3d5e12c5bfbbe5e87620139a973baf3b8b38882f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:40:14 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 05 Apr 2022 23:40:15 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 05 Apr 2022 23:40:16 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Tue, 05 Apr 2022 23:40:17 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Tue, 05 Apr 2022 23:40:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:40:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:40:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:40:50 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:40:52 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:40:53 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:40:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:40:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:40:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b2722ae7be0ff0cf5eded6aadd56fac0762dd62d9d70fa6adcb8f6d1e49886`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f374683eff0d6a466efc5d34ad429c5036c1844745b7fb5e671acc5c99ffb657`  
		Last Modified: Tue, 05 Apr 2022 23:46:54 GMT  
		Size: 79.5 MB (79530552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f750002a3ec30e22bb20d3239f5fe4fee21e210162ead7e9033696de7dc005`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298341c922e7c6401822293c8117d39f6b522eec9328ad5d99984664597e2fb2`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112a0544dadb51700b587a9eeec1edf0a08ac1b1b1ca7df6fcecd28e29699376`  
		Last Modified: Tue, 05 Apr 2022 23:46:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6557494848c9dc8724c5ac32d3f3fa295fcce12dda0371364715562cd081f7b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131006838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd14ec4762789d1971a8b1ad3cb9d03bdc82b483ee1d4c5c66b9605120fcd1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:13:10 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 06:13:12 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 06:13:16 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 06:13:19 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 06:13:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:13:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:16:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:16:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:16:35 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:16:37 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:16:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:17:00 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:17:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993be47f4edb53a4bc9224b3a08c0670a728c46bb73adc5dffb32eeff91025c4`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e41a173aef92355df92077dca5ab59768b4c200b980900cfc69a48e20196ddd`  
		Last Modified: Wed, 06 Apr 2022 06:30:39 GMT  
		Size: 84.8 MB (84792026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b283ee9b1b9f13c52c92a03aac531e73351ef2696316eef2698abba85917415`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa01cd80c432a54874d465e696da5343cdf4ed623406e7c541306c7fcbee1f7e`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c46a28fa5b9a7e0483f87a59c125d4a7bdc210f72772bb04c8a775be7fae816`  
		Last Modified: Wed, 06 Apr 2022 06:30:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:d454a91588360cd4d1c37efa9293427956c242142a109507d81ca9968715a18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:819963937619a1891b4e1f4c6125d4ea4f3bb6195d72042307ae2cd68071b1ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad3c8256a516f93654aed599432527de806b5da9c2088233c692591c291a9a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:31 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 22 Apr 2022 02:52:31 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 22 Apr 2022 02:52:31 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 22 Apr 2022 02:52:31 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 22 Apr 2022 02:52:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:52:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:52:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:52:54 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:52:54 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:52:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:52:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:52:55 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:52:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b744c9184d699263c8a3ef44c0767a0429db8c6892701eef91c0237b61421e5`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d15a78b4ec63a31d0349185788c72af768e99002fcbb2a6a46c3a8a6fd263eb`  
		Last Modified: Fri, 22 Apr 2022 02:57:36 GMT  
		Size: 85.8 MB (85753125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76088cf45319c739b3d59169b2c599481218be04824f4aadb20657eb83c43f1b`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4519dcc8d4be31b8246d8f666c1db6c7eab0ff35ade6ece88c6b7f39a784d29`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 6.8 KB (6769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f902b376b26e5290db3e69f9cfadc24be1001705c68c97205619cd98b2a00d`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7b57317ff2a88ce03e890f2af9935783be428c6a7338246d2a769f2337adfd87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123002163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a800c91370dab00fef4613f7de3fd6d98bb439a35be243b2d4bead63c77e58e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:39:22 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 05 Apr 2022 23:39:23 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 05 Apr 2022 23:39:24 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Tue, 05 Apr 2022 23:39:25 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Tue, 05 Apr 2022 23:39:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:39:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:39:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:39:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:39:58 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:39:59 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:39:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:40:01 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:40:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae937f7cdd608c1e55602715591fcccd2ef458d343d49c4624e4f5548eb7cb6`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0739a94b8e362ab4dcd6ee7ccb9e1831c626697dd4399aeee2dc309cb9f55b7`  
		Last Modified: Tue, 05 Apr 2022 23:46:22 GMT  
		Size: 84.9 MB (84926018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5445c5978da64786d52c0af313da2b96045ec64d3ff111176b31a12b92ede7`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b489aa0ef89a027e08e62ed43068a4438c948fc1ffedfd7f1f922bd2ccd53f`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def5e5f2644da0b7228457a3c1b4781b12440c749482e87fce0ff9a9a326da31`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5ce596303c369e20bf1cfe515bf50072f54352805dedf84ae8d47d48d3fd6773
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136560761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0049b450ab4d30711dba89ae824e1ad6462d78839299509a3ade9063437bf75a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:09:58 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 06:10:03 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 06:10:08 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 06:10:14 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 06:10:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:10:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:12:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:12:40 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:12:41 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:12:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:12:56 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:13:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a178369021f591b4cc51cb60e441c508c1bdd374f8637b320ee53c252277e`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a43e2e4fc3ef203cecf379efbcea7465d06dcb2c8c104a249ce67f169be38d3`  
		Last Modified: Wed, 06 Apr 2022 06:29:58 GMT  
		Size: 90.3 MB (90345953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e5dbb81bd3e3cb0af9cd73a48f109b99c4dbda39fd549b68c1b07da7f1653f`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dfc2b3e168179bbae7e90a25a3745e7a154cbf48bdc3f9e55bce53aea2fef5`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880985305c8f0183a6f2e94ca8428ec6392e22eb5e6a8a003f18ba2ffdc33618`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:d454a91588360cd4d1c37efa9293427956c242142a109507d81ca9968715a18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:819963937619a1891b4e1f4c6125d4ea4f3bb6195d72042307ae2cd68071b1ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad3c8256a516f93654aed599432527de806b5da9c2088233c692591c291a9a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:31 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 22 Apr 2022 02:52:31 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 22 Apr 2022 02:52:31 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 22 Apr 2022 02:52:31 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 22 Apr 2022 02:52:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:52:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:52:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:52:54 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:52:54 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:52:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:52:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:52:55 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:52:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b744c9184d699263c8a3ef44c0767a0429db8c6892701eef91c0237b61421e5`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d15a78b4ec63a31d0349185788c72af768e99002fcbb2a6a46c3a8a6fd263eb`  
		Last Modified: Fri, 22 Apr 2022 02:57:36 GMT  
		Size: 85.8 MB (85753125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76088cf45319c739b3d59169b2c599481218be04824f4aadb20657eb83c43f1b`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4519dcc8d4be31b8246d8f666c1db6c7eab0ff35ade6ece88c6b7f39a784d29`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 6.8 KB (6769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f902b376b26e5290db3e69f9cfadc24be1001705c68c97205619cd98b2a00d`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7b57317ff2a88ce03e890f2af9935783be428c6a7338246d2a769f2337adfd87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123002163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a800c91370dab00fef4613f7de3fd6d98bb439a35be243b2d4bead63c77e58e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:39:22 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 05 Apr 2022 23:39:23 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 05 Apr 2022 23:39:24 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Tue, 05 Apr 2022 23:39:25 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Tue, 05 Apr 2022 23:39:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:39:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:39:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:39:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:39:58 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:39:59 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:39:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:40:01 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:40:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae937f7cdd608c1e55602715591fcccd2ef458d343d49c4624e4f5548eb7cb6`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0739a94b8e362ab4dcd6ee7ccb9e1831c626697dd4399aeee2dc309cb9f55b7`  
		Last Modified: Tue, 05 Apr 2022 23:46:22 GMT  
		Size: 84.9 MB (84926018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5445c5978da64786d52c0af313da2b96045ec64d3ff111176b31a12b92ede7`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b489aa0ef89a027e08e62ed43068a4438c948fc1ffedfd7f1f922bd2ccd53f`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def5e5f2644da0b7228457a3c1b4781b12440c749482e87fce0ff9a9a326da31`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5ce596303c369e20bf1cfe515bf50072f54352805dedf84ae8d47d48d3fd6773
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136560761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0049b450ab4d30711dba89ae824e1ad6462d78839299509a3ade9063437bf75a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:09:58 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 06:10:03 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 06:10:08 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 06:10:14 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 06:10:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:10:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:12:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:12:40 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:12:41 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:12:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:12:56 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:13:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a178369021f591b4cc51cb60e441c508c1bdd374f8637b320ee53c252277e`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a43e2e4fc3ef203cecf379efbcea7465d06dcb2c8c104a249ce67f169be38d3`  
		Last Modified: Wed, 06 Apr 2022 06:29:58 GMT  
		Size: 90.3 MB (90345953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e5dbb81bd3e3cb0af9cd73a48f109b99c4dbda39fd549b68c1b07da7f1653f`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dfc2b3e168179bbae7e90a25a3745e7a154cbf48bdc3f9e55bce53aea2fef5`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880985305c8f0183a6f2e94ca8428ec6392e22eb5e6a8a003f18ba2ffdc33618`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.24`

```console
$ docker pull mariadb@sha256:d454a91588360cd4d1c37efa9293427956c242142a109507d81ca9968715a18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.24` - linux; amd64

```console
$ docker pull mariadb@sha256:819963937619a1891b4e1f4c6125d4ea4f3bb6195d72042307ae2cd68071b1ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad3c8256a516f93654aed599432527de806b5da9c2088233c692591c291a9a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:31 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 22 Apr 2022 02:52:31 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 22 Apr 2022 02:52:31 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 22 Apr 2022 02:52:31 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 22 Apr 2022 02:52:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:52:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:52:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:52:54 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:52:54 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:52:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:52:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:52:55 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:52:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b744c9184d699263c8a3ef44c0767a0429db8c6892701eef91c0237b61421e5`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d15a78b4ec63a31d0349185788c72af768e99002fcbb2a6a46c3a8a6fd263eb`  
		Last Modified: Fri, 22 Apr 2022 02:57:36 GMT  
		Size: 85.8 MB (85753125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76088cf45319c739b3d59169b2c599481218be04824f4aadb20657eb83c43f1b`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4519dcc8d4be31b8246d8f666c1db6c7eab0ff35ade6ece88c6b7f39a784d29`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 6.8 KB (6769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f902b376b26e5290db3e69f9cfadc24be1001705c68c97205619cd98b2a00d`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7b57317ff2a88ce03e890f2af9935783be428c6a7338246d2a769f2337adfd87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123002163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a800c91370dab00fef4613f7de3fd6d98bb439a35be243b2d4bead63c77e58e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:39:22 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 05 Apr 2022 23:39:23 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 05 Apr 2022 23:39:24 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Tue, 05 Apr 2022 23:39:25 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Tue, 05 Apr 2022 23:39:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:39:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:39:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:39:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:39:58 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:39:59 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:39:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:40:01 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:40:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae937f7cdd608c1e55602715591fcccd2ef458d343d49c4624e4f5548eb7cb6`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0739a94b8e362ab4dcd6ee7ccb9e1831c626697dd4399aeee2dc309cb9f55b7`  
		Last Modified: Tue, 05 Apr 2022 23:46:22 GMT  
		Size: 84.9 MB (84926018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5445c5978da64786d52c0af313da2b96045ec64d3ff111176b31a12b92ede7`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b489aa0ef89a027e08e62ed43068a4438c948fc1ffedfd7f1f922bd2ccd53f`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def5e5f2644da0b7228457a3c1b4781b12440c749482e87fce0ff9a9a326da31`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5ce596303c369e20bf1cfe515bf50072f54352805dedf84ae8d47d48d3fd6773
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136560761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0049b450ab4d30711dba89ae824e1ad6462d78839299509a3ade9063437bf75a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:09:58 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 06:10:03 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 06:10:08 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 06:10:14 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 06:10:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:10:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:12:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:12:40 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:12:41 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:12:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:12:56 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:13:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a178369021f591b4cc51cb60e441c508c1bdd374f8637b320ee53c252277e`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a43e2e4fc3ef203cecf379efbcea7465d06dcb2c8c104a249ce67f169be38d3`  
		Last Modified: Wed, 06 Apr 2022 06:29:58 GMT  
		Size: 90.3 MB (90345953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e5dbb81bd3e3cb0af9cd73a48f109b99c4dbda39fd549b68c1b07da7f1653f`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dfc2b3e168179bbae7e90a25a3745e7a154cbf48bdc3f9e55bce53aea2fef5`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880985305c8f0183a6f2e94ca8428ec6392e22eb5e6a8a003f18ba2ffdc33618`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.24-focal`

```console
$ docker pull mariadb@sha256:d454a91588360cd4d1c37efa9293427956c242142a109507d81ca9968715a18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.24-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:819963937619a1891b4e1f4c6125d4ea4f3bb6195d72042307ae2cd68071b1ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad3c8256a516f93654aed599432527de806b5da9c2088233c692591c291a9a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:31 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 22 Apr 2022 02:52:31 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 22 Apr 2022 02:52:31 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 22 Apr 2022 02:52:31 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 22 Apr 2022 02:52:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:52:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:52:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:52:54 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:52:54 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:52:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 22 Apr 2022 02:52:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:52:55 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:52:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b744c9184d699263c8a3ef44c0767a0429db8c6892701eef91c0237b61421e5`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d15a78b4ec63a31d0349185788c72af768e99002fcbb2a6a46c3a8a6fd263eb`  
		Last Modified: Fri, 22 Apr 2022 02:57:36 GMT  
		Size: 85.8 MB (85753125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76088cf45319c739b3d59169b2c599481218be04824f4aadb20657eb83c43f1b`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4519dcc8d4be31b8246d8f666c1db6c7eab0ff35ade6ece88c6b7f39a784d29`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 6.8 KB (6769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f902b376b26e5290db3e69f9cfadc24be1001705c68c97205619cd98b2a00d`  
		Last Modified: Fri, 22 Apr 2022 02:57:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7b57317ff2a88ce03e890f2af9935783be428c6a7338246d2a769f2337adfd87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123002163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a800c91370dab00fef4613f7de3fd6d98bb439a35be243b2d4bead63c77e58e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:39:22 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 05 Apr 2022 23:39:23 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 05 Apr 2022 23:39:24 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Tue, 05 Apr 2022 23:39:25 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Tue, 05 Apr 2022 23:39:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:39:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:39:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:39:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:39:58 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:39:59 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:39:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 05 Apr 2022 23:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:40:01 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:40:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae937f7cdd608c1e55602715591fcccd2ef458d343d49c4624e4f5548eb7cb6`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0739a94b8e362ab4dcd6ee7ccb9e1831c626697dd4399aeee2dc309cb9f55b7`  
		Last Modified: Tue, 05 Apr 2022 23:46:22 GMT  
		Size: 84.9 MB (84926018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5445c5978da64786d52c0af313da2b96045ec64d3ff111176b31a12b92ede7`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b489aa0ef89a027e08e62ed43068a4438c948fc1ffedfd7f1f922bd2ccd53f`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def5e5f2644da0b7228457a3c1b4781b12440c749482e87fce0ff9a9a326da31`  
		Last Modified: Tue, 05 Apr 2022 23:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5ce596303c369e20bf1cfe515bf50072f54352805dedf84ae8d47d48d3fd6773
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136560761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0049b450ab4d30711dba89ae824e1ad6462d78839299509a3ade9063437bf75a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:09:58 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 06:10:03 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 06:10:08 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 06:10:14 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 06:10:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:10:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:12:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:12:40 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:12:41 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:12:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 06:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:12:56 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:13:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a178369021f591b4cc51cb60e441c508c1bdd374f8637b320ee53c252277e`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a43e2e4fc3ef203cecf379efbcea7465d06dcb2c8c104a249ce67f169be38d3`  
		Last Modified: Wed, 06 Apr 2022 06:29:58 GMT  
		Size: 90.3 MB (90345953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e5dbb81bd3e3cb0af9cd73a48f109b99c4dbda39fd549b68c1b07da7f1653f`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dfc2b3e168179bbae7e90a25a3745e7a154cbf48bdc3f9e55bce53aea2fef5`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880985305c8f0183a6f2e94ca8428ec6392e22eb5e6a8a003f18ba2ffdc33618`  
		Last Modified: Wed, 06 Apr 2022 06:29:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:e61ac7f6f384bbdf4fe7f29b9b35229d7327ba6b3050a39b30a743939dc47603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:5d5daf7e35f3b1e8dc54b7f279bf8d0fabdc5489f329b9e4af289e92c692abd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127923752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8247f649c1ad0ed98bded330f521a2114583f7d253dcb91228d0f865e76ac90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:03 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:52:03 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:52:03 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:52:03 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:52:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:52:25 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:52:25 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:52:25 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:52:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:52:25 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:52:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490dd7915b8002205becea23f1301b54b93df661098f49fb349100eace3c473d`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0791622d551403008eaaa8a55b8c2ce888d9cf059518ffec3789cef789c4c987`  
		Last Modified: Fri, 22 Apr 2022 02:57:07 GMT  
		Size: 88.0 MB (87997283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43c35539e9763ffe7ff15d83e7fe71d078c83207758e1114050595ca29ecfc9`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42c10e4d1ed516fbfdc6e0848f37064f65ff78b2638f1c30002dbd8850e140d`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 6.8 KB (6769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c1c1366228a7e26641352ae90752a61a5878fde7aca3fca56723f427ba135526
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125184175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c82a89978bc9f09f40479630d98948afe6415e734fd8683205be1523f96135`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:38:38 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:38:39 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:38:40 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:38:41 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:38:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:38:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:39:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:39:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:39:09 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:39:10 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:39:11 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77310d2400907e7e91427f8e26f473ac1f4877ee906b98ab6aaace077c6bc17d`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dbe984f8b4d1705b10a9ef118a909a3e3901eb037a679736804c24f73eb57f`  
		Last Modified: Tue, 05 Apr 2022 23:45:50 GMT  
		Size: 87.1 MB (87108148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4b15e55c412040ddc97fe0014e928b42f5e39e609897499208e5d58a042820`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff5a50cdf79c9f700ad72a77ebdbea595780ea75c5e94f5dcf1b75b0bf25522`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:db8a91713e57661a449d5c78e43cdf3c719fa7791f9bf8f1524c019776d54a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138781862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf547d9ac61f58e9edec1da3ef77cf9df432f12ca344baf1882d95913ae5a896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:06:49 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 06:06:51 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 06:06:55 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 06:06:59 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 06:07:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:09:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:09:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:09:25 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:09:26 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:09:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:09:34 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:09:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617a2e535b1283d12ee78ea375f013ef2f0f123de9511ce9745cd285a8fec00`  
		Last Modified: Wed, 06 Apr 2022 06:29:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d1995a652d0c44ad4189d51ed6dfb950f1edb27dafa2add330b4f8cd86c5f`  
		Last Modified: Wed, 06 Apr 2022 06:29:18 GMT  
		Size: 92.6 MB (92567174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839d4891454c5ff141f738c6fe5b733e0959ffc2fee1fdc57aace5fd547efed5`  
		Last Modified: Wed, 06 Apr 2022 06:29:00 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf0682f26533d0bdb76da32a6d90ac08d551b1219e79e9f7d742e0e711a671e`  
		Last Modified: Wed, 06 Apr 2022 06:29:00 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:04652e28b66023a0295a84be62aefb6f5b2ab32171e314175a3f63a78c6aeef3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127198159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc3c5916525d13560f4b4b25b0e8151e47a8bc455aae8a0f0a3ae03a19b2f45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:23:41 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:23:41 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:23:42 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:23:42 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:23:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:23:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:24:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:24:42 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:24:42 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:24:42 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:24:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:24:44 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:24:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fb65dfb7bfadd22596171fe5454faeb610cc39920fc6fcddd3f99715b6594f`  
		Last Modified: Fri, 22 Apr 2022 02:27:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c4360a6f8123f6f8730826efa42bc162a0abfc6cc4d3e762db3f61c3f98848`  
		Last Modified: Fri, 22 Apr 2022 02:27:28 GMT  
		Size: 89.3 MB (89290810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a851624fbd4c0981e63aabd6bbfdb07b44616bed75da2079b3b7d6b78803f734`  
		Last Modified: Fri, 22 Apr 2022 02:27:16 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066be019881a416b3163e98a409f5313e4b468558f7a3c363d947312515c2d44`  
		Last Modified: Fri, 22 Apr 2022 02:27:15 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:e61ac7f6f384bbdf4fe7f29b9b35229d7327ba6b3050a39b30a743939dc47603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:5d5daf7e35f3b1e8dc54b7f279bf8d0fabdc5489f329b9e4af289e92c692abd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127923752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8247f649c1ad0ed98bded330f521a2114583f7d253dcb91228d0f865e76ac90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:03 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:52:03 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:52:03 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:52:03 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:52:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:52:25 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:52:25 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:52:25 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:52:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:52:25 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:52:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490dd7915b8002205becea23f1301b54b93df661098f49fb349100eace3c473d`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0791622d551403008eaaa8a55b8c2ce888d9cf059518ffec3789cef789c4c987`  
		Last Modified: Fri, 22 Apr 2022 02:57:07 GMT  
		Size: 88.0 MB (87997283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43c35539e9763ffe7ff15d83e7fe71d078c83207758e1114050595ca29ecfc9`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42c10e4d1ed516fbfdc6e0848f37064f65ff78b2638f1c30002dbd8850e140d`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 6.8 KB (6769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c1c1366228a7e26641352ae90752a61a5878fde7aca3fca56723f427ba135526
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125184175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c82a89978bc9f09f40479630d98948afe6415e734fd8683205be1523f96135`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:38:38 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:38:39 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:38:40 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:38:41 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:38:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:38:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:39:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:39:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:39:09 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:39:10 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:39:11 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77310d2400907e7e91427f8e26f473ac1f4877ee906b98ab6aaace077c6bc17d`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dbe984f8b4d1705b10a9ef118a909a3e3901eb037a679736804c24f73eb57f`  
		Last Modified: Tue, 05 Apr 2022 23:45:50 GMT  
		Size: 87.1 MB (87108148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4b15e55c412040ddc97fe0014e928b42f5e39e609897499208e5d58a042820`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff5a50cdf79c9f700ad72a77ebdbea595780ea75c5e94f5dcf1b75b0bf25522`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:db8a91713e57661a449d5c78e43cdf3c719fa7791f9bf8f1524c019776d54a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138781862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf547d9ac61f58e9edec1da3ef77cf9df432f12ca344baf1882d95913ae5a896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:06:49 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 06:06:51 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 06:06:55 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 06:06:59 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 06:07:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:09:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:09:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:09:25 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:09:26 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:09:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:09:34 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:09:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617a2e535b1283d12ee78ea375f013ef2f0f123de9511ce9745cd285a8fec00`  
		Last Modified: Wed, 06 Apr 2022 06:29:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d1995a652d0c44ad4189d51ed6dfb950f1edb27dafa2add330b4f8cd86c5f`  
		Last Modified: Wed, 06 Apr 2022 06:29:18 GMT  
		Size: 92.6 MB (92567174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839d4891454c5ff141f738c6fe5b733e0959ffc2fee1fdc57aace5fd547efed5`  
		Last Modified: Wed, 06 Apr 2022 06:29:00 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf0682f26533d0bdb76da32a6d90ac08d551b1219e79e9f7d742e0e711a671e`  
		Last Modified: Wed, 06 Apr 2022 06:29:00 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:04652e28b66023a0295a84be62aefb6f5b2ab32171e314175a3f63a78c6aeef3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127198159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc3c5916525d13560f4b4b25b0e8151e47a8bc455aae8a0f0a3ae03a19b2f45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:23:41 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:23:41 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:23:42 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:23:42 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:23:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:23:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:24:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:24:42 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:24:42 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:24:42 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:24:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:24:44 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:24:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fb65dfb7bfadd22596171fe5454faeb610cc39920fc6fcddd3f99715b6594f`  
		Last Modified: Fri, 22 Apr 2022 02:27:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c4360a6f8123f6f8730826efa42bc162a0abfc6cc4d3e762db3f61c3f98848`  
		Last Modified: Fri, 22 Apr 2022 02:27:28 GMT  
		Size: 89.3 MB (89290810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a851624fbd4c0981e63aabd6bbfdb07b44616bed75da2079b3b7d6b78803f734`  
		Last Modified: Fri, 22 Apr 2022 02:27:16 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066be019881a416b3163e98a409f5313e4b468558f7a3c363d947312515c2d44`  
		Last Modified: Fri, 22 Apr 2022 02:27:15 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.15`

```console
$ docker pull mariadb@sha256:e61ac7f6f384bbdf4fe7f29b9b35229d7327ba6b3050a39b30a743939dc47603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.15` - linux; amd64

```console
$ docker pull mariadb@sha256:5d5daf7e35f3b1e8dc54b7f279bf8d0fabdc5489f329b9e4af289e92c692abd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127923752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8247f649c1ad0ed98bded330f521a2114583f7d253dcb91228d0f865e76ac90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:03 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:52:03 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:52:03 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:52:03 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:52:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:52:25 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:52:25 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:52:25 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:52:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:52:25 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:52:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490dd7915b8002205becea23f1301b54b93df661098f49fb349100eace3c473d`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0791622d551403008eaaa8a55b8c2ce888d9cf059518ffec3789cef789c4c987`  
		Last Modified: Fri, 22 Apr 2022 02:57:07 GMT  
		Size: 88.0 MB (87997283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43c35539e9763ffe7ff15d83e7fe71d078c83207758e1114050595ca29ecfc9`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42c10e4d1ed516fbfdc6e0848f37064f65ff78b2638f1c30002dbd8850e140d`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 6.8 KB (6769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c1c1366228a7e26641352ae90752a61a5878fde7aca3fca56723f427ba135526
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125184175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c82a89978bc9f09f40479630d98948afe6415e734fd8683205be1523f96135`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:38:38 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:38:39 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:38:40 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:38:41 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:38:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:38:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:39:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:39:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:39:09 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:39:10 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:39:11 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77310d2400907e7e91427f8e26f473ac1f4877ee906b98ab6aaace077c6bc17d`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dbe984f8b4d1705b10a9ef118a909a3e3901eb037a679736804c24f73eb57f`  
		Last Modified: Tue, 05 Apr 2022 23:45:50 GMT  
		Size: 87.1 MB (87108148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4b15e55c412040ddc97fe0014e928b42f5e39e609897499208e5d58a042820`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff5a50cdf79c9f700ad72a77ebdbea595780ea75c5e94f5dcf1b75b0bf25522`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; ppc64le

```console
$ docker pull mariadb@sha256:db8a91713e57661a449d5c78e43cdf3c719fa7791f9bf8f1524c019776d54a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138781862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf547d9ac61f58e9edec1da3ef77cf9df432f12ca344baf1882d95913ae5a896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:06:49 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 06:06:51 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 06:06:55 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 06:06:59 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 06:07:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:09:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:09:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:09:25 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:09:26 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:09:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:09:34 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:09:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617a2e535b1283d12ee78ea375f013ef2f0f123de9511ce9745cd285a8fec00`  
		Last Modified: Wed, 06 Apr 2022 06:29:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d1995a652d0c44ad4189d51ed6dfb950f1edb27dafa2add330b4f8cd86c5f`  
		Last Modified: Wed, 06 Apr 2022 06:29:18 GMT  
		Size: 92.6 MB (92567174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839d4891454c5ff141f738c6fe5b733e0959ffc2fee1fdc57aace5fd547efed5`  
		Last Modified: Wed, 06 Apr 2022 06:29:00 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf0682f26533d0bdb76da32a6d90ac08d551b1219e79e9f7d742e0e711a671e`  
		Last Modified: Wed, 06 Apr 2022 06:29:00 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; s390x

```console
$ docker pull mariadb@sha256:04652e28b66023a0295a84be62aefb6f5b2ab32171e314175a3f63a78c6aeef3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127198159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc3c5916525d13560f4b4b25b0e8151e47a8bc455aae8a0f0a3ae03a19b2f45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:23:41 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:23:41 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:23:42 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:23:42 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:23:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:23:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:24:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:24:42 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:24:42 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:24:42 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:24:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:24:44 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:24:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fb65dfb7bfadd22596171fe5454faeb610cc39920fc6fcddd3f99715b6594f`  
		Last Modified: Fri, 22 Apr 2022 02:27:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c4360a6f8123f6f8730826efa42bc162a0abfc6cc4d3e762db3f61c3f98848`  
		Last Modified: Fri, 22 Apr 2022 02:27:28 GMT  
		Size: 89.3 MB (89290810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a851624fbd4c0981e63aabd6bbfdb07b44616bed75da2079b3b7d6b78803f734`  
		Last Modified: Fri, 22 Apr 2022 02:27:16 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066be019881a416b3163e98a409f5313e4b468558f7a3c363d947312515c2d44`  
		Last Modified: Fri, 22 Apr 2022 02:27:15 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.15-focal`

```console
$ docker pull mariadb@sha256:e61ac7f6f384bbdf4fe7f29b9b35229d7327ba6b3050a39b30a743939dc47603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.15-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:5d5daf7e35f3b1e8dc54b7f279bf8d0fabdc5489f329b9e4af289e92c692abd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127923752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8247f649c1ad0ed98bded330f521a2114583f7d253dcb91228d0f865e76ac90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:52:03 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:52:03 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:52:03 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:52:03 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:52:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:52:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:52:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:52:25 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:52:25 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:52:25 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:52:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:52:25 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:52:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490dd7915b8002205becea23f1301b54b93df661098f49fb349100eace3c473d`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0791622d551403008eaaa8a55b8c2ce888d9cf059518ffec3789cef789c4c987`  
		Last Modified: Fri, 22 Apr 2022 02:57:07 GMT  
		Size: 88.0 MB (87997283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43c35539e9763ffe7ff15d83e7fe71d078c83207758e1114050595ca29ecfc9`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42c10e4d1ed516fbfdc6e0848f37064f65ff78b2638f1c30002dbd8850e140d`  
		Last Modified: Fri, 22 Apr 2022 02:56:54 GMT  
		Size: 6.8 KB (6769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c1c1366228a7e26641352ae90752a61a5878fde7aca3fca56723f427ba135526
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125184175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c82a89978bc9f09f40479630d98948afe6415e734fd8683205be1523f96135`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:38:38 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:38:39 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:38:40 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:38:41 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:38:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:38:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:39:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:39:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:39:09 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:39:10 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:39:11 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77310d2400907e7e91427f8e26f473ac1f4877ee906b98ab6aaace077c6bc17d`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dbe984f8b4d1705b10a9ef118a909a3e3901eb037a679736804c24f73eb57f`  
		Last Modified: Tue, 05 Apr 2022 23:45:50 GMT  
		Size: 87.1 MB (87108148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4b15e55c412040ddc97fe0014e928b42f5e39e609897499208e5d58a042820`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff5a50cdf79c9f700ad72a77ebdbea595780ea75c5e94f5dcf1b75b0bf25522`  
		Last Modified: Tue, 05 Apr 2022 23:45:37 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:db8a91713e57661a449d5c78e43cdf3c719fa7791f9bf8f1524c019776d54a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138781862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf547d9ac61f58e9edec1da3ef77cf9df432f12ca344baf1882d95913ae5a896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:06:49 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 06:06:51 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 06:06:55 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 06:06:59 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 06:07:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:09:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:09:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:09:25 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:09:26 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:09:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:09:34 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:09:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617a2e535b1283d12ee78ea375f013ef2f0f123de9511ce9745cd285a8fec00`  
		Last Modified: Wed, 06 Apr 2022 06:29:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d1995a652d0c44ad4189d51ed6dfb950f1edb27dafa2add330b4f8cd86c5f`  
		Last Modified: Wed, 06 Apr 2022 06:29:18 GMT  
		Size: 92.6 MB (92567174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839d4891454c5ff141f738c6fe5b733e0959ffc2fee1fdc57aace5fd547efed5`  
		Last Modified: Wed, 06 Apr 2022 06:29:00 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf0682f26533d0bdb76da32a6d90ac08d551b1219e79e9f7d742e0e711a671e`  
		Last Modified: Wed, 06 Apr 2022 06:29:00 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:04652e28b66023a0295a84be62aefb6f5b2ab32171e314175a3f63a78c6aeef3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127198159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc3c5916525d13560f4b4b25b0e8151e47a8bc455aae8a0f0a3ae03a19b2f45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:23:41 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:23:41 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 22 Apr 2022 02:23:42 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:23:42 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 22 Apr 2022 02:23:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:23:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:24:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:24:42 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:24:42 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:24:42 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:24:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:24:44 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:24:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fb65dfb7bfadd22596171fe5454faeb610cc39920fc6fcddd3f99715b6594f`  
		Last Modified: Fri, 22 Apr 2022 02:27:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c4360a6f8123f6f8730826efa42bc162a0abfc6cc4d3e762db3f61c3f98848`  
		Last Modified: Fri, 22 Apr 2022 02:27:28 GMT  
		Size: 89.3 MB (89290810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a851624fbd4c0981e63aabd6bbfdb07b44616bed75da2079b3b7d6b78803f734`  
		Last Modified: Fri, 22 Apr 2022 02:27:16 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066be019881a416b3163e98a409f5313e4b468558f7a3c363d947312515c2d44`  
		Last Modified: Fri, 22 Apr 2022 02:27:15 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:4daa0a3034a9dc8a350bc14a4d90f02d96eb03f8f173e22f5e288cabf4f0d48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:50f7f199fb81c7cc4a3b367ee8a25f18ce83439a565d094d1d55d25924b195a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b1a894e91d2f10ceabfce4375d818c5ca907add9dfbaf8d5954c717baa1d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:35 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:51:35 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:51:35 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:51:35 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:51:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:58 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:58 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585fa6ed9f9263b79c20959c2e25d32d6523ac4267f3f4b450311c77bbfc30ff`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c4c29c67dbd6b0c81f43ef62d78d3a581ab7f158f68716c49129209ce26140`  
		Last Modified: Fri, 22 Apr 2022 02:56:37 GMT  
		Size: 88.2 MB (88243195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e60110958fb03947e33902acb382866ef3dc70a9dd00ec275c738ccf39c525`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505d73d050133db6e682e04624cbd8a35f21434a6abfe41a42acf3d86f2a8be2`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:6c19a6398374c6edbf818b7e3ad38386b7291f1285df2fb5107998214705a11b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125268888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e48e5513cea6c16a59799e8f49ec96f5ca96ba77523e252dd8bd0cbe397cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:46 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:37:47 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:37:48 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:37:49 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:37:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:38:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:38:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:38:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:38:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:38:31 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:38:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed8fb95bcdf669d85f5ab1a92ebf76ffbe15e967f8fb8f2b25f9941ba5287b8`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe252cbc90974dd81a735bd409fad908c5b318ad375363730709ac3ef5acf81`  
		Last Modified: Tue, 05 Apr 2022 23:45:17 GMT  
		Size: 87.2 MB (87192865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7d993e41c7701c00ef553bd87a3fae5a39ed1f03b104c169ec432c21559dfb`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c52b754325316917513478d6fb6c3a399a889e895c1b13d5494aad6e93f6ca`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:878e304deb4cb67343dac2685154d4a44895c5e712e637d03ae0358bc4b5739a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138842414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a611ecffa5f3b09f3db55891625d99f4e5530acac85af106e7b747967606b149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:01:10 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 06:01:15 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 06:01:21 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 06:01:26 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 06:01:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:01:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:06:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:06:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:06:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:06:23 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:06:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:06:30 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:06:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ce788e3e0cd8a44529d2e1f2e6e2a00ed6649cc7c2ab9541fd945bda01dd7e`  
		Last Modified: Wed, 06 Apr 2022 06:28:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda9e38416c1445098d83a650c6067a6b35a909f889fd5be9762fe2843e902e`  
		Last Modified: Wed, 06 Apr 2022 06:28:39 GMT  
		Size: 92.6 MB (92627724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa6e3137397e91dec4c63f7f7d20b68085a007a247f84e7ae4a9307a4b3975`  
		Last Modified: Wed, 06 Apr 2022 06:28:22 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf051756ec0b5bf3aa049d3bf473e48d94de2d67624c50ee4782e6213d1016`  
		Last Modified: Wed, 06 Apr 2022 06:28:21 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; s390x

```console
$ docker pull mariadb@sha256:f3145aec7ef88c78b5e58998c5533b612c4340b7653db9e515771788921372de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127224189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5299ca6cc5d9abc9540158598205030ffb81fc77ef90715c497be93c07a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:22:07 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:22:08 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:22:08 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:22:08 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:22:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:22:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:23:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:23:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:23:25 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:23:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:23:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:23:26 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:23:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e35c54487aecc070dabfd10f05fea192997a924c40f34ce639efb014e680c9`  
		Last Modified: Fri, 22 Apr 2022 02:26:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3c9680acb91618fb11946acb1d0ffe3b786aa0dca839e443807bdf8c602bf7`  
		Last Modified: Fri, 22 Apr 2022 02:27:02 GMT  
		Size: 89.3 MB (89316836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2f75131c8fca54541218624eb65a78cd5a644e59d8d26d299f25ee5de9145b`  
		Last Modified: Fri, 22 Apr 2022 02:26:49 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452e2c047542abc87ef70ff67d163f63116cd3ffe1eadc207a6ec96b27099743`  
		Last Modified: Fri, 22 Apr 2022 02:26:50 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:4daa0a3034a9dc8a350bc14a4d90f02d96eb03f8f173e22f5e288cabf4f0d48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:50f7f199fb81c7cc4a3b367ee8a25f18ce83439a565d094d1d55d25924b195a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b1a894e91d2f10ceabfce4375d818c5ca907add9dfbaf8d5954c717baa1d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:35 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:51:35 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:51:35 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:51:35 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:51:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:58 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:58 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585fa6ed9f9263b79c20959c2e25d32d6523ac4267f3f4b450311c77bbfc30ff`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c4c29c67dbd6b0c81f43ef62d78d3a581ab7f158f68716c49129209ce26140`  
		Last Modified: Fri, 22 Apr 2022 02:56:37 GMT  
		Size: 88.2 MB (88243195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e60110958fb03947e33902acb382866ef3dc70a9dd00ec275c738ccf39c525`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505d73d050133db6e682e04624cbd8a35f21434a6abfe41a42acf3d86f2a8be2`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:6c19a6398374c6edbf818b7e3ad38386b7291f1285df2fb5107998214705a11b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125268888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e48e5513cea6c16a59799e8f49ec96f5ca96ba77523e252dd8bd0cbe397cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:46 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:37:47 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:37:48 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:37:49 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:37:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:38:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:38:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:38:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:38:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:38:31 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:38:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed8fb95bcdf669d85f5ab1a92ebf76ffbe15e967f8fb8f2b25f9941ba5287b8`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe252cbc90974dd81a735bd409fad908c5b318ad375363730709ac3ef5acf81`  
		Last Modified: Tue, 05 Apr 2022 23:45:17 GMT  
		Size: 87.2 MB (87192865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7d993e41c7701c00ef553bd87a3fae5a39ed1f03b104c169ec432c21559dfb`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c52b754325316917513478d6fb6c3a399a889e895c1b13d5494aad6e93f6ca`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:878e304deb4cb67343dac2685154d4a44895c5e712e637d03ae0358bc4b5739a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138842414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a611ecffa5f3b09f3db55891625d99f4e5530acac85af106e7b747967606b149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:01:10 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 06:01:15 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 06:01:21 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 06:01:26 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 06:01:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:01:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:06:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:06:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:06:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:06:23 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:06:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:06:30 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:06:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ce788e3e0cd8a44529d2e1f2e6e2a00ed6649cc7c2ab9541fd945bda01dd7e`  
		Last Modified: Wed, 06 Apr 2022 06:28:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda9e38416c1445098d83a650c6067a6b35a909f889fd5be9762fe2843e902e`  
		Last Modified: Wed, 06 Apr 2022 06:28:39 GMT  
		Size: 92.6 MB (92627724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa6e3137397e91dec4c63f7f7d20b68085a007a247f84e7ae4a9307a4b3975`  
		Last Modified: Wed, 06 Apr 2022 06:28:22 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf051756ec0b5bf3aa049d3bf473e48d94de2d67624c50ee4782e6213d1016`  
		Last Modified: Wed, 06 Apr 2022 06:28:21 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:f3145aec7ef88c78b5e58998c5533b612c4340b7653db9e515771788921372de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127224189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5299ca6cc5d9abc9540158598205030ffb81fc77ef90715c497be93c07a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:22:07 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:22:08 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:22:08 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:22:08 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:22:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:22:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:23:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:23:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:23:25 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:23:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:23:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:23:26 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:23:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e35c54487aecc070dabfd10f05fea192997a924c40f34ce639efb014e680c9`  
		Last Modified: Fri, 22 Apr 2022 02:26:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3c9680acb91618fb11946acb1d0ffe3b786aa0dca839e443807bdf8c602bf7`  
		Last Modified: Fri, 22 Apr 2022 02:27:02 GMT  
		Size: 89.3 MB (89316836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2f75131c8fca54541218624eb65a78cd5a644e59d8d26d299f25ee5de9145b`  
		Last Modified: Fri, 22 Apr 2022 02:26:49 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452e2c047542abc87ef70ff67d163f63116cd3ffe1eadc207a6ec96b27099743`  
		Last Modified: Fri, 22 Apr 2022 02:26:50 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.7`

```console
$ docker pull mariadb@sha256:4daa0a3034a9dc8a350bc14a4d90f02d96eb03f8f173e22f5e288cabf4f0d48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.7` - linux; amd64

```console
$ docker pull mariadb@sha256:50f7f199fb81c7cc4a3b367ee8a25f18ce83439a565d094d1d55d25924b195a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b1a894e91d2f10ceabfce4375d818c5ca907add9dfbaf8d5954c717baa1d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:35 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:51:35 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:51:35 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:51:35 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:51:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:58 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:58 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585fa6ed9f9263b79c20959c2e25d32d6523ac4267f3f4b450311c77bbfc30ff`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c4c29c67dbd6b0c81f43ef62d78d3a581ab7f158f68716c49129209ce26140`  
		Last Modified: Fri, 22 Apr 2022 02:56:37 GMT  
		Size: 88.2 MB (88243195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e60110958fb03947e33902acb382866ef3dc70a9dd00ec275c738ccf39c525`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505d73d050133db6e682e04624cbd8a35f21434a6abfe41a42acf3d86f2a8be2`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:6c19a6398374c6edbf818b7e3ad38386b7291f1285df2fb5107998214705a11b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125268888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e48e5513cea6c16a59799e8f49ec96f5ca96ba77523e252dd8bd0cbe397cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:46 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:37:47 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:37:48 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:37:49 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:37:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:38:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:38:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:38:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:38:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:38:31 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:38:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed8fb95bcdf669d85f5ab1a92ebf76ffbe15e967f8fb8f2b25f9941ba5287b8`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe252cbc90974dd81a735bd409fad908c5b318ad375363730709ac3ef5acf81`  
		Last Modified: Tue, 05 Apr 2022 23:45:17 GMT  
		Size: 87.2 MB (87192865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7d993e41c7701c00ef553bd87a3fae5a39ed1f03b104c169ec432c21559dfb`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c52b754325316917513478d6fb6c3a399a889e895c1b13d5494aad6e93f6ca`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:878e304deb4cb67343dac2685154d4a44895c5e712e637d03ae0358bc4b5739a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138842414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a611ecffa5f3b09f3db55891625d99f4e5530acac85af106e7b747967606b149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:01:10 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 06:01:15 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 06:01:21 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 06:01:26 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 06:01:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:01:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:06:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:06:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:06:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:06:23 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:06:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:06:30 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:06:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ce788e3e0cd8a44529d2e1f2e6e2a00ed6649cc7c2ab9541fd945bda01dd7e`  
		Last Modified: Wed, 06 Apr 2022 06:28:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda9e38416c1445098d83a650c6067a6b35a909f889fd5be9762fe2843e902e`  
		Last Modified: Wed, 06 Apr 2022 06:28:39 GMT  
		Size: 92.6 MB (92627724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa6e3137397e91dec4c63f7f7d20b68085a007a247f84e7ae4a9307a4b3975`  
		Last Modified: Wed, 06 Apr 2022 06:28:22 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf051756ec0b5bf3aa049d3bf473e48d94de2d67624c50ee4782e6213d1016`  
		Last Modified: Wed, 06 Apr 2022 06:28:21 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; s390x

```console
$ docker pull mariadb@sha256:f3145aec7ef88c78b5e58998c5533b612c4340b7653db9e515771788921372de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127224189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5299ca6cc5d9abc9540158598205030ffb81fc77ef90715c497be93c07a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:22:07 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:22:08 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:22:08 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:22:08 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:22:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:22:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:23:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:23:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:23:25 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:23:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:23:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:23:26 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:23:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e35c54487aecc070dabfd10f05fea192997a924c40f34ce639efb014e680c9`  
		Last Modified: Fri, 22 Apr 2022 02:26:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3c9680acb91618fb11946acb1d0ffe3b786aa0dca839e443807bdf8c602bf7`  
		Last Modified: Fri, 22 Apr 2022 02:27:02 GMT  
		Size: 89.3 MB (89316836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2f75131c8fca54541218624eb65a78cd5a644e59d8d26d299f25ee5de9145b`  
		Last Modified: Fri, 22 Apr 2022 02:26:49 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452e2c047542abc87ef70ff67d163f63116cd3ffe1eadc207a6ec96b27099743`  
		Last Modified: Fri, 22 Apr 2022 02:26:50 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.7-focal`

```console
$ docker pull mariadb@sha256:4daa0a3034a9dc8a350bc14a4d90f02d96eb03f8f173e22f5e288cabf4f0d48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:50f7f199fb81c7cc4a3b367ee8a25f18ce83439a565d094d1d55d25924b195a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b1a894e91d2f10ceabfce4375d818c5ca907add9dfbaf8d5954c717baa1d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:35 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:51:35 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:51:35 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:51:35 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:51:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:58 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:58 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585fa6ed9f9263b79c20959c2e25d32d6523ac4267f3f4b450311c77bbfc30ff`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c4c29c67dbd6b0c81f43ef62d78d3a581ab7f158f68716c49129209ce26140`  
		Last Modified: Fri, 22 Apr 2022 02:56:37 GMT  
		Size: 88.2 MB (88243195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e60110958fb03947e33902acb382866ef3dc70a9dd00ec275c738ccf39c525`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505d73d050133db6e682e04624cbd8a35f21434a6abfe41a42acf3d86f2a8be2`  
		Last Modified: Fri, 22 Apr 2022 02:56:24 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:6c19a6398374c6edbf818b7e3ad38386b7291f1285df2fb5107998214705a11b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125268888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e48e5513cea6c16a59799e8f49ec96f5ca96ba77523e252dd8bd0cbe397cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:46 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:37:47 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:37:48 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:37:49 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:37:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:38:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:38:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:38:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:38:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:38:31 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:38:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed8fb95bcdf669d85f5ab1a92ebf76ffbe15e967f8fb8f2b25f9941ba5287b8`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe252cbc90974dd81a735bd409fad908c5b318ad375363730709ac3ef5acf81`  
		Last Modified: Tue, 05 Apr 2022 23:45:17 GMT  
		Size: 87.2 MB (87192865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7d993e41c7701c00ef553bd87a3fae5a39ed1f03b104c169ec432c21559dfb`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c52b754325316917513478d6fb6c3a399a889e895c1b13d5494aad6e93f6ca`  
		Last Modified: Tue, 05 Apr 2022 23:45:04 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:878e304deb4cb67343dac2685154d4a44895c5e712e637d03ae0358bc4b5739a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138842414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a611ecffa5f3b09f3db55891625d99f4e5530acac85af106e7b747967606b149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 06:01:10 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 06:01:15 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 06:01:21 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 06:01:26 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 06:01:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 06:01:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:06:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:06:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:06:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:06:23 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:06:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:06:30 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:06:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ce788e3e0cd8a44529d2e1f2e6e2a00ed6649cc7c2ab9541fd945bda01dd7e`  
		Last Modified: Wed, 06 Apr 2022 06:28:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda9e38416c1445098d83a650c6067a6b35a909f889fd5be9762fe2843e902e`  
		Last Modified: Wed, 06 Apr 2022 06:28:39 GMT  
		Size: 92.6 MB (92627724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa6e3137397e91dec4c63f7f7d20b68085a007a247f84e7ae4a9307a4b3975`  
		Last Modified: Wed, 06 Apr 2022 06:28:22 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf051756ec0b5bf3aa049d3bf473e48d94de2d67624c50ee4782e6213d1016`  
		Last Modified: Wed, 06 Apr 2022 06:28:21 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:f3145aec7ef88c78b5e58998c5533b612c4340b7653db9e515771788921372de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127224189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5299ca6cc5d9abc9540158598205030ffb81fc77ef90715c497be93c07a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:22:07 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:22:08 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 22 Apr 2022 02:22:08 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:22:08 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 22 Apr 2022 02:22:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:22:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:23:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:23:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:23:25 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:23:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:23:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:23:26 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:23:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e35c54487aecc070dabfd10f05fea192997a924c40f34ce639efb014e680c9`  
		Last Modified: Fri, 22 Apr 2022 02:26:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3c9680acb91618fb11946acb1d0ffe3b786aa0dca839e443807bdf8c602bf7`  
		Last Modified: Fri, 22 Apr 2022 02:27:02 GMT  
		Size: 89.3 MB (89316836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2f75131c8fca54541218624eb65a78cd5a644e59d8d26d299f25ee5de9145b`  
		Last Modified: Fri, 22 Apr 2022 02:26:49 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452e2c047542abc87ef70ff67d163f63116cd3ffe1eadc207a6ec96b27099743`  
		Last Modified: Fri, 22 Apr 2022 02:26:50 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7`

```console
$ docker pull mariadb@sha256:fac573c78b2030f062d8582c81d3fa2e30c0922ed0843e0c85c4ac85109868b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7` - linux; amd64

```console
$ docker pull mariadb@sha256:c5cefb5639e0f9360734406cb0f8b7a119c29083705059a1c4509cf31b6f1dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1ace59b072bf4850281c7a3262a76f762ef97d774a38f5a5cddda9514dd811`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:30 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:30 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8f6c64a8fa57732c8eb3db48d751c40e0795aa5ca42f05d27c2e9ab31075bc`  
		Last Modified: Fri, 22 Apr 2022 02:55:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9817bd990fc72a53340f7dfdda9343811b5a6f4cbc914369c092d3994a044a`  
		Last Modified: Fri, 22 Apr 2022 02:55:56 GMT  
		Size: 88.7 MB (88741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14828b87067569c6589bb8a62987321b440e088af17c5e8a0163841f3bba2e26`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233be9bdce04aeae1b3a83158f299fccc9e8ef3535617d5ea40ebe5b9dcac8c6`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:796e80b1be01d8549f5371e79b763d8f1bdb8fb2c37530461322ab5e031ae6dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125720109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beee7eb5f13c4d5c9266d5f791bf31c0ff9e79d90e09676e681da928dd09d2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:00 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:01 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:02 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:37:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:37:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:37:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:37:36 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:37:37 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:37:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd363ec17eba0ec2199c03d0185e2f6c14475cf6ceaed83743eff2f224300830`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25985e8a9660011351be8031303461ef7750186d9ff4c5b1b5a8dea2c855099`  
		Last Modified: Tue, 05 Apr 2022 23:44:29 GMT  
		Size: 87.6 MB (87644090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e720e62a0b31078f92f2b1d0ec407f671a0ff9f556e60f0388dd0b58f49a78f`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a050689af938e8cc8c031932ce64cbfbe13f9f6d5163bb03e5dbb2ba4b412e2`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2dc8d6c759f7bab790ce8cbedf00108435005a6bd5372d6b8402309499bb624b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139538511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421f250d9d97c128e04a281415cbe3e56ea7ba80b2113a776c867ec9c0c91ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:55:13 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:21 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:28 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:34 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:55:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:00:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:00:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:00:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:00:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:00:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:00:38 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:00:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641d6fa031615e90c40a726e13fcfad279784e3095cb5743a622e154a01718eb`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b30ede638c309a8dbf803c86421dce897625fff4aeec32dc718921a25fec337`  
		Last Modified: Wed, 06 Apr 2022 06:27:41 GMT  
		Size: 93.3 MB (93323824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a7b909e1bbdb359c1ae0a294cbeda191102e8cd1149689143b7852ebb6317`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e2336774b01c630d2ec6a19c2c0bddb5ae69fc59869c443b0d4dd7b668127`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; s390x

```console
$ docker pull mariadb@sha256:b2805c726caa7af5fe4e44a3ade5afbbb7f7c780567c147cb36b5c7a363464b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127722709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8b068ba5353d198e5fd7c34100da7ebc6771c257d75e23b80a211925de86aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:21:06 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:06 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:21:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:21:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:21:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:21:57 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:21:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e906a7a4ca515f29ae2f9d042b9d50795a7722dff0e54711609032ab009449`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa65ca376e03fed74f419a6a903362e83d6d4e1e1773ad67ad7183de7bbdf2`  
		Last Modified: Fri, 22 Apr 2022 02:26:26 GMT  
		Size: 89.8 MB (89815355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d48c43c28d400d613cd154b3e3182816a6e8b669d1fd7254e80bd5c51ae5f17`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b5541b27b08286050b0bfd633e5710b2273e67032af256ca1137c955ccbd51`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7-focal`

```console
$ docker pull mariadb@sha256:fac573c78b2030f062d8582c81d3fa2e30c0922ed0843e0c85c4ac85109868b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:c5cefb5639e0f9360734406cb0f8b7a119c29083705059a1c4509cf31b6f1dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1ace59b072bf4850281c7a3262a76f762ef97d774a38f5a5cddda9514dd811`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:30 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:30 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8f6c64a8fa57732c8eb3db48d751c40e0795aa5ca42f05d27c2e9ab31075bc`  
		Last Modified: Fri, 22 Apr 2022 02:55:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9817bd990fc72a53340f7dfdda9343811b5a6f4cbc914369c092d3994a044a`  
		Last Modified: Fri, 22 Apr 2022 02:55:56 GMT  
		Size: 88.7 MB (88741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14828b87067569c6589bb8a62987321b440e088af17c5e8a0163841f3bba2e26`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233be9bdce04aeae1b3a83158f299fccc9e8ef3535617d5ea40ebe5b9dcac8c6`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:796e80b1be01d8549f5371e79b763d8f1bdb8fb2c37530461322ab5e031ae6dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125720109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beee7eb5f13c4d5c9266d5f791bf31c0ff9e79d90e09676e681da928dd09d2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:00 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:01 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:02 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:37:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:37:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:37:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:37:36 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:37:37 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:37:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd363ec17eba0ec2199c03d0185e2f6c14475cf6ceaed83743eff2f224300830`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25985e8a9660011351be8031303461ef7750186d9ff4c5b1b5a8dea2c855099`  
		Last Modified: Tue, 05 Apr 2022 23:44:29 GMT  
		Size: 87.6 MB (87644090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e720e62a0b31078f92f2b1d0ec407f671a0ff9f556e60f0388dd0b58f49a78f`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a050689af938e8cc8c031932ce64cbfbe13f9f6d5163bb03e5dbb2ba4b412e2`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2dc8d6c759f7bab790ce8cbedf00108435005a6bd5372d6b8402309499bb624b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139538511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421f250d9d97c128e04a281415cbe3e56ea7ba80b2113a776c867ec9c0c91ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:55:13 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:21 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:28 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:34 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:55:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:00:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:00:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:00:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:00:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:00:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:00:38 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:00:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641d6fa031615e90c40a726e13fcfad279784e3095cb5743a622e154a01718eb`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b30ede638c309a8dbf803c86421dce897625fff4aeec32dc718921a25fec337`  
		Last Modified: Wed, 06 Apr 2022 06:27:41 GMT  
		Size: 93.3 MB (93323824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a7b909e1bbdb359c1ae0a294cbeda191102e8cd1149689143b7852ebb6317`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e2336774b01c630d2ec6a19c2c0bddb5ae69fc59869c443b0d4dd7b668127`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:b2805c726caa7af5fe4e44a3ade5afbbb7f7c780567c147cb36b5c7a363464b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127722709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8b068ba5353d198e5fd7c34100da7ebc6771c257d75e23b80a211925de86aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:21:06 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:06 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:21:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:21:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:21:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:21:57 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:21:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e906a7a4ca515f29ae2f9d042b9d50795a7722dff0e54711609032ab009449`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa65ca376e03fed74f419a6a903362e83d6d4e1e1773ad67ad7183de7bbdf2`  
		Last Modified: Fri, 22 Apr 2022 02:26:26 GMT  
		Size: 89.8 MB (89815355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d48c43c28d400d613cd154b3e3182816a6e8b669d1fd7254e80bd5c51ae5f17`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b5541b27b08286050b0bfd633e5710b2273e67032af256ca1137c955ccbd51`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.3`

```console
$ docker pull mariadb@sha256:fac573c78b2030f062d8582c81d3fa2e30c0922ed0843e0c85c4ac85109868b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.3` - linux; amd64

```console
$ docker pull mariadb@sha256:c5cefb5639e0f9360734406cb0f8b7a119c29083705059a1c4509cf31b6f1dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1ace59b072bf4850281c7a3262a76f762ef97d774a38f5a5cddda9514dd811`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:30 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:30 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8f6c64a8fa57732c8eb3db48d751c40e0795aa5ca42f05d27c2e9ab31075bc`  
		Last Modified: Fri, 22 Apr 2022 02:55:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9817bd990fc72a53340f7dfdda9343811b5a6f4cbc914369c092d3994a044a`  
		Last Modified: Fri, 22 Apr 2022 02:55:56 GMT  
		Size: 88.7 MB (88741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14828b87067569c6589bb8a62987321b440e088af17c5e8a0163841f3bba2e26`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233be9bdce04aeae1b3a83158f299fccc9e8ef3535617d5ea40ebe5b9dcac8c6`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:796e80b1be01d8549f5371e79b763d8f1bdb8fb2c37530461322ab5e031ae6dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125720109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beee7eb5f13c4d5c9266d5f791bf31c0ff9e79d90e09676e681da928dd09d2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:00 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:01 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:02 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:37:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:37:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:37:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:37:36 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:37:37 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:37:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd363ec17eba0ec2199c03d0185e2f6c14475cf6ceaed83743eff2f224300830`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25985e8a9660011351be8031303461ef7750186d9ff4c5b1b5a8dea2c855099`  
		Last Modified: Tue, 05 Apr 2022 23:44:29 GMT  
		Size: 87.6 MB (87644090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e720e62a0b31078f92f2b1d0ec407f671a0ff9f556e60f0388dd0b58f49a78f`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a050689af938e8cc8c031932ce64cbfbe13f9f6d5163bb03e5dbb2ba4b412e2`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2dc8d6c759f7bab790ce8cbedf00108435005a6bd5372d6b8402309499bb624b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139538511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421f250d9d97c128e04a281415cbe3e56ea7ba80b2113a776c867ec9c0c91ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:55:13 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:21 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:28 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:34 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:55:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:00:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:00:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:00:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:00:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:00:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:00:38 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:00:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641d6fa031615e90c40a726e13fcfad279784e3095cb5743a622e154a01718eb`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b30ede638c309a8dbf803c86421dce897625fff4aeec32dc718921a25fec337`  
		Last Modified: Wed, 06 Apr 2022 06:27:41 GMT  
		Size: 93.3 MB (93323824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a7b909e1bbdb359c1ae0a294cbeda191102e8cd1149689143b7852ebb6317`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e2336774b01c630d2ec6a19c2c0bddb5ae69fc59869c443b0d4dd7b668127`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; s390x

```console
$ docker pull mariadb@sha256:b2805c726caa7af5fe4e44a3ade5afbbb7f7c780567c147cb36b5c7a363464b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127722709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8b068ba5353d198e5fd7c34100da7ebc6771c257d75e23b80a211925de86aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:21:06 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:06 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:21:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:21:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:21:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:21:57 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:21:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e906a7a4ca515f29ae2f9d042b9d50795a7722dff0e54711609032ab009449`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa65ca376e03fed74f419a6a903362e83d6d4e1e1773ad67ad7183de7bbdf2`  
		Last Modified: Fri, 22 Apr 2022 02:26:26 GMT  
		Size: 89.8 MB (89815355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d48c43c28d400d613cd154b3e3182816a6e8b669d1fd7254e80bd5c51ae5f17`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b5541b27b08286050b0bfd633e5710b2273e67032af256ca1137c955ccbd51`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.3-focal`

```console
$ docker pull mariadb@sha256:fac573c78b2030f062d8582c81d3fa2e30c0922ed0843e0c85c4ac85109868b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:c5cefb5639e0f9360734406cb0f8b7a119c29083705059a1c4509cf31b6f1dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1ace59b072bf4850281c7a3262a76f762ef97d774a38f5a5cddda9514dd811`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:30 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:30 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8f6c64a8fa57732c8eb3db48d751c40e0795aa5ca42f05d27c2e9ab31075bc`  
		Last Modified: Fri, 22 Apr 2022 02:55:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9817bd990fc72a53340f7dfdda9343811b5a6f4cbc914369c092d3994a044a`  
		Last Modified: Fri, 22 Apr 2022 02:55:56 GMT  
		Size: 88.7 MB (88741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14828b87067569c6589bb8a62987321b440e088af17c5e8a0163841f3bba2e26`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233be9bdce04aeae1b3a83158f299fccc9e8ef3535617d5ea40ebe5b9dcac8c6`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:796e80b1be01d8549f5371e79b763d8f1bdb8fb2c37530461322ab5e031ae6dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125720109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beee7eb5f13c4d5c9266d5f791bf31c0ff9e79d90e09676e681da928dd09d2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:00 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:01 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:02 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:37:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:37:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:37:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:37:36 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:37:37 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:37:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd363ec17eba0ec2199c03d0185e2f6c14475cf6ceaed83743eff2f224300830`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25985e8a9660011351be8031303461ef7750186d9ff4c5b1b5a8dea2c855099`  
		Last Modified: Tue, 05 Apr 2022 23:44:29 GMT  
		Size: 87.6 MB (87644090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e720e62a0b31078f92f2b1d0ec407f671a0ff9f556e60f0388dd0b58f49a78f`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a050689af938e8cc8c031932ce64cbfbe13f9f6d5163bb03e5dbb2ba4b412e2`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2dc8d6c759f7bab790ce8cbedf00108435005a6bd5372d6b8402309499bb624b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139538511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421f250d9d97c128e04a281415cbe3e56ea7ba80b2113a776c867ec9c0c91ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:55:13 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:21 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:28 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:34 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:55:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:00:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:00:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:00:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:00:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:00:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:00:38 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:00:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641d6fa031615e90c40a726e13fcfad279784e3095cb5743a622e154a01718eb`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b30ede638c309a8dbf803c86421dce897625fff4aeec32dc718921a25fec337`  
		Last Modified: Wed, 06 Apr 2022 06:27:41 GMT  
		Size: 93.3 MB (93323824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a7b909e1bbdb359c1ae0a294cbeda191102e8cd1149689143b7852ebb6317`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e2336774b01c630d2ec6a19c2c0bddb5ae69fc59869c443b0d4dd7b668127`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:b2805c726caa7af5fe4e44a3ade5afbbb7f7c780567c147cb36b5c7a363464b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127722709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8b068ba5353d198e5fd7c34100da7ebc6771c257d75e23b80a211925de86aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:21:06 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:06 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:21:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:21:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:21:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:21:57 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:21:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e906a7a4ca515f29ae2f9d042b9d50795a7722dff0e54711609032ab009449`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa65ca376e03fed74f419a6a903362e83d6d4e1e1773ad67ad7183de7bbdf2`  
		Last Modified: Fri, 22 Apr 2022 02:26:26 GMT  
		Size: 89.8 MB (89815355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d48c43c28d400d613cd154b3e3182816a6e8b669d1fd7254e80bd5c51ae5f17`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b5541b27b08286050b0bfd633e5710b2273e67032af256ca1137c955ccbd51`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-rc`

```console
$ docker pull mariadb@sha256:c85682a7c33528161d69e2638e95b11d0663bb83ad1ffea968e95c52cfb5739f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:6207f31973a665b4d1c9ba7ea7ac726adad41a661a549561fc671b44148ce330
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128578395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9732c0915d292a0e4f73669df378c84618d6492d687d02bd6217d4d3dff650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:50:32 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:50:32 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:50:32 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:50:32 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:50:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:50:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:02 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:02 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:02 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:03 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ba526ebec155d55cbb43daf63138efab1b47b098a037e64dd6acfcee49c6fd`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c3c04a1f7b4ecf07d5a5de05f17a2d0290974d190181a5f6a2533bde7931cf`  
		Last Modified: Fri, 22 Apr 2022 02:55:27 GMT  
		Size: 88.7 MB (88651923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8147174b3e651ed73d19ba9e151df9da5da3d253719e13ff39d98fb4f37b05b0`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e24d2b3f05313227b1155b461f451eac48ce5ae7c60d77d5cf22ed1c4bb2df9`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31cd6fe543073f235afe83c47cc6672073212098653f47f10f91366d0e460a3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125649619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c6c6bb8738a2aa3f90b104b05f382485c2ac7361ecc67c10fea5f8657a0e5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:36:14 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:36:15 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:36:16 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:36:17 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:36:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:36:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:36:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:36:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:36:49 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:36:50 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:36:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:36:51 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:36:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f56daf3efbe831b6f445daf75a6c8f34b982f81539d61e8092b59c0525f4cf`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699bbef151cad72b453529d69bb11b62cc613ea80fcc70c3e68ca864d15a199f`  
		Last Modified: Tue, 05 Apr 2022 23:43:58 GMT  
		Size: 87.6 MB (87573593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0dad28a4892729d8347da6ee8e68fc19df6be7479103b2e734ef79e3ba386`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98066ee1e8b00a2cd18d0f55329bcd394831d34e35f96aa67eaeff58fefab336`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b9e0f0d5e482843d284dce1d6187f77915024afc0b8a263320639a8d844ad927
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139620664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b799be0484c4ffbfa56e694f0f9d15890864f98507489cb4d3e22319af051647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:49:44 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 05:49:53 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 05:50:11 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 05:50:16 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 05:50:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:50:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 05:54:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 05:54:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 05:54:40 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 05:54:41 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:54:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:54:51 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 05:54:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa7b49a666543fca900b55550c381cf460a59c5e5ade24cc0af942d302e0745`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16172bf145415f0af93529ed2eb4c2173d6589161a67d29bd418bfffaa69951`  
		Last Modified: Wed, 06 Apr 2022 06:27:01 GMT  
		Size: 93.4 MB (93405974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ced70b615cb3106f7935f445957a07e6c2cb95d357dbf2b965e58930b4b418`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810a8ff779a339e295e8961100ad4d9e7c5c05a4cdc181683c41ebd437062a5`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:c76ca29aedf81817f5b5c44c74fba2d9205af851850c6faca87445755dc4c46b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127687683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbeceb483cce646f28db321c4f1654cbcf4ed40d444f3b830997f6972e491759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:19:52 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:19:52 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:19:53 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:19:53 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:19:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:19:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:20:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:20:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:20:49 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:20:50 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:20:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:20:51 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:20:51 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4ba62b910cb5597e9c0cd2021dfb695c794064eab1a7d836f0703ac7c9f4cd`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf8b985798f7ba131bf803d27319891e3ba63b1af55ec8b62db1774ba927065`  
		Last Modified: Fri, 22 Apr 2022 02:26:00 GMT  
		Size: 89.8 MB (89780333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9f4fbf77e6e3e22bf151c858b609c860735abe700df22f6df1e70d9442416`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5263367654b9b5be7517ca33c552026b40ea6536458d3bec38d908b4ded868`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-rc-focal`

```console
$ docker pull mariadb@sha256:c85682a7c33528161d69e2638e95b11d0663bb83ad1ffea968e95c52cfb5739f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-rc-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:6207f31973a665b4d1c9ba7ea7ac726adad41a661a549561fc671b44148ce330
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128578395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9732c0915d292a0e4f73669df378c84618d6492d687d02bd6217d4d3dff650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:50:32 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:50:32 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:50:32 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:50:32 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:50:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:50:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:02 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:02 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:02 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:03 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ba526ebec155d55cbb43daf63138efab1b47b098a037e64dd6acfcee49c6fd`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c3c04a1f7b4ecf07d5a5de05f17a2d0290974d190181a5f6a2533bde7931cf`  
		Last Modified: Fri, 22 Apr 2022 02:55:27 GMT  
		Size: 88.7 MB (88651923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8147174b3e651ed73d19ba9e151df9da5da3d253719e13ff39d98fb4f37b05b0`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e24d2b3f05313227b1155b461f451eac48ce5ae7c60d77d5cf22ed1c4bb2df9`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31cd6fe543073f235afe83c47cc6672073212098653f47f10f91366d0e460a3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125649619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c6c6bb8738a2aa3f90b104b05f382485c2ac7361ecc67c10fea5f8657a0e5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:36:14 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:36:15 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:36:16 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:36:17 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:36:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:36:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:36:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:36:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:36:49 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:36:50 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:36:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:36:51 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:36:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f56daf3efbe831b6f445daf75a6c8f34b982f81539d61e8092b59c0525f4cf`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699bbef151cad72b453529d69bb11b62cc613ea80fcc70c3e68ca864d15a199f`  
		Last Modified: Tue, 05 Apr 2022 23:43:58 GMT  
		Size: 87.6 MB (87573593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0dad28a4892729d8347da6ee8e68fc19df6be7479103b2e734ef79e3ba386`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98066ee1e8b00a2cd18d0f55329bcd394831d34e35f96aa67eaeff58fefab336`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b9e0f0d5e482843d284dce1d6187f77915024afc0b8a263320639a8d844ad927
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139620664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b799be0484c4ffbfa56e694f0f9d15890864f98507489cb4d3e22319af051647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:49:44 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 05:49:53 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 05:50:11 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 05:50:16 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 05:50:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:50:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 05:54:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 05:54:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 05:54:40 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 05:54:41 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:54:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:54:51 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 05:54:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa7b49a666543fca900b55550c381cf460a59c5e5ade24cc0af942d302e0745`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16172bf145415f0af93529ed2eb4c2173d6589161a67d29bd418bfffaa69951`  
		Last Modified: Wed, 06 Apr 2022 06:27:01 GMT  
		Size: 93.4 MB (93405974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ced70b615cb3106f7935f445957a07e6c2cb95d357dbf2b965e58930b4b418`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810a8ff779a339e295e8961100ad4d9e7c5c05a4cdc181683c41ebd437062a5`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:c76ca29aedf81817f5b5c44c74fba2d9205af851850c6faca87445755dc4c46b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127687683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbeceb483cce646f28db321c4f1654cbcf4ed40d444f3b830997f6972e491759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:19:52 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:19:52 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:19:53 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:19:53 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:19:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:19:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:20:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:20:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:20:49 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:20:50 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:20:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:20:51 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:20:51 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4ba62b910cb5597e9c0cd2021dfb695c794064eab1a7d836f0703ac7c9f4cd`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf8b985798f7ba131bf803d27319891e3ba63b1af55ec8b62db1774ba927065`  
		Last Modified: Fri, 22 Apr 2022 02:26:00 GMT  
		Size: 89.8 MB (89780333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9f4fbf77e6e3e22bf151c858b609c860735abe700df22f6df1e70d9442416`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5263367654b9b5be7517ca33c552026b40ea6536458d3bec38d908b4ded868`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.2-rc`

```console
$ docker pull mariadb@sha256:c85682a7c33528161d69e2638e95b11d0663bb83ad1ffea968e95c52cfb5739f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.2-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:6207f31973a665b4d1c9ba7ea7ac726adad41a661a549561fc671b44148ce330
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128578395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9732c0915d292a0e4f73669df378c84618d6492d687d02bd6217d4d3dff650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:50:32 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:50:32 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:50:32 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:50:32 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:50:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:50:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:02 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:02 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:02 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:03 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ba526ebec155d55cbb43daf63138efab1b47b098a037e64dd6acfcee49c6fd`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c3c04a1f7b4ecf07d5a5de05f17a2d0290974d190181a5f6a2533bde7931cf`  
		Last Modified: Fri, 22 Apr 2022 02:55:27 GMT  
		Size: 88.7 MB (88651923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8147174b3e651ed73d19ba9e151df9da5da3d253719e13ff39d98fb4f37b05b0`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e24d2b3f05313227b1155b461f451eac48ce5ae7c60d77d5cf22ed1c4bb2df9`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31cd6fe543073f235afe83c47cc6672073212098653f47f10f91366d0e460a3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125649619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c6c6bb8738a2aa3f90b104b05f382485c2ac7361ecc67c10fea5f8657a0e5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:36:14 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:36:15 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:36:16 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:36:17 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:36:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:36:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:36:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:36:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:36:49 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:36:50 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:36:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:36:51 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:36:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f56daf3efbe831b6f445daf75a6c8f34b982f81539d61e8092b59c0525f4cf`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699bbef151cad72b453529d69bb11b62cc613ea80fcc70c3e68ca864d15a199f`  
		Last Modified: Tue, 05 Apr 2022 23:43:58 GMT  
		Size: 87.6 MB (87573593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0dad28a4892729d8347da6ee8e68fc19df6be7479103b2e734ef79e3ba386`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98066ee1e8b00a2cd18d0f55329bcd394831d34e35f96aa67eaeff58fefab336`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b9e0f0d5e482843d284dce1d6187f77915024afc0b8a263320639a8d844ad927
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139620664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b799be0484c4ffbfa56e694f0f9d15890864f98507489cb4d3e22319af051647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:49:44 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 05:49:53 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 05:50:11 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 05:50:16 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 05:50:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:50:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 05:54:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 05:54:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 05:54:40 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 05:54:41 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:54:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:54:51 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 05:54:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa7b49a666543fca900b55550c381cf460a59c5e5ade24cc0af942d302e0745`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16172bf145415f0af93529ed2eb4c2173d6589161a67d29bd418bfffaa69951`  
		Last Modified: Wed, 06 Apr 2022 06:27:01 GMT  
		Size: 93.4 MB (93405974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ced70b615cb3106f7935f445957a07e6c2cb95d357dbf2b965e58930b4b418`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810a8ff779a339e295e8961100ad4d9e7c5c05a4cdc181683c41ebd437062a5`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:c76ca29aedf81817f5b5c44c74fba2d9205af851850c6faca87445755dc4c46b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127687683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbeceb483cce646f28db321c4f1654cbcf4ed40d444f3b830997f6972e491759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:19:52 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:19:52 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:19:53 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:19:53 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:19:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:19:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:20:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:20:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:20:49 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:20:50 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:20:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:20:51 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:20:51 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4ba62b910cb5597e9c0cd2021dfb695c794064eab1a7d836f0703ac7c9f4cd`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf8b985798f7ba131bf803d27319891e3ba63b1af55ec8b62db1774ba927065`  
		Last Modified: Fri, 22 Apr 2022 02:26:00 GMT  
		Size: 89.8 MB (89780333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9f4fbf77e6e3e22bf151c858b609c860735abe700df22f6df1e70d9442416`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5263367654b9b5be7517ca33c552026b40ea6536458d3bec38d908b4ded868`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.2-rc-focal`

```console
$ docker pull mariadb@sha256:c85682a7c33528161d69e2638e95b11d0663bb83ad1ffea968e95c52cfb5739f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.2-rc-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:6207f31973a665b4d1c9ba7ea7ac726adad41a661a549561fc671b44148ce330
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128578395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9732c0915d292a0e4f73669df378c84618d6492d687d02bd6217d4d3dff650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:50:32 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:50:32 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:50:32 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:50:32 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:50:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:50:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:02 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:02 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:02 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:03 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ba526ebec155d55cbb43daf63138efab1b47b098a037e64dd6acfcee49c6fd`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c3c04a1f7b4ecf07d5a5de05f17a2d0290974d190181a5f6a2533bde7931cf`  
		Last Modified: Fri, 22 Apr 2022 02:55:27 GMT  
		Size: 88.7 MB (88651923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8147174b3e651ed73d19ba9e151df9da5da3d253719e13ff39d98fb4f37b05b0`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e24d2b3f05313227b1155b461f451eac48ce5ae7c60d77d5cf22ed1c4bb2df9`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31cd6fe543073f235afe83c47cc6672073212098653f47f10f91366d0e460a3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125649619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c6c6bb8738a2aa3f90b104b05f382485c2ac7361ecc67c10fea5f8657a0e5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:36:14 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:36:15 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:36:16 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:36:17 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:36:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:36:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:36:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:36:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:36:49 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:36:50 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:36:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:36:51 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:36:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f56daf3efbe831b6f445daf75a6c8f34b982f81539d61e8092b59c0525f4cf`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699bbef151cad72b453529d69bb11b62cc613ea80fcc70c3e68ca864d15a199f`  
		Last Modified: Tue, 05 Apr 2022 23:43:58 GMT  
		Size: 87.6 MB (87573593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0dad28a4892729d8347da6ee8e68fc19df6be7479103b2e734ef79e3ba386`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98066ee1e8b00a2cd18d0f55329bcd394831d34e35f96aa67eaeff58fefab336`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b9e0f0d5e482843d284dce1d6187f77915024afc0b8a263320639a8d844ad927
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139620664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b799be0484c4ffbfa56e694f0f9d15890864f98507489cb4d3e22319af051647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:49:44 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 05:49:53 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 05:50:11 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 05:50:16 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 05:50:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:50:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 05:54:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 05:54:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 05:54:40 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 05:54:41 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:54:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:54:51 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 05:54:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa7b49a666543fca900b55550c381cf460a59c5e5ade24cc0af942d302e0745`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16172bf145415f0af93529ed2eb4c2173d6589161a67d29bd418bfffaa69951`  
		Last Modified: Wed, 06 Apr 2022 06:27:01 GMT  
		Size: 93.4 MB (93405974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ced70b615cb3106f7935f445957a07e6c2cb95d357dbf2b965e58930b4b418`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810a8ff779a339e295e8961100ad4d9e7c5c05a4cdc181683c41ebd437062a5`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:c76ca29aedf81817f5b5c44c74fba2d9205af851850c6faca87445755dc4c46b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127687683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbeceb483cce646f28db321c4f1654cbcf4ed40d444f3b830997f6972e491759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:19:52 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:19:52 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 22 Apr 2022 02:19:53 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:19:53 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 22 Apr 2022 02:19:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:19:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:20:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:20:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:20:49 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:20:50 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:20:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:20:51 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:20:51 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4ba62b910cb5597e9c0cd2021dfb695c794064eab1a7d836f0703ac7c9f4cd`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf8b985798f7ba131bf803d27319891e3ba63b1af55ec8b62db1774ba927065`  
		Last Modified: Fri, 22 Apr 2022 02:26:00 GMT  
		Size: 89.8 MB (89780333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9f4fbf77e6e3e22bf151c858b609c860735abe700df22f6df1e70d9442416`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5263367654b9b5be7517ca33c552026b40ea6536458d3bec38d908b4ded868`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:fac573c78b2030f062d8582c81d3fa2e30c0922ed0843e0c85c4ac85109868b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:c5cefb5639e0f9360734406cb0f8b7a119c29083705059a1c4509cf31b6f1dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1ace59b072bf4850281c7a3262a76f762ef97d774a38f5a5cddda9514dd811`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:30 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:30 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8f6c64a8fa57732c8eb3db48d751c40e0795aa5ca42f05d27c2e9ab31075bc`  
		Last Modified: Fri, 22 Apr 2022 02:55:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9817bd990fc72a53340f7dfdda9343811b5a6f4cbc914369c092d3994a044a`  
		Last Modified: Fri, 22 Apr 2022 02:55:56 GMT  
		Size: 88.7 MB (88741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14828b87067569c6589bb8a62987321b440e088af17c5e8a0163841f3bba2e26`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233be9bdce04aeae1b3a83158f299fccc9e8ef3535617d5ea40ebe5b9dcac8c6`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:796e80b1be01d8549f5371e79b763d8f1bdb8fb2c37530461322ab5e031ae6dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125720109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beee7eb5f13c4d5c9266d5f791bf31c0ff9e79d90e09676e681da928dd09d2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:00 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:01 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:02 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:37:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:37:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:37:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:37:36 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:37:37 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:37:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd363ec17eba0ec2199c03d0185e2f6c14475cf6ceaed83743eff2f224300830`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25985e8a9660011351be8031303461ef7750186d9ff4c5b1b5a8dea2c855099`  
		Last Modified: Tue, 05 Apr 2022 23:44:29 GMT  
		Size: 87.6 MB (87644090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e720e62a0b31078f92f2b1d0ec407f671a0ff9f556e60f0388dd0b58f49a78f`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a050689af938e8cc8c031932ce64cbfbe13f9f6d5163bb03e5dbb2ba4b412e2`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2dc8d6c759f7bab790ce8cbedf00108435005a6bd5372d6b8402309499bb624b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139538511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421f250d9d97c128e04a281415cbe3e56ea7ba80b2113a776c867ec9c0c91ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:55:13 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:21 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:28 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:34 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:55:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:00:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:00:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:00:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:00:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:00:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:00:38 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:00:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641d6fa031615e90c40a726e13fcfad279784e3095cb5743a622e154a01718eb`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b30ede638c309a8dbf803c86421dce897625fff4aeec32dc718921a25fec337`  
		Last Modified: Wed, 06 Apr 2022 06:27:41 GMT  
		Size: 93.3 MB (93323824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a7b909e1bbdb359c1ae0a294cbeda191102e8cd1149689143b7852ebb6317`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e2336774b01c630d2ec6a19c2c0bddb5ae69fc59869c443b0d4dd7b668127`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; s390x

```console
$ docker pull mariadb@sha256:b2805c726caa7af5fe4e44a3ade5afbbb7f7c780567c147cb36b5c7a363464b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127722709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8b068ba5353d198e5fd7c34100da7ebc6771c257d75e23b80a211925de86aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:21:06 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:06 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:21:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:21:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:21:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:21:57 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:21:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e906a7a4ca515f29ae2f9d042b9d50795a7722dff0e54711609032ab009449`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa65ca376e03fed74f419a6a903362e83d6d4e1e1773ad67ad7183de7bbdf2`  
		Last Modified: Fri, 22 Apr 2022 02:26:26 GMT  
		Size: 89.8 MB (89815355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d48c43c28d400d613cd154b3e3182816a6e8b669d1fd7254e80bd5c51ae5f17`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b5541b27b08286050b0bfd633e5710b2273e67032af256ca1137c955ccbd51`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:fac573c78b2030f062d8582c81d3fa2e30c0922ed0843e0c85c4ac85109868b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:c5cefb5639e0f9360734406cb0f8b7a119c29083705059a1c4509cf31b6f1dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1ace59b072bf4850281c7a3262a76f762ef97d774a38f5a5cddda9514dd811`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:49:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:50:11 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:50:23 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:50:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:50:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:50:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:51:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:51:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:51:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:51:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:51:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:51:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:51:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:51:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:51:30 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:51:30 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c31fd2b56f53ff5ba5ad5d21b9b28fa703a2f00ba36f7eb46f2d33b5990991`  
		Last Modified: Fri, 22 Apr 2022 02:55:18 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b74a4775214476da7b0f4c35eca591deb95c8bc63302ab6f9e683bdf27c64`  
		Last Modified: Fri, 22 Apr 2022 02:55:17 GMT  
		Size: 5.5 MB (5488530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9826fce863ca3c5d0aba036e072e4d8e223bed29a3a7c69e257e9e8041343`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 3.6 MB (3584958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c55a00590e4f6368ec1f193c5ed403478245d2a7a10d09e41ed70caee085a0`  
		Last Modified: Fri, 22 Apr 2022 02:55:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc07b7e87bb4284714b6d047b39b0b5f4e21fec8aae18c882caaf0224049425c`  
		Last Modified: Fri, 22 Apr 2022 02:55:16 GMT  
		Size: 2.3 MB (2272009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf1a0d04d7cbb85b720ddc123637c146ca65878e7c24c71b738588d5ab9b1`  
		Last Modified: Fri, 22 Apr 2022 02:55:13 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8f6c64a8fa57732c8eb3db48d751c40e0795aa5ca42f05d27c2e9ab31075bc`  
		Last Modified: Fri, 22 Apr 2022 02:55:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9817bd990fc72a53340f7dfdda9343811b5a6f4cbc914369c092d3994a044a`  
		Last Modified: Fri, 22 Apr 2022 02:55:56 GMT  
		Size: 88.7 MB (88741666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14828b87067569c6589bb8a62987321b440e088af17c5e8a0163841f3bba2e26`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233be9bdce04aeae1b3a83158f299fccc9e8ef3535617d5ea40ebe5b9dcac8c6`  
		Last Modified: Fri, 22 Apr 2022 02:55:42 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:796e80b1be01d8549f5371e79b763d8f1bdb8fb2c37530461322ab5e031ae6dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125720109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beee7eb5f13c4d5c9266d5f791bf31c0ff9e79d90e09676e681da928dd09d2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:35:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:35:45 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:35:46 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:36:02 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:36:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:36:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:36:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:37:00 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:01 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:37:02 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:03 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:37:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:37:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:37:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:37:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:37:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:37:36 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:37:37 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:37:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aeff3983d331dab896639b0075392defb2c2f3213392f7dfdd6e66a191138a`  
		Last Modified: Tue, 05 Apr 2022 23:43:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f67acd5c529c3a4def5e56ffaf9ddf9444a3d36fcae6983e21a750d011c45`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 5.3 MB (5320011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d2eb0ba121cbbe785f2c5ac88f394d9753bd19f03cbe6f279b8b157f3b31a`  
		Last Modified: Tue, 05 Apr 2022 23:43:48 GMT  
		Size: 3.4 MB (3369725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13bb612b0140e72c928bac602f32ca20814af531ebd3aef1f6252a51792f60d`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a3a6d81793ce0a47c670d0f157a7a8815e74a70fbfde1a000cd4685617388`  
		Last Modified: Tue, 05 Apr 2022 23:43:47 GMT  
		Size: 2.2 MB (2201995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8127165a089e214f746178a1219245b9b4ae06c7a379f9c4b26194319cee19`  
		Last Modified: Tue, 05 Apr 2022 23:43:45 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd363ec17eba0ec2199c03d0185e2f6c14475cf6ceaed83743eff2f224300830`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25985e8a9660011351be8031303461ef7750186d9ff4c5b1b5a8dea2c855099`  
		Last Modified: Tue, 05 Apr 2022 23:44:29 GMT  
		Size: 87.6 MB (87644090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e720e62a0b31078f92f2b1d0ec407f671a0ff9f556e60f0388dd0b58f49a78f`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a050689af938e8cc8c031932ce64cbfbe13f9f6d5163bb03e5dbb2ba4b412e2`  
		Last Modified: Tue, 05 Apr 2022 23:44:16 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2dc8d6c759f7bab790ce8cbedf00108435005a6bd5372d6b8402309499bb624b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139538511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421f250d9d97c128e04a281415cbe3e56ea7ba80b2113a776c867ec9c0c91ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:45:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 05:46:56 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:47:00 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 05:48:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 05:49:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:49:22 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 05:49:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 05:55:13 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:21 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 05:55:28 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:34 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 05:55:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 05:55:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 06:00:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 06:00:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 06:00:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 06:00:25 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 06:00:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 06:00:38 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 06:00:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512fe19a54fae6f6f48b7c07bece6ca69fd7791d6eecd9ace7c2522a78a1026c`  
		Last Modified: Wed, 06 Apr 2022 06:26:51 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7ffd744b571919d68a83dbabef9478292b81785bc9b2c48fdd069a7c8fd4d`  
		Last Modified: Wed, 06 Apr 2022 06:26:49 GMT  
		Size: 6.7 MB (6667357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54ecf983b6f86c5413fec94304c5a25733dd40f05259165ef70993070b1e3e9`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 3.7 MB (3672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe55abcea2621200e796441693c923102240368c670225582a36aacbc70f0`  
		Last Modified: Wed, 06 Apr 2022 06:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1980158f5bdf68e3aa2bfca9ddba8341f801ddc5a9da7570d68018d5a2dcebd`  
		Last Modified: Wed, 06 Apr 2022 06:26:48 GMT  
		Size: 2.6 MB (2568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b2466e25100e6186fcc76286ded72a2a31ecd230076353975325326b15124`  
		Last Modified: Wed, 06 Apr 2022 06:26:43 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641d6fa031615e90c40a726e13fcfad279784e3095cb5743a622e154a01718eb`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b30ede638c309a8dbf803c86421dce897625fff4aeec32dc718921a25fec337`  
		Last Modified: Wed, 06 Apr 2022 06:27:41 GMT  
		Size: 93.3 MB (93323824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a7b909e1bbdb359c1ae0a294cbeda191102e8cd1149689143b7852ebb6317`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e2336774b01c630d2ec6a19c2c0bddb5ae69fc59869c443b0d4dd7b668127`  
		Last Modified: Wed, 06 Apr 2022 06:27:23 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:b2805c726caa7af5fe4e44a3ade5afbbb7f7c780567c147cb36b5c7a363464b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127722709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8b068ba5353d198e5fd7c34100da7ebc6771c257d75e23b80a211925de86aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:19:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 22 Apr 2022 02:19:18 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 22 Apr 2022 02:19:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 22 Apr 2022 02:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 Apr 2022 02:19:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 22 Apr 2022 02:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Fri, 22 Apr 2022 02:21:06 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:06 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 22 Apr 2022 02:21:07 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 22 Apr 2022 02:21:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 22 Apr 2022 02:21:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 22 Apr 2022 02:21:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 22 Apr 2022 02:21:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 22 Apr 2022 02:21:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 22 Apr 2022 02:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 02:21:57 GMT
EXPOSE 3306
# Fri, 22 Apr 2022 02:21:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc8f5833a8cfe0537845df0a5d311b211ef889ed5d5e12ace1bd3eb30834c6`  
		Last Modified: Fri, 22 Apr 2022 02:25:50 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f4186175df1fdbe352452d13a8d94670ff3446432648e7b163e9a1c6a94d88`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 5.4 MB (5378760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea503bea58815ffe61d67ad911ffab94ad5a57e364db2126c3cb11e8f732d37`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 3.2 MB (3244218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb02e31628a4e2997c0f38de59eb7d09325086dd65b6b511c1e63c7fdd1692`  
		Last Modified: Fri, 22 Apr 2022 02:25:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da960e123e0d72767a541ecf7347f03dfad9502e82a54cd713eb6c1e2d294b`  
		Last Modified: Fri, 22 Apr 2022 02:25:49 GMT  
		Size: 2.2 MB (2183672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ddf5cdd828e8ea2c4c69fedbb30d4aebf50bbc1c279fae4855faec077ae98`  
		Last Modified: Fri, 22 Apr 2022 02:25:47 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e906a7a4ca515f29ae2f9d042b9d50795a7722dff0e54711609032ab009449`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa65ca376e03fed74f419a6a903362e83d6d4e1e1773ad67ad7183de7bbdf2`  
		Last Modified: Fri, 22 Apr 2022 02:26:26 GMT  
		Size: 89.8 MB (89815355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d48c43c28d400d613cd154b3e3182816a6e8b669d1fd7254e80bd5c51ae5f17`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b5541b27b08286050b0bfd633e5710b2273e67032af256ca1137c955ccbd51`  
		Last Modified: Fri, 22 Apr 2022 02:26:13 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
