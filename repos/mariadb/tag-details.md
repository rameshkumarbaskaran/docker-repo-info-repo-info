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
$ docker pull mariadb@sha256:e4421edf721f25823f7a867b231a3b41dda67fcc219ad489a5f646c1f2f8a729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:364e6c38ee64f7f961cc1b70d5c31e554754c4a9fcd6516c9b5c31accf134e61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100166b773f8bdb6f5bfcd16a5ae670bc02ec8a0b6f52f6f74cc560aad592fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ef26c44d0008a5eaeb76320f9509d0728c66ee924af3909910b9e9c8d062`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f6e068c19c3abd463f2e8818220f4304558532ce1eea0ba7e88249533a3de2`  
		Last Modified: Wed, 06 Apr 2022 01:54:00 GMT  
		Size: 88.7 MB (88741687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd25d3e0e6be214d9c5ca5d3597275c41c80a9a551f7aef80ddd34f5f41140`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e322e4875b51e5cf140539cccf19a26d235f52baae4c7cc88024a59f599fe`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 6.8 KB (6775 bytes)  
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
$ docker pull mariadb@sha256:73f1a363d1bd5d67665a2e95e281a6c5f9d60cfc954d37bcc543f4323ea16cb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139540029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3073063783d6646d082607b57b7093f8c0726cc621b6b59d5852a14441fc89b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:39 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2f383467f58f976dd982b1bc6e6fff20f589e60b19d6e00b2a84d8b95c1a7`  
		Last Modified: Fri, 01 Apr 2022 17:29:04 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; s390x

```console
$ docker pull mariadb@sha256:2c2eb9a9fa59f3ddae7a55bd0ddf77e246352438463824741eb92a6a347697e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127721348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5405ba6fc8203440741f811f94a5463c814b05cb550bca60b138a06c6605527b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:31:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8a3bf7f3897df0dfedf0c9629a9a933240987145b59678a8d0d26fac2722de`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2029403953732bae90490466205f4c53ff7e048f32f70a2cbab8d2e089984ded`  
		Last Modified: Tue, 05 Apr 2022 23:34:25 GMT  
		Size: 89.8 MB (89815166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc5f84bad71845209754dbd765377f1bbe548ba402569ff98b4f69425f4f93`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f2fd91a171567a326fb6c302b2a10ac5003b1e43c94400e96a1613d65915f`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:e4421edf721f25823f7a867b231a3b41dda67fcc219ad489a5f646c1f2f8a729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:364e6c38ee64f7f961cc1b70d5c31e554754c4a9fcd6516c9b5c31accf134e61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100166b773f8bdb6f5bfcd16a5ae670bc02ec8a0b6f52f6f74cc560aad592fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ef26c44d0008a5eaeb76320f9509d0728c66ee924af3909910b9e9c8d062`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f6e068c19c3abd463f2e8818220f4304558532ce1eea0ba7e88249533a3de2`  
		Last Modified: Wed, 06 Apr 2022 01:54:00 GMT  
		Size: 88.7 MB (88741687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd25d3e0e6be214d9c5ca5d3597275c41c80a9a551f7aef80ddd34f5f41140`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e322e4875b51e5cf140539cccf19a26d235f52baae4c7cc88024a59f599fe`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 6.8 KB (6775 bytes)  
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
$ docker pull mariadb@sha256:73f1a363d1bd5d67665a2e95e281a6c5f9d60cfc954d37bcc543f4323ea16cb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139540029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3073063783d6646d082607b57b7093f8c0726cc621b6b59d5852a14441fc89b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:39 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2f383467f58f976dd982b1bc6e6fff20f589e60b19d6e00b2a84d8b95c1a7`  
		Last Modified: Fri, 01 Apr 2022 17:29:04 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:2c2eb9a9fa59f3ddae7a55bd0ddf77e246352438463824741eb92a6a347697e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127721348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5405ba6fc8203440741f811f94a5463c814b05cb550bca60b138a06c6605527b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:31:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8a3bf7f3897df0dfedf0c9629a9a933240987145b59678a8d0d26fac2722de`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2029403953732bae90490466205f4c53ff7e048f32f70a2cbab8d2e089984ded`  
		Last Modified: Tue, 05 Apr 2022 23:34:25 GMT  
		Size: 89.8 MB (89815166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc5f84bad71845209754dbd765377f1bbe548ba402569ff98b4f69425f4f93`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f2fd91a171567a326fb6c302b2a10ac5003b1e43c94400e96a1613d65915f`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:d28588e5e7f3abcf5a8e364baaf497675f6c7c7fdde3d6dbebc127f80e78cc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:bae1af3a9ab7d216a21591bcf4524263edd1c820915e679ae1553d517934992e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109315419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8f3a60883793bbf979c342242c10343081b11d7898a2375b23ea64d51ec981`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:11:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:11:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:11:30 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:11:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:11:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:11:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:11:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:11:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:11:53 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 00:11:53 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 00:11:53 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 00:11:53 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 00:11:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Wed, 06 Apr 2022 00:11:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:12:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:12:27 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:12:27 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:12:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:12:28 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229eef75b67b318b8c76eb00e60e1aa7b2ebdfaf759f30a88e4c49fa36eb8648`  
		Last Modified: Wed, 06 Apr 2022 01:56:38 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfaf091f1fb44dbaf7f7e2ef64b08b4bbd721bb85efa1a6873f59363a3c00ac`  
		Last Modified: Wed, 06 Apr 2022 01:56:39 GMT  
		Size: 4.8 MB (4813215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ced99642795c1758efcd44723e438622b236ca8059747078a7b449b66d8b84`  
		Last Modified: Wed, 06 Apr 2022 01:56:37 GMT  
		Size: 3.6 MB (3553168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71e962c603d015aefc6871e1e17a5dbe314e7265562820bf1513ec83e935ad3`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388953686a88dd1fb56b5fc8f2e77d4a8572a8217ddcae794f50ab5022a206c`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 1.6 MB (1583440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6b130a76ec2bbd10f45727c92bf7833e510d58070d6ed730dd8fe5364d449`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 5.2 KB (5167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ce2f4c12c6653d03e939b29fe301973ce8589b549c9f76b1fdefa99a55ab50`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98b2cb6250231ed8cef6de96815e140e12ba409d091fb57ee1adfe2c289ad9b`  
		Last Modified: Wed, 06 Apr 2022 01:56:44 GMT  
		Size: 72.6 MB (72638754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5bbf2fe5aa655e9cf36beac127786eecb56097e4ab21bab76154f593fbf97`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59159102a72740462897aeaabf19c0152976db3874fde7f09b268b45a5ad992`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aad673b55427fd9d7f8ca33f31eeaec2f327fc06001f88d0be4f4138a3576fb`  
		Last Modified: Wed, 06 Apr 2022 01:56:34 GMT  
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
$ docker pull mariadb@sha256:bb15b05ff6a038ff3d8c6c487fc01dd544054a09d8418fa112f808bca23d676e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133b521439e19cf4bbc797a82404d5f1283beeefe84f1036b229ac3b505dac05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:18:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:19:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:19:44 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:20:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:20:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:20:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:20:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:21:29 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:30 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:32 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:34 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 21:21:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:23:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:26:45 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:27:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:27:12 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:27:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee36c86f28b3454fed4c8ac5e091c4599123141b97f4c2d06bcaacef3db2ea7`  
		Last Modified: Sat, 19 Mar 2022 21:29:40 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b3bdd7509a19317e5839d95ede6349efc532222db47bead436a5c7b050e85d`  
		Last Modified: Sat, 19 Mar 2022 21:29:47 GMT  
		Size: 5.6 MB (5630211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2784f406f140da871c18b0b6482e18de484e2d4827fa0216dc1ec8e3ef8aa513`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 3.5 MB (3533413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4aba83fb5ef3f7de5b84459fc4721d07fc86c85e606c13347570174773185`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413573cd9619e1f71e4549da75acfb8c299766f9215e8130a557954f9c25519`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 1.9 MB (1936744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c31864f49567b8a3f7e571d3f5d2108c556425e17d0ff91b78c295eba74dbb`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d85e8ff6d332e09313c616b10d030e5694a52436cec84ca1b53f9c3da9ed25e`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96fd22c02287002999574e230adbefacaa56d0f60bbd6ff87906f6d459676e6`  
		Last Modified: Sat, 19 Mar 2022 21:29:49 GMT  
		Size: 76.2 MB (76158819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cb5401efa11b07ec297c948ccf553be601e0b23eb71e7ed7a14d936994735a`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332eb5bb646168f2ec0c2a411da4f710fcf0fb0693ca1a44859b0403433add2a`  
		Last Modified: Fri, 01 Apr 2022 17:31:05 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19a0a3d27ec087cd94fa80a0d3ea7dd913131fa244ccb6abadb6a2e5f80b29a`  
		Last Modified: Fri, 01 Apr 2022 17:31:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:d28588e5e7f3abcf5a8e364baaf497675f6c7c7fdde3d6dbebc127f80e78cc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:bae1af3a9ab7d216a21591bcf4524263edd1c820915e679ae1553d517934992e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109315419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8f3a60883793bbf979c342242c10343081b11d7898a2375b23ea64d51ec981`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:11:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:11:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:11:30 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:11:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:11:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:11:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:11:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:11:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:11:53 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 00:11:53 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 00:11:53 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 00:11:53 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 00:11:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Wed, 06 Apr 2022 00:11:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:12:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:12:27 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:12:27 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:12:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:12:28 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229eef75b67b318b8c76eb00e60e1aa7b2ebdfaf759f30a88e4c49fa36eb8648`  
		Last Modified: Wed, 06 Apr 2022 01:56:38 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfaf091f1fb44dbaf7f7e2ef64b08b4bbd721bb85efa1a6873f59363a3c00ac`  
		Last Modified: Wed, 06 Apr 2022 01:56:39 GMT  
		Size: 4.8 MB (4813215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ced99642795c1758efcd44723e438622b236ca8059747078a7b449b66d8b84`  
		Last Modified: Wed, 06 Apr 2022 01:56:37 GMT  
		Size: 3.6 MB (3553168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71e962c603d015aefc6871e1e17a5dbe314e7265562820bf1513ec83e935ad3`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388953686a88dd1fb56b5fc8f2e77d4a8572a8217ddcae794f50ab5022a206c`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 1.6 MB (1583440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6b130a76ec2bbd10f45727c92bf7833e510d58070d6ed730dd8fe5364d449`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 5.2 KB (5167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ce2f4c12c6653d03e939b29fe301973ce8589b549c9f76b1fdefa99a55ab50`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98b2cb6250231ed8cef6de96815e140e12ba409d091fb57ee1adfe2c289ad9b`  
		Last Modified: Wed, 06 Apr 2022 01:56:44 GMT  
		Size: 72.6 MB (72638754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5bbf2fe5aa655e9cf36beac127786eecb56097e4ab21bab76154f593fbf97`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59159102a72740462897aeaabf19c0152976db3874fde7f09b268b45a5ad992`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aad673b55427fd9d7f8ca33f31eeaec2f327fc06001f88d0be4f4138a3576fb`  
		Last Modified: Wed, 06 Apr 2022 01:56:34 GMT  
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
$ docker pull mariadb@sha256:bb15b05ff6a038ff3d8c6c487fc01dd544054a09d8418fa112f808bca23d676e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133b521439e19cf4bbc797a82404d5f1283beeefe84f1036b229ac3b505dac05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:18:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:19:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:19:44 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:20:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:20:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:20:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:20:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:21:29 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:30 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:32 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:34 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 21:21:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:23:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:26:45 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:27:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:27:12 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:27:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee36c86f28b3454fed4c8ac5e091c4599123141b97f4c2d06bcaacef3db2ea7`  
		Last Modified: Sat, 19 Mar 2022 21:29:40 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b3bdd7509a19317e5839d95ede6349efc532222db47bead436a5c7b050e85d`  
		Last Modified: Sat, 19 Mar 2022 21:29:47 GMT  
		Size: 5.6 MB (5630211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2784f406f140da871c18b0b6482e18de484e2d4827fa0216dc1ec8e3ef8aa513`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 3.5 MB (3533413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4aba83fb5ef3f7de5b84459fc4721d07fc86c85e606c13347570174773185`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413573cd9619e1f71e4549da75acfb8c299766f9215e8130a557954f9c25519`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 1.9 MB (1936744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c31864f49567b8a3f7e571d3f5d2108c556425e17d0ff91b78c295eba74dbb`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d85e8ff6d332e09313c616b10d030e5694a52436cec84ca1b53f9c3da9ed25e`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96fd22c02287002999574e230adbefacaa56d0f60bbd6ff87906f6d459676e6`  
		Last Modified: Sat, 19 Mar 2022 21:29:49 GMT  
		Size: 76.2 MB (76158819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cb5401efa11b07ec297c948ccf553be601e0b23eb71e7ed7a14d936994735a`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332eb5bb646168f2ec0c2a411da4f710fcf0fb0693ca1a44859b0403433add2a`  
		Last Modified: Fri, 01 Apr 2022 17:31:05 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19a0a3d27ec087cd94fa80a0d3ea7dd913131fa244ccb6abadb6a2e5f80b29a`  
		Last Modified: Fri, 01 Apr 2022 17:31:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.43`

```console
$ docker pull mariadb@sha256:d28588e5e7f3abcf5a8e364baaf497675f6c7c7fdde3d6dbebc127f80e78cc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.43` - linux; amd64

```console
$ docker pull mariadb@sha256:bae1af3a9ab7d216a21591bcf4524263edd1c820915e679ae1553d517934992e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109315419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8f3a60883793bbf979c342242c10343081b11d7898a2375b23ea64d51ec981`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:11:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:11:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:11:30 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:11:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:11:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:11:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:11:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:11:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:11:53 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 00:11:53 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 00:11:53 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 00:11:53 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 00:11:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Wed, 06 Apr 2022 00:11:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:12:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:12:27 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:12:27 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:12:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:12:28 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229eef75b67b318b8c76eb00e60e1aa7b2ebdfaf759f30a88e4c49fa36eb8648`  
		Last Modified: Wed, 06 Apr 2022 01:56:38 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfaf091f1fb44dbaf7f7e2ef64b08b4bbd721bb85efa1a6873f59363a3c00ac`  
		Last Modified: Wed, 06 Apr 2022 01:56:39 GMT  
		Size: 4.8 MB (4813215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ced99642795c1758efcd44723e438622b236ca8059747078a7b449b66d8b84`  
		Last Modified: Wed, 06 Apr 2022 01:56:37 GMT  
		Size: 3.6 MB (3553168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71e962c603d015aefc6871e1e17a5dbe314e7265562820bf1513ec83e935ad3`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388953686a88dd1fb56b5fc8f2e77d4a8572a8217ddcae794f50ab5022a206c`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 1.6 MB (1583440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6b130a76ec2bbd10f45727c92bf7833e510d58070d6ed730dd8fe5364d449`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 5.2 KB (5167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ce2f4c12c6653d03e939b29fe301973ce8589b549c9f76b1fdefa99a55ab50`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98b2cb6250231ed8cef6de96815e140e12ba409d091fb57ee1adfe2c289ad9b`  
		Last Modified: Wed, 06 Apr 2022 01:56:44 GMT  
		Size: 72.6 MB (72638754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5bbf2fe5aa655e9cf36beac127786eecb56097e4ab21bab76154f593fbf97`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59159102a72740462897aeaabf19c0152976db3874fde7f09b268b45a5ad992`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aad673b55427fd9d7f8ca33f31eeaec2f327fc06001f88d0be4f4138a3576fb`  
		Last Modified: Wed, 06 Apr 2022 01:56:34 GMT  
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
$ docker pull mariadb@sha256:bb15b05ff6a038ff3d8c6c487fc01dd544054a09d8418fa112f808bca23d676e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133b521439e19cf4bbc797a82404d5f1283beeefe84f1036b229ac3b505dac05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:18:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:19:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:19:44 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:20:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:20:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:20:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:20:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:21:29 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:30 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:32 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:34 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 21:21:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:23:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:26:45 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:27:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:27:12 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:27:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee36c86f28b3454fed4c8ac5e091c4599123141b97f4c2d06bcaacef3db2ea7`  
		Last Modified: Sat, 19 Mar 2022 21:29:40 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b3bdd7509a19317e5839d95ede6349efc532222db47bead436a5c7b050e85d`  
		Last Modified: Sat, 19 Mar 2022 21:29:47 GMT  
		Size: 5.6 MB (5630211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2784f406f140da871c18b0b6482e18de484e2d4827fa0216dc1ec8e3ef8aa513`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 3.5 MB (3533413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4aba83fb5ef3f7de5b84459fc4721d07fc86c85e606c13347570174773185`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413573cd9619e1f71e4549da75acfb8c299766f9215e8130a557954f9c25519`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 1.9 MB (1936744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c31864f49567b8a3f7e571d3f5d2108c556425e17d0ff91b78c295eba74dbb`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d85e8ff6d332e09313c616b10d030e5694a52436cec84ca1b53f9c3da9ed25e`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96fd22c02287002999574e230adbefacaa56d0f60bbd6ff87906f6d459676e6`  
		Last Modified: Sat, 19 Mar 2022 21:29:49 GMT  
		Size: 76.2 MB (76158819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cb5401efa11b07ec297c948ccf553be601e0b23eb71e7ed7a14d936994735a`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332eb5bb646168f2ec0c2a411da4f710fcf0fb0693ca1a44859b0403433add2a`  
		Last Modified: Fri, 01 Apr 2022 17:31:05 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19a0a3d27ec087cd94fa80a0d3ea7dd913131fa244ccb6abadb6a2e5f80b29a`  
		Last Modified: Fri, 01 Apr 2022 17:31:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.43-bionic`

```console
$ docker pull mariadb@sha256:d28588e5e7f3abcf5a8e364baaf497675f6c7c7fdde3d6dbebc127f80e78cc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.43-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:bae1af3a9ab7d216a21591bcf4524263edd1c820915e679ae1553d517934992e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109315419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8f3a60883793bbf979c342242c10343081b11d7898a2375b23ea64d51ec981`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:11:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:11:30 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:11:30 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:11:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:11:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:11:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:11:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:11:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:11:53 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 00:11:53 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 06 Apr 2022 00:11:53 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 00:11:53 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Wed, 06 Apr 2022 00:11:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Wed, 06 Apr 2022 00:11:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:12:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:12:27 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:12:27 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:12:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:12:28 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229eef75b67b318b8c76eb00e60e1aa7b2ebdfaf759f30a88e4c49fa36eb8648`  
		Last Modified: Wed, 06 Apr 2022 01:56:38 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfaf091f1fb44dbaf7f7e2ef64b08b4bbd721bb85efa1a6873f59363a3c00ac`  
		Last Modified: Wed, 06 Apr 2022 01:56:39 GMT  
		Size: 4.8 MB (4813215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ced99642795c1758efcd44723e438622b236ca8059747078a7b449b66d8b84`  
		Last Modified: Wed, 06 Apr 2022 01:56:37 GMT  
		Size: 3.6 MB (3553168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71e962c603d015aefc6871e1e17a5dbe314e7265562820bf1513ec83e935ad3`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388953686a88dd1fb56b5fc8f2e77d4a8572a8217ddcae794f50ab5022a206c`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 1.6 MB (1583440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c6b130a76ec2bbd10f45727c92bf7833e510d58070d6ed730dd8fe5364d449`  
		Last Modified: Wed, 06 Apr 2022 01:56:36 GMT  
		Size: 5.2 KB (5167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ce2f4c12c6653d03e939b29fe301973ce8589b549c9f76b1fdefa99a55ab50`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98b2cb6250231ed8cef6de96815e140e12ba409d091fb57ee1adfe2c289ad9b`  
		Last Modified: Wed, 06 Apr 2022 01:56:44 GMT  
		Size: 72.6 MB (72638754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5bbf2fe5aa655e9cf36beac127786eecb56097e4ab21bab76154f593fbf97`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59159102a72740462897aeaabf19c0152976db3874fde7f09b268b45a5ad992`  
		Last Modified: Wed, 06 Apr 2022 01:56:33 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aad673b55427fd9d7f8ca33f31eeaec2f327fc06001f88d0be4f4138a3576fb`  
		Last Modified: Wed, 06 Apr 2022 01:56:34 GMT  
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
$ docker pull mariadb@sha256:bb15b05ff6a038ff3d8c6c487fc01dd544054a09d8418fa112f808bca23d676e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133b521439e19cf4bbc797a82404d5f1283beeefe84f1036b229ac3b505dac05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:18:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:19:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:19:44 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:20:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:20:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:20:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:20:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:21:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:21:29 GMT
ARG MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:30 GMT
ENV MARIADB_MAJOR=10.2
# Sat, 19 Mar 2022 21:21:32 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:34 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Sat, 19 Mar 2022 21:21:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Sat, 19 Mar 2022 21:21:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:23:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:23:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:23:45 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:26:45 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:26:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:27:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:27:12 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:27:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee36c86f28b3454fed4c8ac5e091c4599123141b97f4c2d06bcaacef3db2ea7`  
		Last Modified: Sat, 19 Mar 2022 21:29:40 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b3bdd7509a19317e5839d95ede6349efc532222db47bead436a5c7b050e85d`  
		Last Modified: Sat, 19 Mar 2022 21:29:47 GMT  
		Size: 5.6 MB (5630211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2784f406f140da871c18b0b6482e18de484e2d4827fa0216dc1ec8e3ef8aa513`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 3.5 MB (3533413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4aba83fb5ef3f7de5b84459fc4721d07fc86c85e606c13347570174773185`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413573cd9619e1f71e4549da75acfb8c299766f9215e8130a557954f9c25519`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 1.9 MB (1936744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c31864f49567b8a3f7e571d3f5d2108c556425e17d0ff91b78c295eba74dbb`  
		Last Modified: Sat, 19 Mar 2022 21:29:38 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d85e8ff6d332e09313c616b10d030e5694a52436cec84ca1b53f9c3da9ed25e`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96fd22c02287002999574e230adbefacaa56d0f60bbd6ff87906f6d459676e6`  
		Last Modified: Sat, 19 Mar 2022 21:29:49 GMT  
		Size: 76.2 MB (76158819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cb5401efa11b07ec297c948ccf553be601e0b23eb71e7ed7a14d936994735a`  
		Last Modified: Sat, 19 Mar 2022 21:29:35 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332eb5bb646168f2ec0c2a411da4f710fcf0fb0693ca1a44859b0403433add2a`  
		Last Modified: Fri, 01 Apr 2022 17:31:05 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19a0a3d27ec087cd94fa80a0d3ea7dd913131fa244ccb6abadb6a2e5f80b29a`  
		Last Modified: Fri, 01 Apr 2022 17:31:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:c41049e90acf6c212f43677c02dedb21e7c9cca4a3ab6d90732f9f9c791aa8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:6579e6ccec771609b20f4022273823d7469d3fb5bc7f2f1609d29d5fe956365d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39faa709969abaec9629e285b592dc7e7ad7d06523da06c3d9b84fc2fc212907`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:10:48 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 00:10:48 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 00:10:48 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 00:10:48 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 00:10:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:10:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:11:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:11:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:11:16 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:11:16 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:11:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:11:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:11:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:11:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d771618f5fcd4ceb4c667c15fc15730b57fbcacd0cc3e93196655f46b9de4c`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59834a219274472bedd9b70b5247c61e160d5d135bb1e126a468709f53082b0b`  
		Last Modified: Wed, 06 Apr 2022 01:56:17 GMT  
		Size: 80.2 MB (80191188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b18118bafdb3a7f5bc362cd669228922a106980195fd6ec2172e9d01d4a4bd`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755a04677fec7009da543632f5a12ee936b854604b564ab9be6b7211b7024aae`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e37be5d2902ac40ee9f8840cdffa342b6bd9bbd86c32f0ff30b2988ea7976`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
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
$ docker pull mariadb@sha256:7278de7ad5bbcd676cdd3f7087615a411d6430ca4dccf29eb341c4cccb95c0b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131008236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c64f172171ed9245c735e546f89601800e44b3355f2048d68b3cdfcce09d18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:16:29 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:30 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:32 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:34 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:16:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:18:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:18:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:18:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:26:08 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:26:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:26:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:26:27 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:26:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c8d3df4b6b8e3255209c736c47a061df523c9fa1f35f9a2645191166f9e11`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ea247ebcc10c99016e39d4667495cd4b57e9aa0d1750ad7868fe82680138fd`  
		Last Modified: Sat, 19 Mar 2022 21:29:13 GMT  
		Size: 84.8 MB (84791811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454c6501617cf40901a23bbfa94933e4928b0c8b1b81d7d70a3ac5dd84281e6`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c278465911da10f0aafc19618813e0a65d7c1f43db3ba813e12a936c0d0f0b`  
		Last Modified: Fri, 01 Apr 2022 17:30:43 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f904d81e50308dea5a612f7fc172616a6212857d4470fa097f13d4dd8347c3a`  
		Last Modified: Fri, 01 Apr 2022 17:30:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:c41049e90acf6c212f43677c02dedb21e7c9cca4a3ab6d90732f9f9c791aa8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:6579e6ccec771609b20f4022273823d7469d3fb5bc7f2f1609d29d5fe956365d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39faa709969abaec9629e285b592dc7e7ad7d06523da06c3d9b84fc2fc212907`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:10:48 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 00:10:48 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 00:10:48 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 00:10:48 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 00:10:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:10:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:11:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:11:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:11:16 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:11:16 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:11:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:11:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:11:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:11:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d771618f5fcd4ceb4c667c15fc15730b57fbcacd0cc3e93196655f46b9de4c`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59834a219274472bedd9b70b5247c61e160d5d135bb1e126a468709f53082b0b`  
		Last Modified: Wed, 06 Apr 2022 01:56:17 GMT  
		Size: 80.2 MB (80191188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b18118bafdb3a7f5bc362cd669228922a106980195fd6ec2172e9d01d4a4bd`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755a04677fec7009da543632f5a12ee936b854604b564ab9be6b7211b7024aae`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e37be5d2902ac40ee9f8840cdffa342b6bd9bbd86c32f0ff30b2988ea7976`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
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
$ docker pull mariadb@sha256:7278de7ad5bbcd676cdd3f7087615a411d6430ca4dccf29eb341c4cccb95c0b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131008236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c64f172171ed9245c735e546f89601800e44b3355f2048d68b3cdfcce09d18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:16:29 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:30 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:32 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:34 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:16:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:18:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:18:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:18:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:26:08 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:26:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:26:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:26:27 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:26:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c8d3df4b6b8e3255209c736c47a061df523c9fa1f35f9a2645191166f9e11`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ea247ebcc10c99016e39d4667495cd4b57e9aa0d1750ad7868fe82680138fd`  
		Last Modified: Sat, 19 Mar 2022 21:29:13 GMT  
		Size: 84.8 MB (84791811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454c6501617cf40901a23bbfa94933e4928b0c8b1b81d7d70a3ac5dd84281e6`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c278465911da10f0aafc19618813e0a65d7c1f43db3ba813e12a936c0d0f0b`  
		Last Modified: Fri, 01 Apr 2022 17:30:43 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f904d81e50308dea5a612f7fc172616a6212857d4470fa097f13d4dd8347c3a`  
		Last Modified: Fri, 01 Apr 2022 17:30:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.34`

```console
$ docker pull mariadb@sha256:c41049e90acf6c212f43677c02dedb21e7c9cca4a3ab6d90732f9f9c791aa8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.34` - linux; amd64

```console
$ docker pull mariadb@sha256:6579e6ccec771609b20f4022273823d7469d3fb5bc7f2f1609d29d5fe956365d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39faa709969abaec9629e285b592dc7e7ad7d06523da06c3d9b84fc2fc212907`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:10:48 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 00:10:48 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 00:10:48 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 00:10:48 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 00:10:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:10:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:11:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:11:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:11:16 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:11:16 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:11:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:11:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:11:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:11:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d771618f5fcd4ceb4c667c15fc15730b57fbcacd0cc3e93196655f46b9de4c`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59834a219274472bedd9b70b5247c61e160d5d135bb1e126a468709f53082b0b`  
		Last Modified: Wed, 06 Apr 2022 01:56:17 GMT  
		Size: 80.2 MB (80191188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b18118bafdb3a7f5bc362cd669228922a106980195fd6ec2172e9d01d4a4bd`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755a04677fec7009da543632f5a12ee936b854604b564ab9be6b7211b7024aae`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e37be5d2902ac40ee9f8840cdffa342b6bd9bbd86c32f0ff30b2988ea7976`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
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
$ docker pull mariadb@sha256:7278de7ad5bbcd676cdd3f7087615a411d6430ca4dccf29eb341c4cccb95c0b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131008236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c64f172171ed9245c735e546f89601800e44b3355f2048d68b3cdfcce09d18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:16:29 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:30 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:32 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:34 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:16:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:18:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:18:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:18:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:26:08 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:26:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:26:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:26:27 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:26:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c8d3df4b6b8e3255209c736c47a061df523c9fa1f35f9a2645191166f9e11`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ea247ebcc10c99016e39d4667495cd4b57e9aa0d1750ad7868fe82680138fd`  
		Last Modified: Sat, 19 Mar 2022 21:29:13 GMT  
		Size: 84.8 MB (84791811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454c6501617cf40901a23bbfa94933e4928b0c8b1b81d7d70a3ac5dd84281e6`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c278465911da10f0aafc19618813e0a65d7c1f43db3ba813e12a936c0d0f0b`  
		Last Modified: Fri, 01 Apr 2022 17:30:43 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f904d81e50308dea5a612f7fc172616a6212857d4470fa097f13d4dd8347c3a`  
		Last Modified: Fri, 01 Apr 2022 17:30:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.34-focal`

```console
$ docker pull mariadb@sha256:c41049e90acf6c212f43677c02dedb21e7c9cca4a3ab6d90732f9f9c791aa8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.34-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:6579e6ccec771609b20f4022273823d7469d3fb5bc7f2f1609d29d5fe956365d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39faa709969abaec9629e285b592dc7e7ad7d06523da06c3d9b84fc2fc212907`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:10:48 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 00:10:48 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 06 Apr 2022 00:10:48 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 00:10:48 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Wed, 06 Apr 2022 00:10:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:10:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:11:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:11:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:11:16 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:11:16 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:11:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:11:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:11:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:11:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d771618f5fcd4ceb4c667c15fc15730b57fbcacd0cc3e93196655f46b9de4c`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59834a219274472bedd9b70b5247c61e160d5d135bb1e126a468709f53082b0b`  
		Last Modified: Wed, 06 Apr 2022 01:56:17 GMT  
		Size: 80.2 MB (80191188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b18118bafdb3a7f5bc362cd669228922a106980195fd6ec2172e9d01d4a4bd`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755a04677fec7009da543632f5a12ee936b854604b564ab9be6b7211b7024aae`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e37be5d2902ac40ee9f8840cdffa342b6bd9bbd86c32f0ff30b2988ea7976`  
		Last Modified: Wed, 06 Apr 2022 01:56:05 GMT  
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
$ docker pull mariadb@sha256:7278de7ad5bbcd676cdd3f7087615a411d6430ca4dccf29eb341c4cccb95c0b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131008236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c64f172171ed9245c735e546f89601800e44b3355f2048d68b3cdfcce09d18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:16:29 GMT
ARG MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:30 GMT
ENV MARIADB_MAJOR=10.3
# Sat, 19 Mar 2022 21:16:32 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:34 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Sat, 19 Mar 2022 21:16:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:16:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:18:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:18:22 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:18:24 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:26:08 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:26:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:26:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:26:27 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:26:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c8d3df4b6b8e3255209c736c47a061df523c9fa1f35f9a2645191166f9e11`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ea247ebcc10c99016e39d4667495cd4b57e9aa0d1750ad7868fe82680138fd`  
		Last Modified: Sat, 19 Mar 2022 21:29:13 GMT  
		Size: 84.8 MB (84791811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454c6501617cf40901a23bbfa94933e4928b0c8b1b81d7d70a3ac5dd84281e6`  
		Last Modified: Sat, 19 Mar 2022 21:28:57 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c278465911da10f0aafc19618813e0a65d7c1f43db3ba813e12a936c0d0f0b`  
		Last Modified: Fri, 01 Apr 2022 17:30:43 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f904d81e50308dea5a612f7fc172616a6212857d4470fa097f13d4dd8347c3a`  
		Last Modified: Fri, 01 Apr 2022 17:30:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:c5e91d6503e594e464a4e1186271727b889be797a5363fd8a58dca661b5e4b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:152317013ac4385ea9cd5560743b26ec596f732f50ea987e6c13e9a1e995e404
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9eedbcf3d609e0f9ed3bb2008e18342001337fb6b2bb2e845d07eb800cc37e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:10:19 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 00:10:20 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 00:10:20 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 00:10:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 00:10:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:10:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:10:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:10:44 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:10:44 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:10:45 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:10:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:10:45 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc09ffeb8fb5a109d132031612ddbebc407610edc5fdc89536bad43d42158ff0`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4a37200735f9b065606fc4813f2b58432dd4e4064b686e206ae03b2d8e7553`  
		Last Modified: Wed, 06 Apr 2022 01:55:45 GMT  
		Size: 85.8 MB (85753312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5e9b7511b70ef7bd57b80df540ae3caf5bf3feec10baf21f680832a9d92727`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e26005acc12342fb4e55353dfe9a176ebf5b9aa3d46664beacd20bd21c1dbc`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be0faecd5aa5f36ea8ef78d3fe01564c6f0e885d177468ef7050694db52a1f0`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
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
$ docker pull mariadb@sha256:67c8ce133dceee85bf7ae68af6b483ef052736308859cabfdb08e51856f89b0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136562273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad9d15b9a855734a3a0e88914e3fd54c4c4e00a35faa6163d74ac3b55ed6f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:14:14 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:15 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:18 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:14:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:15:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:16:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:25:29 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:25:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:25:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:52 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cc082e834587f61f02cf5842d3676410f0a7743ce3f12abd0dadf35166d28d`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054bd3a03783d1b3a1c4bcf98f998aa5ecdeba7a84dfa29a6dc6e7f778ab0a1e`  
		Last Modified: Sat, 19 Mar 2022 21:28:36 GMT  
		Size: 90.3 MB (90345847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e952abd50af62b471597b6b082e469096d04492801dda280b92d8a817e1d8c6`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9280b2015c0d7d2d80c9c576b641adbfc91412bc8bd7767744e49d17e26d4f`  
		Last Modified: Fri, 01 Apr 2022 17:30:22 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecad413236244805d916ec8e61daec1a2cbfd6842766d647b51e6d770ecc5bed`  
		Last Modified: Fri, 01 Apr 2022 17:30:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:c5e91d6503e594e464a4e1186271727b889be797a5363fd8a58dca661b5e4b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:152317013ac4385ea9cd5560743b26ec596f732f50ea987e6c13e9a1e995e404
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9eedbcf3d609e0f9ed3bb2008e18342001337fb6b2bb2e845d07eb800cc37e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:10:19 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 00:10:20 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 00:10:20 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 00:10:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 00:10:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:10:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:10:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:10:44 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:10:44 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:10:45 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:10:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:10:45 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc09ffeb8fb5a109d132031612ddbebc407610edc5fdc89536bad43d42158ff0`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4a37200735f9b065606fc4813f2b58432dd4e4064b686e206ae03b2d8e7553`  
		Last Modified: Wed, 06 Apr 2022 01:55:45 GMT  
		Size: 85.8 MB (85753312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5e9b7511b70ef7bd57b80df540ae3caf5bf3feec10baf21f680832a9d92727`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e26005acc12342fb4e55353dfe9a176ebf5b9aa3d46664beacd20bd21c1dbc`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be0faecd5aa5f36ea8ef78d3fe01564c6f0e885d177468ef7050694db52a1f0`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
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
$ docker pull mariadb@sha256:67c8ce133dceee85bf7ae68af6b483ef052736308859cabfdb08e51856f89b0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136562273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad9d15b9a855734a3a0e88914e3fd54c4c4e00a35faa6163d74ac3b55ed6f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:14:14 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:15 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:18 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:14:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:15:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:16:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:25:29 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:25:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:25:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:52 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cc082e834587f61f02cf5842d3676410f0a7743ce3f12abd0dadf35166d28d`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054bd3a03783d1b3a1c4bcf98f998aa5ecdeba7a84dfa29a6dc6e7f778ab0a1e`  
		Last Modified: Sat, 19 Mar 2022 21:28:36 GMT  
		Size: 90.3 MB (90345847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e952abd50af62b471597b6b082e469096d04492801dda280b92d8a817e1d8c6`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9280b2015c0d7d2d80c9c576b641adbfc91412bc8bd7767744e49d17e26d4f`  
		Last Modified: Fri, 01 Apr 2022 17:30:22 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecad413236244805d916ec8e61daec1a2cbfd6842766d647b51e6d770ecc5bed`  
		Last Modified: Fri, 01 Apr 2022 17:30:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.24`

```console
$ docker pull mariadb@sha256:c5e91d6503e594e464a4e1186271727b889be797a5363fd8a58dca661b5e4b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.24` - linux; amd64

```console
$ docker pull mariadb@sha256:152317013ac4385ea9cd5560743b26ec596f732f50ea987e6c13e9a1e995e404
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9eedbcf3d609e0f9ed3bb2008e18342001337fb6b2bb2e845d07eb800cc37e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:10:19 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 00:10:20 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 00:10:20 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 00:10:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 00:10:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:10:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:10:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:10:44 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:10:44 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:10:45 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:10:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:10:45 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc09ffeb8fb5a109d132031612ddbebc407610edc5fdc89536bad43d42158ff0`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4a37200735f9b065606fc4813f2b58432dd4e4064b686e206ae03b2d8e7553`  
		Last Modified: Wed, 06 Apr 2022 01:55:45 GMT  
		Size: 85.8 MB (85753312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5e9b7511b70ef7bd57b80df540ae3caf5bf3feec10baf21f680832a9d92727`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e26005acc12342fb4e55353dfe9a176ebf5b9aa3d46664beacd20bd21c1dbc`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be0faecd5aa5f36ea8ef78d3fe01564c6f0e885d177468ef7050694db52a1f0`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
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
$ docker pull mariadb@sha256:67c8ce133dceee85bf7ae68af6b483ef052736308859cabfdb08e51856f89b0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136562273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad9d15b9a855734a3a0e88914e3fd54c4c4e00a35faa6163d74ac3b55ed6f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:14:14 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:15 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:18 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:14:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:15:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:16:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:25:29 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:25:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:25:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:52 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cc082e834587f61f02cf5842d3676410f0a7743ce3f12abd0dadf35166d28d`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054bd3a03783d1b3a1c4bcf98f998aa5ecdeba7a84dfa29a6dc6e7f778ab0a1e`  
		Last Modified: Sat, 19 Mar 2022 21:28:36 GMT  
		Size: 90.3 MB (90345847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e952abd50af62b471597b6b082e469096d04492801dda280b92d8a817e1d8c6`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9280b2015c0d7d2d80c9c576b641adbfc91412bc8bd7767744e49d17e26d4f`  
		Last Modified: Fri, 01 Apr 2022 17:30:22 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecad413236244805d916ec8e61daec1a2cbfd6842766d647b51e6d770ecc5bed`  
		Last Modified: Fri, 01 Apr 2022 17:30:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.24-focal`

```console
$ docker pull mariadb@sha256:c5e91d6503e594e464a4e1186271727b889be797a5363fd8a58dca661b5e4b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.24-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:152317013ac4385ea9cd5560743b26ec596f732f50ea987e6c13e9a1e995e404
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9eedbcf3d609e0f9ed3bb2008e18342001337fb6b2bb2e845d07eb800cc37e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:10:19 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 00:10:20 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 06 Apr 2022 00:10:20 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 00:10:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Wed, 06 Apr 2022 00:10:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:10:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:10:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:10:44 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:10:44 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:10:45 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:10:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 06 Apr 2022 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:10:45 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:10:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc09ffeb8fb5a109d132031612ddbebc407610edc5fdc89536bad43d42158ff0`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4a37200735f9b065606fc4813f2b58432dd4e4064b686e206ae03b2d8e7553`  
		Last Modified: Wed, 06 Apr 2022 01:55:45 GMT  
		Size: 85.8 MB (85753312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5e9b7511b70ef7bd57b80df540ae3caf5bf3feec10baf21f680832a9d92727`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e26005acc12342fb4e55353dfe9a176ebf5b9aa3d46664beacd20bd21c1dbc`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be0faecd5aa5f36ea8ef78d3fe01564c6f0e885d177468ef7050694db52a1f0`  
		Last Modified: Wed, 06 Apr 2022 01:55:32 GMT  
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
$ docker pull mariadb@sha256:67c8ce133dceee85bf7ae68af6b483ef052736308859cabfdb08e51856f89b0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136562273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad9d15b9a855734a3a0e88914e3fd54c4c4e00a35faa6163d74ac3b55ed6f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:14:14 GMT
ARG MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:15 GMT
ENV MARIADB_MAJOR=10.4
# Sat, 19 Mar 2022 21:14:18 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:20 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Sat, 19 Mar 2022 21:14:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:14:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:15:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:16:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:16:05 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:25:29 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:25:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Apr 2022 17:25:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:52 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cc082e834587f61f02cf5842d3676410f0a7743ce3f12abd0dadf35166d28d`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054bd3a03783d1b3a1c4bcf98f998aa5ecdeba7a84dfa29a6dc6e7f778ab0a1e`  
		Last Modified: Sat, 19 Mar 2022 21:28:36 GMT  
		Size: 90.3 MB (90345847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e952abd50af62b471597b6b082e469096d04492801dda280b92d8a817e1d8c6`  
		Last Modified: Sat, 19 Mar 2022 21:28:19 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9280b2015c0d7d2d80c9c576b641adbfc91412bc8bd7767744e49d17e26d4f`  
		Last Modified: Fri, 01 Apr 2022 17:30:22 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecad413236244805d916ec8e61daec1a2cbfd6842766d647b51e6d770ecc5bed`  
		Last Modified: Fri, 01 Apr 2022 17:30:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:13a5bd85125db885a0dbf0746cee4ce4327996ba657d7d79a01b693ce2fd0401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:68e36c4e48d5ef9f29e446db54aab7852f54bde0991657d2603b282b757ed323
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127923856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b7d2c79b8cf7e98e75bfb213f0833a054d6c23f48896cf070f71ef5f5ebc63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:09:52 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 00:09:52 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 00:09:52 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 00:09:52 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 00:09:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:09:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:10:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:10:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:10:16 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:10:16 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:10:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:10:16 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:10:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40cc2957dd9a6fe8c21516a9e0274144fc6eaa50a26b91cec7dc5bd889c637d`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb06ed7078af49710dc64fb89d88a241ca537044bb6ea74b0d8816aeb6e03160`  
		Last Modified: Wed, 06 Apr 2022 01:55:11 GMT  
		Size: 88.0 MB (87997319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f20d625170046096e8e151b072f700e3a0c75619382f37989b95fae63aad61b`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb1c47d4d07b98fdf5061e03f5701a04496ff4f70a257a7bb2295585a5f42e2`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 6.8 KB (6770 bytes)  
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
$ docker pull mariadb@sha256:1d9fbb4d902dc9ae32610f753eba353f6fe23f9472a563b860290b61cb78733a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138783602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f071c18b40ac9aadc0c3f1b34fdf7a9b635436e2b67ab4d552e5de33b0714ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:12:05 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:07 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:09 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:10 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:12:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:13:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:13:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:13:50 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:25:11 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:25:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:17 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d7e00cc5af3960b98c6509ffc589802530f8ec93faa4b179c232eeb696a3f3`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc1e85429494765529e765afc97c110c7c5eeb112cf6687f89cb532e4d5677`  
		Last Modified: Sat, 19 Mar 2022 21:27:57 GMT  
		Size: 92.6 MB (92567297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857b6a5edbb178d15e798427c44003557d3f8138fcec12bb78b4ddc0724994bf`  
		Last Modified: Sat, 19 Mar 2022 21:27:41 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491ba7373d5704c3cde4dcb0d1180bf8db4ef1964030b70a88158210c104247f`  
		Last Modified: Fri, 01 Apr 2022 17:30:01 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:199879a341df75c4bfb84c09c3b6f0f3c504215253a4d262970e0bc8a39aa9c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127196167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1ff70cb663ab48b2cb427d1660ee600b9c7112f3f566f7fef8099814097e3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:32:37 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:32:37 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:32:37 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:32:37 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:32:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:32:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:32:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:33:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:33:01 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:33:01 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:33:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:33:01 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:33:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7116963c40cda3b4e0c02bd63d8f027cc08e7ffe19fecb34dca80c6c455e7e9`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba93c8f2b0252af49ae08645900f44205084b7f2ab0d2101c0d7eee427040038`  
		Last Modified: Tue, 05 Apr 2022 23:35:18 GMT  
		Size: 89.3 MB (89289987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9273daee5599a10b50994ecead2da824027c6c4f2c12dce13f26769e25ae3379`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986242cb83e4cc10d13e19ba1a4d75b1528762c8dbce20d4326d8d9d8cc7862`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:13a5bd85125db885a0dbf0746cee4ce4327996ba657d7d79a01b693ce2fd0401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:68e36c4e48d5ef9f29e446db54aab7852f54bde0991657d2603b282b757ed323
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127923856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b7d2c79b8cf7e98e75bfb213f0833a054d6c23f48896cf070f71ef5f5ebc63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:09:52 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 00:09:52 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 00:09:52 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 00:09:52 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 00:09:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:09:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:10:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:10:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:10:16 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:10:16 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:10:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:10:16 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:10:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40cc2957dd9a6fe8c21516a9e0274144fc6eaa50a26b91cec7dc5bd889c637d`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb06ed7078af49710dc64fb89d88a241ca537044bb6ea74b0d8816aeb6e03160`  
		Last Modified: Wed, 06 Apr 2022 01:55:11 GMT  
		Size: 88.0 MB (87997319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f20d625170046096e8e151b072f700e3a0c75619382f37989b95fae63aad61b`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb1c47d4d07b98fdf5061e03f5701a04496ff4f70a257a7bb2295585a5f42e2`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 6.8 KB (6770 bytes)  
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
$ docker pull mariadb@sha256:1d9fbb4d902dc9ae32610f753eba353f6fe23f9472a563b860290b61cb78733a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138783602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f071c18b40ac9aadc0c3f1b34fdf7a9b635436e2b67ab4d552e5de33b0714ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:12:05 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:07 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:09 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:10 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:12:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:13:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:13:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:13:50 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:25:11 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:25:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:17 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d7e00cc5af3960b98c6509ffc589802530f8ec93faa4b179c232eeb696a3f3`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc1e85429494765529e765afc97c110c7c5eeb112cf6687f89cb532e4d5677`  
		Last Modified: Sat, 19 Mar 2022 21:27:57 GMT  
		Size: 92.6 MB (92567297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857b6a5edbb178d15e798427c44003557d3f8138fcec12bb78b4ddc0724994bf`  
		Last Modified: Sat, 19 Mar 2022 21:27:41 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491ba7373d5704c3cde4dcb0d1180bf8db4ef1964030b70a88158210c104247f`  
		Last Modified: Fri, 01 Apr 2022 17:30:01 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:199879a341df75c4bfb84c09c3b6f0f3c504215253a4d262970e0bc8a39aa9c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127196167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1ff70cb663ab48b2cb427d1660ee600b9c7112f3f566f7fef8099814097e3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:32:37 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:32:37 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:32:37 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:32:37 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:32:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:32:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:32:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:33:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:33:01 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:33:01 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:33:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:33:01 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:33:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7116963c40cda3b4e0c02bd63d8f027cc08e7ffe19fecb34dca80c6c455e7e9`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba93c8f2b0252af49ae08645900f44205084b7f2ab0d2101c0d7eee427040038`  
		Last Modified: Tue, 05 Apr 2022 23:35:18 GMT  
		Size: 89.3 MB (89289987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9273daee5599a10b50994ecead2da824027c6c4f2c12dce13f26769e25ae3379`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986242cb83e4cc10d13e19ba1a4d75b1528762c8dbce20d4326d8d9d8cc7862`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.15`

```console
$ docker pull mariadb@sha256:13a5bd85125db885a0dbf0746cee4ce4327996ba657d7d79a01b693ce2fd0401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.15` - linux; amd64

```console
$ docker pull mariadb@sha256:68e36c4e48d5ef9f29e446db54aab7852f54bde0991657d2603b282b757ed323
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127923856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b7d2c79b8cf7e98e75bfb213f0833a054d6c23f48896cf070f71ef5f5ebc63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:09:52 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 00:09:52 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 00:09:52 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 00:09:52 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 00:09:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:09:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:10:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:10:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:10:16 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:10:16 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:10:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:10:16 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:10:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40cc2957dd9a6fe8c21516a9e0274144fc6eaa50a26b91cec7dc5bd889c637d`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb06ed7078af49710dc64fb89d88a241ca537044bb6ea74b0d8816aeb6e03160`  
		Last Modified: Wed, 06 Apr 2022 01:55:11 GMT  
		Size: 88.0 MB (87997319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f20d625170046096e8e151b072f700e3a0c75619382f37989b95fae63aad61b`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb1c47d4d07b98fdf5061e03f5701a04496ff4f70a257a7bb2295585a5f42e2`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 6.8 KB (6770 bytes)  
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
$ docker pull mariadb@sha256:1d9fbb4d902dc9ae32610f753eba353f6fe23f9472a563b860290b61cb78733a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138783602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f071c18b40ac9aadc0c3f1b34fdf7a9b635436e2b67ab4d552e5de33b0714ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:12:05 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:07 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:09 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:10 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:12:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:13:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:13:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:13:50 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:25:11 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:25:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:17 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d7e00cc5af3960b98c6509ffc589802530f8ec93faa4b179c232eeb696a3f3`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc1e85429494765529e765afc97c110c7c5eeb112cf6687f89cb532e4d5677`  
		Last Modified: Sat, 19 Mar 2022 21:27:57 GMT  
		Size: 92.6 MB (92567297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857b6a5edbb178d15e798427c44003557d3f8138fcec12bb78b4ddc0724994bf`  
		Last Modified: Sat, 19 Mar 2022 21:27:41 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491ba7373d5704c3cde4dcb0d1180bf8db4ef1964030b70a88158210c104247f`  
		Last Modified: Fri, 01 Apr 2022 17:30:01 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; s390x

```console
$ docker pull mariadb@sha256:199879a341df75c4bfb84c09c3b6f0f3c504215253a4d262970e0bc8a39aa9c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127196167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1ff70cb663ab48b2cb427d1660ee600b9c7112f3f566f7fef8099814097e3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:32:37 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:32:37 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:32:37 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:32:37 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:32:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:32:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:32:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:33:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:33:01 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:33:01 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:33:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:33:01 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:33:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7116963c40cda3b4e0c02bd63d8f027cc08e7ffe19fecb34dca80c6c455e7e9`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba93c8f2b0252af49ae08645900f44205084b7f2ab0d2101c0d7eee427040038`  
		Last Modified: Tue, 05 Apr 2022 23:35:18 GMT  
		Size: 89.3 MB (89289987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9273daee5599a10b50994ecead2da824027c6c4f2c12dce13f26769e25ae3379`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986242cb83e4cc10d13e19ba1a4d75b1528762c8dbce20d4326d8d9d8cc7862`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.15-focal`

```console
$ docker pull mariadb@sha256:13a5bd85125db885a0dbf0746cee4ce4327996ba657d7d79a01b693ce2fd0401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.15-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:68e36c4e48d5ef9f29e446db54aab7852f54bde0991657d2603b282b757ed323
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127923856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b7d2c79b8cf7e98e75bfb213f0833a054d6c23f48896cf070f71ef5f5ebc63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:09:52 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 00:09:52 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 06 Apr 2022 00:09:52 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 00:09:52 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Wed, 06 Apr 2022 00:09:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:09:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:10:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:10:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:10:16 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:10:16 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:10:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:10:16 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:10:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40cc2957dd9a6fe8c21516a9e0274144fc6eaa50a26b91cec7dc5bd889c637d`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb06ed7078af49710dc64fb89d88a241ca537044bb6ea74b0d8816aeb6e03160`  
		Last Modified: Wed, 06 Apr 2022 01:55:11 GMT  
		Size: 88.0 MB (87997319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f20d625170046096e8e151b072f700e3a0c75619382f37989b95fae63aad61b`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb1c47d4d07b98fdf5061e03f5701a04496ff4f70a257a7bb2295585a5f42e2`  
		Last Modified: Wed, 06 Apr 2022 01:54:58 GMT  
		Size: 6.8 KB (6770 bytes)  
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
$ docker pull mariadb@sha256:1d9fbb4d902dc9ae32610f753eba353f6fe23f9472a563b860290b61cb78733a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138783602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f071c18b40ac9aadc0c3f1b34fdf7a9b635436e2b67ab4d552e5de33b0714ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:12:05 GMT
ARG MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:07 GMT
ENV MARIADB_MAJOR=10.5
# Sat, 19 Mar 2022 21:12:09 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:10 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Sat, 19 Mar 2022 21:12:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:12:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:13:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:13:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:13:50 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:25:11 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:25:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:17 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d7e00cc5af3960b98c6509ffc589802530f8ec93faa4b179c232eeb696a3f3`  
		Last Modified: Sat, 19 Mar 2022 21:27:40 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc1e85429494765529e765afc97c110c7c5eeb112cf6687f89cb532e4d5677`  
		Last Modified: Sat, 19 Mar 2022 21:27:57 GMT  
		Size: 92.6 MB (92567297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857b6a5edbb178d15e798427c44003557d3f8138fcec12bb78b4ddc0724994bf`  
		Last Modified: Sat, 19 Mar 2022 21:27:41 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491ba7373d5704c3cde4dcb0d1180bf8db4ef1964030b70a88158210c104247f`  
		Last Modified: Fri, 01 Apr 2022 17:30:01 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:199879a341df75c4bfb84c09c3b6f0f3c504215253a4d262970e0bc8a39aa9c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127196167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1ff70cb663ab48b2cb427d1660ee600b9c7112f3f566f7fef8099814097e3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:32:37 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:32:37 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 05 Apr 2022 23:32:37 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:32:37 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Tue, 05 Apr 2022 23:32:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:32:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:32:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:33:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:33:01 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:33:01 GMT
COPY file:c436b2c23059cf9de16997684da0d7d691080e3af50a8feff6f4c1ee6edfd4c3 in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:33:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:33:01 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:33:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7116963c40cda3b4e0c02bd63d8f027cc08e7ffe19fecb34dca80c6c455e7e9`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba93c8f2b0252af49ae08645900f44205084b7f2ab0d2101c0d7eee427040038`  
		Last Modified: Tue, 05 Apr 2022 23:35:18 GMT  
		Size: 89.3 MB (89289987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9273daee5599a10b50994ecead2da824027c6c4f2c12dce13f26769e25ae3379`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986242cb83e4cc10d13e19ba1a4d75b1528762c8dbce20d4326d8d9d8cc7862`  
		Last Modified: Tue, 05 Apr 2022 23:35:06 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:444da9e26cfc0f5982b34ca44bf7ec1ac8fff9142a46713d23157545ed5d8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:01c79a7ed1368a6ee3f51f9dc8b5c2f78ac1133f42bf1d02646db29b4c708377
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f735287a1313975ded29e78e492aabc31b49e871487494118f947ed5b5a9afa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:09:24 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 00:09:24 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 00:09:24 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 00:09:24 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 00:09:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:09:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:48 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:48 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaeae3f278f18aef12b73f8911a68bba9804a38a8d651082215d0a5968d2b61f`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70478b6487c60dca5f41d96f606c371a2c47b66e3a313cae8b00704ff73cf4a0`  
		Last Modified: Wed, 06 Apr 2022 01:54:42 GMT  
		Size: 88.2 MB (88243073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3737f687ab8c0db96120a41f36df017c39b9d91a12eb29f097ea74dab2fa185d`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380823a8f0a6b8a22ca16debd92c277daa8616369ea4e776c1df466b99a7c95f`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 6.8 KB (6776 bytes)  
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
$ docker pull mariadb@sha256:97dbea401a11a7c5300257491e77d4afd8f0a62fd6a74495d6f7ce4d534f6a63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138843827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc459eef0d8145e08f336e55f64e8efd9cc92453a35167e2ef7e47d6f09cee4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:09:53 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:55 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:56 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:58 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:10:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:11:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:11:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:11:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:00 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:02 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fa8adf7b6a2087ecfda116d886c6593bc7c18497532d5a0cfb9eb34200fd31`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc64de0146146a96cc25d1fd2223c33bdd8bcd2e92d92c1735e33f46d2e7a13`  
		Last Modified: Sat, 19 Mar 2022 21:27:19 GMT  
		Size: 92.6 MB (92627523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29e4f9cc4867b675364abc5418d094c5bd07f46375b8d63d9859a4744a1086f`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233de215a2cef0fcde417b55874825acb3306da2b0d7db1ad609ffdd3a301cae`  
		Last Modified: Fri, 01 Apr 2022 17:29:41 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; s390x

```console
$ docker pull mariadb@sha256:7cf649fce071a046d45537f3d48fb3c5c237e52c222b815e6ddc00aace1109bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127222721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e565077e434b00390a7bd89516a9203e62e97c7cc66115cd41d686cc16ef77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:32:05 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:32:05 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:32:05 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:32:05 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:32:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:32:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:32:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:32:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:32:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:32:29 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:32:29 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:32:29 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c5654770a7ddf4708cb4db11b3f4bf304cc6ee2ca984f1b70b955b2db34c37`  
		Last Modified: Tue, 05 Apr 2022 23:34:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147ac3529a14f307a827496313cbd2aad50b5fad0b94f74b3ef522606f28d99f`  
		Last Modified: Tue, 05 Apr 2022 23:34:55 GMT  
		Size: 89.3 MB (89316537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a7406b4a28fe346fb92e12a7389e2024de8a48fbd52a31a31d898f5977f335`  
		Last Modified: Tue, 05 Apr 2022 23:34:43 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c2aa5587b4c54b100dd762d56cb8825c07a650ac44acd4c532774d0894c199`  
		Last Modified: Tue, 05 Apr 2022 23:34:43 GMT  
		Size: 6.8 KB (6777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:444da9e26cfc0f5982b34ca44bf7ec1ac8fff9142a46713d23157545ed5d8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:01c79a7ed1368a6ee3f51f9dc8b5c2f78ac1133f42bf1d02646db29b4c708377
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f735287a1313975ded29e78e492aabc31b49e871487494118f947ed5b5a9afa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:09:24 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 00:09:24 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 00:09:24 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 00:09:24 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 00:09:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:09:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:48 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:48 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaeae3f278f18aef12b73f8911a68bba9804a38a8d651082215d0a5968d2b61f`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70478b6487c60dca5f41d96f606c371a2c47b66e3a313cae8b00704ff73cf4a0`  
		Last Modified: Wed, 06 Apr 2022 01:54:42 GMT  
		Size: 88.2 MB (88243073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3737f687ab8c0db96120a41f36df017c39b9d91a12eb29f097ea74dab2fa185d`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380823a8f0a6b8a22ca16debd92c277daa8616369ea4e776c1df466b99a7c95f`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 6.8 KB (6776 bytes)  
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
$ docker pull mariadb@sha256:97dbea401a11a7c5300257491e77d4afd8f0a62fd6a74495d6f7ce4d534f6a63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138843827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc459eef0d8145e08f336e55f64e8efd9cc92453a35167e2ef7e47d6f09cee4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:09:53 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:55 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:56 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:58 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:10:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:11:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:11:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:11:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:00 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:02 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fa8adf7b6a2087ecfda116d886c6593bc7c18497532d5a0cfb9eb34200fd31`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc64de0146146a96cc25d1fd2223c33bdd8bcd2e92d92c1735e33f46d2e7a13`  
		Last Modified: Sat, 19 Mar 2022 21:27:19 GMT  
		Size: 92.6 MB (92627523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29e4f9cc4867b675364abc5418d094c5bd07f46375b8d63d9859a4744a1086f`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233de215a2cef0fcde417b55874825acb3306da2b0d7db1ad609ffdd3a301cae`  
		Last Modified: Fri, 01 Apr 2022 17:29:41 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:7cf649fce071a046d45537f3d48fb3c5c237e52c222b815e6ddc00aace1109bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127222721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e565077e434b00390a7bd89516a9203e62e97c7cc66115cd41d686cc16ef77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:32:05 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:32:05 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:32:05 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:32:05 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:32:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:32:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:32:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:32:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:32:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:32:29 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:32:29 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:32:29 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c5654770a7ddf4708cb4db11b3f4bf304cc6ee2ca984f1b70b955b2db34c37`  
		Last Modified: Tue, 05 Apr 2022 23:34:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147ac3529a14f307a827496313cbd2aad50b5fad0b94f74b3ef522606f28d99f`  
		Last Modified: Tue, 05 Apr 2022 23:34:55 GMT  
		Size: 89.3 MB (89316537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a7406b4a28fe346fb92e12a7389e2024de8a48fbd52a31a31d898f5977f335`  
		Last Modified: Tue, 05 Apr 2022 23:34:43 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c2aa5587b4c54b100dd762d56cb8825c07a650ac44acd4c532774d0894c199`  
		Last Modified: Tue, 05 Apr 2022 23:34:43 GMT  
		Size: 6.8 KB (6777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.7`

```console
$ docker pull mariadb@sha256:444da9e26cfc0f5982b34ca44bf7ec1ac8fff9142a46713d23157545ed5d8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.7` - linux; amd64

```console
$ docker pull mariadb@sha256:01c79a7ed1368a6ee3f51f9dc8b5c2f78ac1133f42bf1d02646db29b4c708377
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f735287a1313975ded29e78e492aabc31b49e871487494118f947ed5b5a9afa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:09:24 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 00:09:24 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 00:09:24 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 00:09:24 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 00:09:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:09:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:48 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:48 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaeae3f278f18aef12b73f8911a68bba9804a38a8d651082215d0a5968d2b61f`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70478b6487c60dca5f41d96f606c371a2c47b66e3a313cae8b00704ff73cf4a0`  
		Last Modified: Wed, 06 Apr 2022 01:54:42 GMT  
		Size: 88.2 MB (88243073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3737f687ab8c0db96120a41f36df017c39b9d91a12eb29f097ea74dab2fa185d`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380823a8f0a6b8a22ca16debd92c277daa8616369ea4e776c1df466b99a7c95f`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 6.8 KB (6776 bytes)  
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
$ docker pull mariadb@sha256:97dbea401a11a7c5300257491e77d4afd8f0a62fd6a74495d6f7ce4d534f6a63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138843827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc459eef0d8145e08f336e55f64e8efd9cc92453a35167e2ef7e47d6f09cee4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:09:53 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:55 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:56 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:58 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:10:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:11:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:11:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:11:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:00 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:02 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fa8adf7b6a2087ecfda116d886c6593bc7c18497532d5a0cfb9eb34200fd31`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc64de0146146a96cc25d1fd2223c33bdd8bcd2e92d92c1735e33f46d2e7a13`  
		Last Modified: Sat, 19 Mar 2022 21:27:19 GMT  
		Size: 92.6 MB (92627523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29e4f9cc4867b675364abc5418d094c5bd07f46375b8d63d9859a4744a1086f`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233de215a2cef0fcde417b55874825acb3306da2b0d7db1ad609ffdd3a301cae`  
		Last Modified: Fri, 01 Apr 2022 17:29:41 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; s390x

```console
$ docker pull mariadb@sha256:7cf649fce071a046d45537f3d48fb3c5c237e52c222b815e6ddc00aace1109bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127222721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e565077e434b00390a7bd89516a9203e62e97c7cc66115cd41d686cc16ef77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:32:05 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:32:05 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:32:05 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:32:05 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:32:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:32:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:32:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:32:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:32:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:32:29 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:32:29 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:32:29 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c5654770a7ddf4708cb4db11b3f4bf304cc6ee2ca984f1b70b955b2db34c37`  
		Last Modified: Tue, 05 Apr 2022 23:34:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147ac3529a14f307a827496313cbd2aad50b5fad0b94f74b3ef522606f28d99f`  
		Last Modified: Tue, 05 Apr 2022 23:34:55 GMT  
		Size: 89.3 MB (89316537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a7406b4a28fe346fb92e12a7389e2024de8a48fbd52a31a31d898f5977f335`  
		Last Modified: Tue, 05 Apr 2022 23:34:43 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c2aa5587b4c54b100dd762d56cb8825c07a650ac44acd4c532774d0894c199`  
		Last Modified: Tue, 05 Apr 2022 23:34:43 GMT  
		Size: 6.8 KB (6777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.7-focal`

```console
$ docker pull mariadb@sha256:444da9e26cfc0f5982b34ca44bf7ec1ac8fff9142a46713d23157545ed5d8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:01c79a7ed1368a6ee3f51f9dc8b5c2f78ac1133f42bf1d02646db29b4c708377
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f735287a1313975ded29e78e492aabc31b49e871487494118f947ed5b5a9afa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:09:24 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 00:09:24 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 06 Apr 2022 00:09:24 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 00:09:24 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Wed, 06 Apr 2022 00:09:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:09:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:48 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:48 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaeae3f278f18aef12b73f8911a68bba9804a38a8d651082215d0a5968d2b61f`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70478b6487c60dca5f41d96f606c371a2c47b66e3a313cae8b00704ff73cf4a0`  
		Last Modified: Wed, 06 Apr 2022 01:54:42 GMT  
		Size: 88.2 MB (88243073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3737f687ab8c0db96120a41f36df017c39b9d91a12eb29f097ea74dab2fa185d`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380823a8f0a6b8a22ca16debd92c277daa8616369ea4e776c1df466b99a7c95f`  
		Last Modified: Wed, 06 Apr 2022 01:54:29 GMT  
		Size: 6.8 KB (6776 bytes)  
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
$ docker pull mariadb@sha256:97dbea401a11a7c5300257491e77d4afd8f0a62fd6a74495d6f7ce4d534f6a63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138843827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc459eef0d8145e08f336e55f64e8efd9cc92453a35167e2ef7e47d6f09cee4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:09:53 GMT
ARG MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:55 GMT
ENV MARIADB_MAJOR=10.6
# Sat, 19 Mar 2022 21:09:56 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:58 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Sat, 19 Mar 2022 21:09:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:10:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:11:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:11:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:11:48 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:56 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:25:00 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:25:02 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fa8adf7b6a2087ecfda116d886c6593bc7c18497532d5a0cfb9eb34200fd31`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc64de0146146a96cc25d1fd2223c33bdd8bcd2e92d92c1735e33f46d2e7a13`  
		Last Modified: Sat, 19 Mar 2022 21:27:19 GMT  
		Size: 92.6 MB (92627523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29e4f9cc4867b675364abc5418d094c5bd07f46375b8d63d9859a4744a1086f`  
		Last Modified: Sat, 19 Mar 2022 21:27:02 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233de215a2cef0fcde417b55874825acb3306da2b0d7db1ad609ffdd3a301cae`  
		Last Modified: Fri, 01 Apr 2022 17:29:41 GMT  
		Size: 6.8 KB (6775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:7cf649fce071a046d45537f3d48fb3c5c237e52c222b815e6ddc00aace1109bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127222721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e565077e434b00390a7bd89516a9203e62e97c7cc66115cd41d686cc16ef77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:32:05 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:32:05 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 05 Apr 2022 23:32:05 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:32:05 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Tue, 05 Apr 2022 23:32:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:32:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:32:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:32:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:32:29 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:32:29 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:32:29 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:32:29 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c5654770a7ddf4708cb4db11b3f4bf304cc6ee2ca984f1b70b955b2db34c37`  
		Last Modified: Tue, 05 Apr 2022 23:34:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147ac3529a14f307a827496313cbd2aad50b5fad0b94f74b3ef522606f28d99f`  
		Last Modified: Tue, 05 Apr 2022 23:34:55 GMT  
		Size: 89.3 MB (89316537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a7406b4a28fe346fb92e12a7389e2024de8a48fbd52a31a31d898f5977f335`  
		Last Modified: Tue, 05 Apr 2022 23:34:43 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c2aa5587b4c54b100dd762d56cb8825c07a650ac44acd4c532774d0894c199`  
		Last Modified: Tue, 05 Apr 2022 23:34:43 GMT  
		Size: 6.8 KB (6777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7`

```console
$ docker pull mariadb@sha256:e4421edf721f25823f7a867b231a3b41dda67fcc219ad489a5f646c1f2f8a729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7` - linux; amd64

```console
$ docker pull mariadb@sha256:364e6c38ee64f7f961cc1b70d5c31e554754c4a9fcd6516c9b5c31accf134e61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100166b773f8bdb6f5bfcd16a5ae670bc02ec8a0b6f52f6f74cc560aad592fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ef26c44d0008a5eaeb76320f9509d0728c66ee924af3909910b9e9c8d062`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f6e068c19c3abd463f2e8818220f4304558532ce1eea0ba7e88249533a3de2`  
		Last Modified: Wed, 06 Apr 2022 01:54:00 GMT  
		Size: 88.7 MB (88741687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd25d3e0e6be214d9c5ca5d3597275c41c80a9a551f7aef80ddd34f5f41140`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e322e4875b51e5cf140539cccf19a26d235f52baae4c7cc88024a59f599fe`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 6.8 KB (6775 bytes)  
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
$ docker pull mariadb@sha256:73f1a363d1bd5d67665a2e95e281a6c5f9d60cfc954d37bcc543f4323ea16cb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139540029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3073063783d6646d082607b57b7093f8c0726cc621b6b59d5852a14441fc89b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:39 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2f383467f58f976dd982b1bc6e6fff20f589e60b19d6e00b2a84d8b95c1a7`  
		Last Modified: Fri, 01 Apr 2022 17:29:04 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; s390x

```console
$ docker pull mariadb@sha256:2c2eb9a9fa59f3ddae7a55bd0ddf77e246352438463824741eb92a6a347697e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127721348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5405ba6fc8203440741f811f94a5463c814b05cb550bca60b138a06c6605527b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:31:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8a3bf7f3897df0dfedf0c9629a9a933240987145b59678a8d0d26fac2722de`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2029403953732bae90490466205f4c53ff7e048f32f70a2cbab8d2e089984ded`  
		Last Modified: Tue, 05 Apr 2022 23:34:25 GMT  
		Size: 89.8 MB (89815166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc5f84bad71845209754dbd765377f1bbe548ba402569ff98b4f69425f4f93`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f2fd91a171567a326fb6c302b2a10ac5003b1e43c94400e96a1613d65915f`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7-focal`

```console
$ docker pull mariadb@sha256:e4421edf721f25823f7a867b231a3b41dda67fcc219ad489a5f646c1f2f8a729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:364e6c38ee64f7f961cc1b70d5c31e554754c4a9fcd6516c9b5c31accf134e61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100166b773f8bdb6f5bfcd16a5ae670bc02ec8a0b6f52f6f74cc560aad592fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ef26c44d0008a5eaeb76320f9509d0728c66ee924af3909910b9e9c8d062`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f6e068c19c3abd463f2e8818220f4304558532ce1eea0ba7e88249533a3de2`  
		Last Modified: Wed, 06 Apr 2022 01:54:00 GMT  
		Size: 88.7 MB (88741687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd25d3e0e6be214d9c5ca5d3597275c41c80a9a551f7aef80ddd34f5f41140`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e322e4875b51e5cf140539cccf19a26d235f52baae4c7cc88024a59f599fe`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 6.8 KB (6775 bytes)  
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
$ docker pull mariadb@sha256:73f1a363d1bd5d67665a2e95e281a6c5f9d60cfc954d37bcc543f4323ea16cb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139540029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3073063783d6646d082607b57b7093f8c0726cc621b6b59d5852a14441fc89b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:39 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2f383467f58f976dd982b1bc6e6fff20f589e60b19d6e00b2a84d8b95c1a7`  
		Last Modified: Fri, 01 Apr 2022 17:29:04 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:2c2eb9a9fa59f3ddae7a55bd0ddf77e246352438463824741eb92a6a347697e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127721348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5405ba6fc8203440741f811f94a5463c814b05cb550bca60b138a06c6605527b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:31:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8a3bf7f3897df0dfedf0c9629a9a933240987145b59678a8d0d26fac2722de`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2029403953732bae90490466205f4c53ff7e048f32f70a2cbab8d2e089984ded`  
		Last Modified: Tue, 05 Apr 2022 23:34:25 GMT  
		Size: 89.8 MB (89815166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc5f84bad71845209754dbd765377f1bbe548ba402569ff98b4f69425f4f93`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f2fd91a171567a326fb6c302b2a10ac5003b1e43c94400e96a1613d65915f`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.3`

```console
$ docker pull mariadb@sha256:e4421edf721f25823f7a867b231a3b41dda67fcc219ad489a5f646c1f2f8a729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.3` - linux; amd64

```console
$ docker pull mariadb@sha256:364e6c38ee64f7f961cc1b70d5c31e554754c4a9fcd6516c9b5c31accf134e61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100166b773f8bdb6f5bfcd16a5ae670bc02ec8a0b6f52f6f74cc560aad592fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ef26c44d0008a5eaeb76320f9509d0728c66ee924af3909910b9e9c8d062`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f6e068c19c3abd463f2e8818220f4304558532ce1eea0ba7e88249533a3de2`  
		Last Modified: Wed, 06 Apr 2022 01:54:00 GMT  
		Size: 88.7 MB (88741687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd25d3e0e6be214d9c5ca5d3597275c41c80a9a551f7aef80ddd34f5f41140`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e322e4875b51e5cf140539cccf19a26d235f52baae4c7cc88024a59f599fe`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 6.8 KB (6775 bytes)  
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
$ docker pull mariadb@sha256:73f1a363d1bd5d67665a2e95e281a6c5f9d60cfc954d37bcc543f4323ea16cb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139540029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3073063783d6646d082607b57b7093f8c0726cc621b6b59d5852a14441fc89b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:39 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2f383467f58f976dd982b1bc6e6fff20f589e60b19d6e00b2a84d8b95c1a7`  
		Last Modified: Fri, 01 Apr 2022 17:29:04 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; s390x

```console
$ docker pull mariadb@sha256:2c2eb9a9fa59f3ddae7a55bd0ddf77e246352438463824741eb92a6a347697e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127721348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5405ba6fc8203440741f811f94a5463c814b05cb550bca60b138a06c6605527b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:31:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8a3bf7f3897df0dfedf0c9629a9a933240987145b59678a8d0d26fac2722de`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2029403953732bae90490466205f4c53ff7e048f32f70a2cbab8d2e089984ded`  
		Last Modified: Tue, 05 Apr 2022 23:34:25 GMT  
		Size: 89.8 MB (89815166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc5f84bad71845209754dbd765377f1bbe548ba402569ff98b4f69425f4f93`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f2fd91a171567a326fb6c302b2a10ac5003b1e43c94400e96a1613d65915f`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.3-focal`

```console
$ docker pull mariadb@sha256:e4421edf721f25823f7a867b231a3b41dda67fcc219ad489a5f646c1f2f8a729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:364e6c38ee64f7f961cc1b70d5c31e554754c4a9fcd6516c9b5c31accf134e61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100166b773f8bdb6f5bfcd16a5ae670bc02ec8a0b6f52f6f74cc560aad592fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ef26c44d0008a5eaeb76320f9509d0728c66ee924af3909910b9e9c8d062`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f6e068c19c3abd463f2e8818220f4304558532ce1eea0ba7e88249533a3de2`  
		Last Modified: Wed, 06 Apr 2022 01:54:00 GMT  
		Size: 88.7 MB (88741687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd25d3e0e6be214d9c5ca5d3597275c41c80a9a551f7aef80ddd34f5f41140`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e322e4875b51e5cf140539cccf19a26d235f52baae4c7cc88024a59f599fe`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 6.8 KB (6775 bytes)  
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
$ docker pull mariadb@sha256:73f1a363d1bd5d67665a2e95e281a6c5f9d60cfc954d37bcc543f4323ea16cb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139540029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3073063783d6646d082607b57b7093f8c0726cc621b6b59d5852a14441fc89b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:39 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2f383467f58f976dd982b1bc6e6fff20f589e60b19d6e00b2a84d8b95c1a7`  
		Last Modified: Fri, 01 Apr 2022 17:29:04 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:2c2eb9a9fa59f3ddae7a55bd0ddf77e246352438463824741eb92a6a347697e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127721348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5405ba6fc8203440741f811f94a5463c814b05cb550bca60b138a06c6605527b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:31:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8a3bf7f3897df0dfedf0c9629a9a933240987145b59678a8d0d26fac2722de`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2029403953732bae90490466205f4c53ff7e048f32f70a2cbab8d2e089984ded`  
		Last Modified: Tue, 05 Apr 2022 23:34:25 GMT  
		Size: 89.8 MB (89815166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc5f84bad71845209754dbd765377f1bbe548ba402569ff98b4f69425f4f93`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f2fd91a171567a326fb6c302b2a10ac5003b1e43c94400e96a1613d65915f`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-rc`

```console
$ docker pull mariadb@sha256:70656b9ebfa172c4eb9667cf6b18ea99a32e895170351828f31750687c85a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:8a3a50858a36c77b6551873ccbcba16a33c7f2d2fb5a3b40e3139efc9f7af769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128578743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c252d4bcf31e323c374063f0fa34040bc8118004682f3947e5b4cf8236686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:09 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 00:08:09 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 00:08:09 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 00:08:09 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 00:08:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:08:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:08:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:08:42 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:08:42 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:08:42 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:08:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16320d9283c836a62d9272e2cb8e84c8612aa06a936a9cf278ba966b3357a4c`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f90c6fb80119d2bc1dc27ee2683d38da9d83f89111078f9f270f28f22ccb05`  
		Last Modified: Wed, 06 Apr 2022 00:13:18 GMT  
		Size: 88.7 MB (88652200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f37343862c2a51efaecba778691d93433d0ddbbf84ef37357bc98a1133429`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa17b756af18f9a13ad8317e402deb3c7a53c17c6632478197a40107f1021ee0`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 6.8 KB (6776 bytes)  
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
$ docker pull mariadb@sha256:358ae3debde472507a69d65e290a88fdbe816a2cc69ffe0115a209ed3161a569
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139622368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a50b4ba89e870cceded162d6074694e5135d07bcee48eb50eedd683a021e62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:03:43 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:45 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:46 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:48 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:03:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:06:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:06:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:06:41 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:05 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:15 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52493fd202a8d6cb59b97704e8fd31fac38295f0194a7be438f2585004d25d59`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25bac626de3b7058fa6ec7cebd0de41b7362b2d268b050650846403389a212b`  
		Last Modified: Sat, 19 Mar 2022 21:25:42 GMT  
		Size: 93.4 MB (93406062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f944df55379e651ac7739ce3bce7a4081fd8a310f6007dda05f0247d8d02a0`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf3fff2954922623ddd62fb9dd58a4600e67a9c8d83f3c6d760d4793f70a8a7`  
		Last Modified: Fri, 01 Apr 2022 17:28:44 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:314966e1a6c7a38fe8653d6a3be5553a4b42353ad8b34b056341e890c4d222dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127686087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919d70e6329a9892721648a9dd39a5a09835302ba0b04aa9e4cc2463df17f34c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:30:53 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:30:53 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:30:53 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:30:53 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:30:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:30:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:18 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f98ec61734557d7fe53ae4831cf9f7ed16bc60b1365ea3d29a83f35bd43bc66`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520274d5fa575ea7aca753dc75f2a9838815de72b9fad41ddad7ea499f686a0e`  
		Last Modified: Tue, 05 Apr 2022 23:34:02 GMT  
		Size: 89.8 MB (89779905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833b80a09fe725b06b314eb33ef843216477c3de0142a74b4db388efb00ba1f1`  
		Last Modified: Tue, 05 Apr 2022 23:33:50 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3178924c2c1fc7e52fcc323020393a9a7e15c740600cf17b9fefd660ae6c0775`  
		Last Modified: Tue, 05 Apr 2022 23:33:50 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-rc-focal`

```console
$ docker pull mariadb@sha256:70656b9ebfa172c4eb9667cf6b18ea99a32e895170351828f31750687c85a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-rc-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:8a3a50858a36c77b6551873ccbcba16a33c7f2d2fb5a3b40e3139efc9f7af769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128578743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c252d4bcf31e323c374063f0fa34040bc8118004682f3947e5b4cf8236686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:09 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 00:08:09 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 00:08:09 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 00:08:09 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 00:08:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:08:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:08:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:08:42 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:08:42 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:08:42 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:08:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16320d9283c836a62d9272e2cb8e84c8612aa06a936a9cf278ba966b3357a4c`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f90c6fb80119d2bc1dc27ee2683d38da9d83f89111078f9f270f28f22ccb05`  
		Last Modified: Wed, 06 Apr 2022 00:13:18 GMT  
		Size: 88.7 MB (88652200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f37343862c2a51efaecba778691d93433d0ddbbf84ef37357bc98a1133429`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa17b756af18f9a13ad8317e402deb3c7a53c17c6632478197a40107f1021ee0`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 6.8 KB (6776 bytes)  
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
$ docker pull mariadb@sha256:358ae3debde472507a69d65e290a88fdbe816a2cc69ffe0115a209ed3161a569
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139622368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a50b4ba89e870cceded162d6074694e5135d07bcee48eb50eedd683a021e62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:03:43 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:45 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:46 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:48 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:03:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:06:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:06:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:06:41 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:05 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:15 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52493fd202a8d6cb59b97704e8fd31fac38295f0194a7be438f2585004d25d59`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25bac626de3b7058fa6ec7cebd0de41b7362b2d268b050650846403389a212b`  
		Last Modified: Sat, 19 Mar 2022 21:25:42 GMT  
		Size: 93.4 MB (93406062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f944df55379e651ac7739ce3bce7a4081fd8a310f6007dda05f0247d8d02a0`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf3fff2954922623ddd62fb9dd58a4600e67a9c8d83f3c6d760d4793f70a8a7`  
		Last Modified: Fri, 01 Apr 2022 17:28:44 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:314966e1a6c7a38fe8653d6a3be5553a4b42353ad8b34b056341e890c4d222dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127686087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919d70e6329a9892721648a9dd39a5a09835302ba0b04aa9e4cc2463df17f34c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:30:53 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:30:53 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:30:53 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:30:53 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:30:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:30:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:18 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f98ec61734557d7fe53ae4831cf9f7ed16bc60b1365ea3d29a83f35bd43bc66`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520274d5fa575ea7aca753dc75f2a9838815de72b9fad41ddad7ea499f686a0e`  
		Last Modified: Tue, 05 Apr 2022 23:34:02 GMT  
		Size: 89.8 MB (89779905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833b80a09fe725b06b314eb33ef843216477c3de0142a74b4db388efb00ba1f1`  
		Last Modified: Tue, 05 Apr 2022 23:33:50 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3178924c2c1fc7e52fcc323020393a9a7e15c740600cf17b9fefd660ae6c0775`  
		Last Modified: Tue, 05 Apr 2022 23:33:50 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.2-rc`

```console
$ docker pull mariadb@sha256:70656b9ebfa172c4eb9667cf6b18ea99a32e895170351828f31750687c85a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.2-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:8a3a50858a36c77b6551873ccbcba16a33c7f2d2fb5a3b40e3139efc9f7af769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128578743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c252d4bcf31e323c374063f0fa34040bc8118004682f3947e5b4cf8236686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:09 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 00:08:09 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 00:08:09 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 00:08:09 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 00:08:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:08:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:08:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:08:42 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:08:42 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:08:42 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:08:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16320d9283c836a62d9272e2cb8e84c8612aa06a936a9cf278ba966b3357a4c`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f90c6fb80119d2bc1dc27ee2683d38da9d83f89111078f9f270f28f22ccb05`  
		Last Modified: Wed, 06 Apr 2022 00:13:18 GMT  
		Size: 88.7 MB (88652200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f37343862c2a51efaecba778691d93433d0ddbbf84ef37357bc98a1133429`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa17b756af18f9a13ad8317e402deb3c7a53c17c6632478197a40107f1021ee0`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 6.8 KB (6776 bytes)  
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
$ docker pull mariadb@sha256:358ae3debde472507a69d65e290a88fdbe816a2cc69ffe0115a209ed3161a569
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139622368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a50b4ba89e870cceded162d6074694e5135d07bcee48eb50eedd683a021e62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:03:43 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:45 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:46 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:48 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:03:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:06:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:06:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:06:41 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:05 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:15 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52493fd202a8d6cb59b97704e8fd31fac38295f0194a7be438f2585004d25d59`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25bac626de3b7058fa6ec7cebd0de41b7362b2d268b050650846403389a212b`  
		Last Modified: Sat, 19 Mar 2022 21:25:42 GMT  
		Size: 93.4 MB (93406062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f944df55379e651ac7739ce3bce7a4081fd8a310f6007dda05f0247d8d02a0`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf3fff2954922623ddd62fb9dd58a4600e67a9c8d83f3c6d760d4793f70a8a7`  
		Last Modified: Fri, 01 Apr 2022 17:28:44 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:314966e1a6c7a38fe8653d6a3be5553a4b42353ad8b34b056341e890c4d222dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127686087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919d70e6329a9892721648a9dd39a5a09835302ba0b04aa9e4cc2463df17f34c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:30:53 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:30:53 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:30:53 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:30:53 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:30:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:30:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:18 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f98ec61734557d7fe53ae4831cf9f7ed16bc60b1365ea3d29a83f35bd43bc66`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520274d5fa575ea7aca753dc75f2a9838815de72b9fad41ddad7ea499f686a0e`  
		Last Modified: Tue, 05 Apr 2022 23:34:02 GMT  
		Size: 89.8 MB (89779905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833b80a09fe725b06b314eb33ef843216477c3de0142a74b4db388efb00ba1f1`  
		Last Modified: Tue, 05 Apr 2022 23:33:50 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3178924c2c1fc7e52fcc323020393a9a7e15c740600cf17b9fefd660ae6c0775`  
		Last Modified: Tue, 05 Apr 2022 23:33:50 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.2-rc-focal`

```console
$ docker pull mariadb@sha256:70656b9ebfa172c4eb9667cf6b18ea99a32e895170351828f31750687c85a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.2-rc-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:8a3a50858a36c77b6551873ccbcba16a33c7f2d2fb5a3b40e3139efc9f7af769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128578743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c252d4bcf31e323c374063f0fa34040bc8118004682f3947e5b4cf8236686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:09 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 00:08:09 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 06 Apr 2022 00:08:09 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 00:08:09 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Wed, 06 Apr 2022 00:08:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:08:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:08:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:08:42 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:08:42 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:08:42 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:08:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16320d9283c836a62d9272e2cb8e84c8612aa06a936a9cf278ba966b3357a4c`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f90c6fb80119d2bc1dc27ee2683d38da9d83f89111078f9f270f28f22ccb05`  
		Last Modified: Wed, 06 Apr 2022 00:13:18 GMT  
		Size: 88.7 MB (88652200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f37343862c2a51efaecba778691d93433d0ddbbf84ef37357bc98a1133429`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa17b756af18f9a13ad8317e402deb3c7a53c17c6632478197a40107f1021ee0`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 6.8 KB (6776 bytes)  
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
$ docker pull mariadb@sha256:358ae3debde472507a69d65e290a88fdbe816a2cc69ffe0115a209ed3161a569
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139622368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a50b4ba89e870cceded162d6074694e5135d07bcee48eb50eedd683a021e62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:03:43 GMT
ARG MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:45 GMT
ENV MARIADB_MAJOR=10.8
# Sat, 19 Mar 2022 21:03:46 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:48 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Sat, 19 Mar 2022 21:03:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:03:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:06:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:06:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:06:41 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:05 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:15 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52493fd202a8d6cb59b97704e8fd31fac38295f0194a7be438f2585004d25d59`  
		Last Modified: Sat, 19 Mar 2022 21:25:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25bac626de3b7058fa6ec7cebd0de41b7362b2d268b050650846403389a212b`  
		Last Modified: Sat, 19 Mar 2022 21:25:42 GMT  
		Size: 93.4 MB (93406062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f944df55379e651ac7739ce3bce7a4081fd8a310f6007dda05f0247d8d02a0`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf3fff2954922623ddd62fb9dd58a4600e67a9c8d83f3c6d760d4793f70a8a7`  
		Last Modified: Fri, 01 Apr 2022 17:28:44 GMT  
		Size: 6.8 KB (6774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:314966e1a6c7a38fe8653d6a3be5553a4b42353ad8b34b056341e890c4d222dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127686087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919d70e6329a9892721648a9dd39a5a09835302ba0b04aa9e4cc2463df17f34c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:30:53 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:30:53 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 05 Apr 2022 23:30:53 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:30:53 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Tue, 05 Apr 2022 23:30:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:30:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:18 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f98ec61734557d7fe53ae4831cf9f7ed16bc60b1365ea3d29a83f35bd43bc66`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520274d5fa575ea7aca753dc75f2a9838815de72b9fad41ddad7ea499f686a0e`  
		Last Modified: Tue, 05 Apr 2022 23:34:02 GMT  
		Size: 89.8 MB (89779905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833b80a09fe725b06b314eb33ef843216477c3de0142a74b4db388efb00ba1f1`  
		Last Modified: Tue, 05 Apr 2022 23:33:50 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3178924c2c1fc7e52fcc323020393a9a7e15c740600cf17b9fefd660ae6c0775`  
		Last Modified: Tue, 05 Apr 2022 23:33:50 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:e4421edf721f25823f7a867b231a3b41dda67fcc219ad489a5f646c1f2f8a729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:364e6c38ee64f7f961cc1b70d5c31e554754c4a9fcd6516c9b5c31accf134e61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100166b773f8bdb6f5bfcd16a5ae670bc02ec8a0b6f52f6f74cc560aad592fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ef26c44d0008a5eaeb76320f9509d0728c66ee924af3909910b9e9c8d062`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f6e068c19c3abd463f2e8818220f4304558532ce1eea0ba7e88249533a3de2`  
		Last Modified: Wed, 06 Apr 2022 01:54:00 GMT  
		Size: 88.7 MB (88741687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd25d3e0e6be214d9c5ca5d3597275c41c80a9a551f7aef80ddd34f5f41140`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e322e4875b51e5cf140539cccf19a26d235f52baae4c7cc88024a59f599fe`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 6.8 KB (6775 bytes)  
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
$ docker pull mariadb@sha256:73f1a363d1bd5d67665a2e95e281a6c5f9d60cfc954d37bcc543f4323ea16cb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139540029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3073063783d6646d082607b57b7093f8c0726cc621b6b59d5852a14441fc89b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:39 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2f383467f58f976dd982b1bc6e6fff20f589e60b19d6e00b2a84d8b95c1a7`  
		Last Modified: Fri, 01 Apr 2022 17:29:04 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; s390x

```console
$ docker pull mariadb@sha256:2c2eb9a9fa59f3ddae7a55bd0ddf77e246352438463824741eb92a6a347697e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127721348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5405ba6fc8203440741f811f94a5463c814b05cb550bca60b138a06c6605527b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:31:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8a3bf7f3897df0dfedf0c9629a9a933240987145b59678a8d0d26fac2722de`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2029403953732bae90490466205f4c53ff7e048f32f70a2cbab8d2e089984ded`  
		Last Modified: Tue, 05 Apr 2022 23:34:25 GMT  
		Size: 89.8 MB (89815166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc5f84bad71845209754dbd765377f1bbe548ba402569ff98b4f69425f4f93`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f2fd91a171567a326fb6c302b2a10ac5003b1e43c94400e96a1613d65915f`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:e4421edf721f25823f7a867b231a3b41dda67fcc219ad489a5f646c1f2f8a729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:364e6c38ee64f7f961cc1b70d5c31e554754c4a9fcd6516c9b5c31accf134e61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100166b773f8bdb6f5bfcd16a5ae670bc02ec8a0b6f52f6f74cc560aad592fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 00:07:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 06 Apr 2022 00:07:49 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:07:49 GMT
ENV GOSU_VERSION=1.14
# Wed, 06 Apr 2022 00:08:00 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 00:08:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 00:08:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:08:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 06 Apr 2022 00:08:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 06 Apr 2022 00:08:50 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:50 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Wed, 06 Apr 2022 00:08:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Wed, 06 Apr 2022 00:08:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 06 Apr 2022 00:09:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 06 Apr 2022 00:09:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 06 Apr 2022 00:09:17 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Wed, 06 Apr 2022 00:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 00:09:17 GMT
EXPOSE 3306
# Wed, 06 Apr 2022 00:09:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3f605beb6e6d8a69fa77cf35c30f19e3697eb1a629c189216a2463d6fa627`  
		Last Modified: Wed, 06 Apr 2022 00:13:09 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43298fa9eba9b9af10e0c5835534f8af5769b95eac5d3150dfd7650d27db130`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 5.5 MB (5488531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f565e2a61005e2a95c0216f4d30e537fb026a9c21901b2c986e4e2bfe4e59191`  
		Last Modified: Wed, 06 Apr 2022 00:13:08 GMT  
		Size: 3.6 MB (3584953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5a73a7467f6e1d52270782768ba7b92d60ffc8798b1cbe34ba974f051b8633`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d219b4dd588962eb150c1fbcfcd360bca838da00ec3615063ab0b85060dbcfc2`  
		Last Modified: Wed, 06 Apr 2022 00:13:07 GMT  
		Size: 2.3 MB (2271785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008719f0a8ad66a14f90ddc20a3de8331c55deeed87faafc3461cd91f9946f3a`  
		Last Modified: Wed, 06 Apr 2022 00:13:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ef26c44d0008a5eaeb76320f9509d0728c66ee924af3909910b9e9c8d062`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f6e068c19c3abd463f2e8818220f4304558532ce1eea0ba7e88249533a3de2`  
		Last Modified: Wed, 06 Apr 2022 01:54:00 GMT  
		Size: 88.7 MB (88741687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd25d3e0e6be214d9c5ca5d3597275c41c80a9a551f7aef80ddd34f5f41140`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e322e4875b51e5cf140539cccf19a26d235f52baae4c7cc88024a59f599fe`  
		Last Modified: Wed, 06 Apr 2022 01:53:47 GMT  
		Size: 6.8 KB (6775 bytes)  
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
$ docker pull mariadb@sha256:73f1a363d1bd5d67665a2e95e281a6c5f9d60cfc954d37bcc543f4323ea16cb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139540029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3073063783d6646d082607b57b7093f8c0726cc621b6b59d5852a14441fc89b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:01:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 19 Mar 2022 21:01:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:01:51 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 21:02:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 21:02:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 21:03:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:03:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 19 Mar 2022 21:03:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Sat, 19 Mar 2022 21:06:59 GMT
ARG MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:01 GMT
ENV MARIADB_MAJOR=10.7
# Sat, 19 Mar 2022 21:07:05 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:07 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Sat, 19 Mar 2022 21:07:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Sat, 19 Mar 2022 21:07:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 19 Mar 2022 21:09:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Sat, 19 Mar 2022 21:09:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 21:09:34 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Apr 2022 17:24:30 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Fri, 01 Apr 2022 17:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Apr 2022 17:24:39 GMT
EXPOSE 3306
# Fri, 01 Apr 2022 17:24:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1be58e73011f4a334ec9256f9677dda55f95379597c076edefe60a01d022b`  
		Last Modified: Sat, 19 Mar 2022 21:25:30 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caab03e1db5b14afbca0931d0bbeb76b4de0c786146d1f681b4b6bbe236efe4c`  
		Last Modified: Sat, 19 Mar 2022 21:25:29 GMT  
		Size: 6.7 MB (6667415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be504c611368aa2b19f070f92533babbc1790180fc795b251f474427f80c24f`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 3.7 MB (3672495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75979928052651750fd08b33b82b50272d98913f128e77cb7dc12b13d2fa3`  
		Last Modified: Sat, 19 Mar 2022 21:25:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3ef8ce446aef60c909c915385b8ccaafa5496f8240a9dc55c524513ba197`  
		Last Modified: Sat, 19 Mar 2022 21:25:28 GMT  
		Size: 2.6 MB (2568993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e52d414b40027d9956fbf7e4249c0efe854f63dded23602ab9e8c7d6c37fa7`  
		Last Modified: Sat, 19 Mar 2022 21:25:25 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8869abea296655465c04abf26a10ee0848fea5da59f7ec407b0a7f596be6`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5677525d2f5e652a46dd101d2064472cd666dc8ae6eeedf09afcfbd34ec09fd1`  
		Last Modified: Sat, 19 Mar 2022 21:26:23 GMT  
		Size: 93.3 MB (93323724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedbd30daf0f51dab9938d15e8f851ecd5a03ad4f35e53ee08885a17ac912737`  
		Last Modified: Sat, 19 Mar 2022 21:26:03 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2f383467f58f976dd982b1bc6e6fff20f589e60b19d6e00b2a84d8b95c1a7`  
		Last Modified: Fri, 01 Apr 2022 17:29:04 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:2c2eb9a9fa59f3ddae7a55bd0ddf77e246352438463824741eb92a6a347697e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127721348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5405ba6fc8203440741f811f94a5463c814b05cb550bca60b138a06c6605527b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Apr 2022 23:30:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:35 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Apr 2022 23:30:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:30:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 05 Apr 2022 23:30:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 05 Apr 2022 23:31:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Tue, 05 Apr 2022 23:31:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Tue, 05 Apr 2022 23:31:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 05 Apr 2022 23:31:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 05 Apr 2022 23:31:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 05 Apr 2022 23:31:55 GMT
COPY file:1e9733e3c770304d3250be6325e07d0f6b8ea7fd42808808cc6b2919d42a9a5e in /usr/local/bin/ 
# Tue, 05 Apr 2022 23:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 23:31:55 GMT
EXPOSE 3306
# Tue, 05 Apr 2022 23:31:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786d34b57a58cd7518e3a46e7d187591cf1458ad74d6380f33024ec729e834b0`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d8373979dde48ba3d9429dd5d5d39c6604d65292a96579c78fbe2a6f87c496`  
		Last Modified: Tue, 05 Apr 2022 23:33:52 GMT  
		Size: 5.4 MB (5378415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f35820cae216fb05efdda06e2f5391e49b26397646009f8b3694af3461e01`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 3.2 MB (3243926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a9d79180c5ef4b17c9958a7e061053b49f5d2997f29440c55ed60e24c5eb7`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea044f9e20a121ed51d87937e7fb34c64087c349e279d2fddd1cc8646a449125`  
		Last Modified: Tue, 05 Apr 2022 23:33:51 GMT  
		Size: 2.2 MB (2183950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ee4152b6853f8a55d6a8b9611a6cce5a39adf29e3e44f849d22bb0776312e`  
		Last Modified: Tue, 05 Apr 2022 23:33:49 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8a3bf7f3897df0dfedf0c9629a9a933240987145b59678a8d0d26fac2722de`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2029403953732bae90490466205f4c53ff7e048f32f70a2cbab8d2e089984ded`  
		Last Modified: Tue, 05 Apr 2022 23:34:25 GMT  
		Size: 89.8 MB (89815166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc5f84bad71845209754dbd765377f1bbe548ba402569ff98b4f69425f4f93`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f2fd91a171567a326fb6c302b2a10ac5003b1e43c94400e96a1613d65915f`  
		Last Modified: Tue, 05 Apr 2022 23:34:13 GMT  
		Size: 6.8 KB (6776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
