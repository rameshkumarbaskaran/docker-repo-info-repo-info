## `mariadb:lts`

```console
$ docker pull mariadb@sha256:0dd97d82bb0a39720cea837f7034378ba8f95cedd39f69bd8bff78856ceeb3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:lts` - linux; amd64

```console
$ docker pull mariadb@sha256:cb15256ad461b9f53a37c787ab49518fa22333c5272cbf65fe0302712b3cb918
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125443369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b68210cde00565ecaab2486667323aa4d2e6726954344218782d3ed12b64c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:21:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 02 Jun 2023 01:21:14 GMT
ENV GOSU_VERSION=1.14
# Fri, 02 Jun 2023 01:21:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 02 Jun 2023 01:21:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Jun 2023 01:21:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Jun 2023 01:21:35 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jun 2023 21:30:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 09 Jun 2023 21:30:21 GMT
ARG MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Fri, 09 Jun 2023 21:30:21 GMT
ENV MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Fri, 09 Jun 2023 21:30:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
# Fri, 09 Jun 2023 21:30:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 09 Jun 2023 21:30:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 09 Jun 2023 21:30:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 09 Jun 2023 21:30:44 GMT
COPY file:cee75098a882f7d33ad2c4c4325b29adc56fc66450e6cee3711d5a1af1bda714 in /usr/local/bin/healthcheck.sh 
# Fri, 09 Jun 2023 21:30:44 GMT
COPY file:cb2b72015a5493e1348f12f52b387586b863bcc87072708862e1aa2af0493eb9 in /usr/local/bin/ 
# Fri, 09 Jun 2023 21:30:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jun 2023 21:30:44 GMT
EXPOSE 3306
# Fri, 09 Jun 2023 21:30:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7942299fe584ae926671d6e010bc59c3ea5e651742cfc7af2488c50fa2daa05f`  
		Last Modified: Fri, 02 Jun 2023 01:24:14 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca116927bbe123aec204718cb63664b2dc19d357b1b6dd7958a354c4b5b3879c`  
		Last Modified: Fri, 02 Jun 2023 01:24:15 GMT  
		Size: 5.6 MB (5592249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0f0b5293ed6194c5d04bf423e3222e39553df6db49e7f775ff6af7c44b92e6`  
		Last Modified: Fri, 02 Jun 2023 01:24:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc618b0ec836d7b31f3aef55d2c55b4f2aabaf000f1dd4ebaf3308f13b7b783`  
		Last Modified: Fri, 09 Jun 2023 21:34:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0c97845923fa015f743f09395fcbcd655d69040955c088403bcecadc1fb248`  
		Last Modified: Fri, 09 Jun 2023 21:35:09 GMT  
		Size: 89.4 MB (89407786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822e5a6b2469b2c63fc9ff398ca76526d3fb170fb92af1221d0f91d3b7fe0421`  
		Last Modified: Fri, 09 Jun 2023 21:34:55 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601fec5a80db939fed90f4543a9c6b3ffbee9003b18048f971eab1ca0b7a232`  
		Last Modified: Fri, 09 Jun 2023 21:34:55 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:59e1bbc4ca2c79816bc946dc72d9db03aed0f9927ff31e23872f71799a30a35d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119887838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85146da97f7a403b57fe05e8c4a5fd97c63d393f9237aed7db2f63efbd0e0796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:40:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 01 Jun 2023 23:40:52 GMT
ENV GOSU_VERSION=1.14
# Thu, 01 Jun 2023 23:40:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 01 Jun 2023 23:41:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 01 Jun 2023 23:41:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 01 Jun 2023 23:41:08 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jun 2023 20:23:32 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 09 Jun 2023 20:23:32 GMT
ARG MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Fri, 09 Jun 2023 20:23:32 GMT
ENV MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Fri, 09 Jun 2023 20:23:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
# Fri, 09 Jun 2023 20:23:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 09 Jun 2023 20:23:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 09 Jun 2023 20:23:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 09 Jun 2023 20:23:54 GMT
COPY file:cee75098a882f7d33ad2c4c4325b29adc56fc66450e6cee3711d5a1af1bda714 in /usr/local/bin/healthcheck.sh 
# Fri, 09 Jun 2023 20:23:54 GMT
COPY file:cb2b72015a5493e1348f12f52b387586b863bcc87072708862e1aa2af0493eb9 in /usr/local/bin/ 
# Fri, 09 Jun 2023 20:23:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jun 2023 20:23:54 GMT
EXPOSE 3306
# Fri, 09 Jun 2023 20:23:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3beef926275df9bcc0f302dcc80b1df1778597e3762c0bcba4aba7cb6640680`  
		Last Modified: Thu, 01 Jun 2023 23:43:36 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd40ffbb6cb3906cf4feaa019e5002505b5aa18f7fc6fc78552fe0499d3b56b0`  
		Last Modified: Thu, 01 Jun 2023 23:43:37 GMT  
		Size: 5.4 MB (5405164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31691bc52e3b474eb0509035feef6f06782d2807ad942714f4d3830b8c5aa1b0`  
		Last Modified: Thu, 01 Jun 2023 23:43:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1239de71c01cf93b88288756589e55028aa68f779a1c4da283efb464c576abe3`  
		Last Modified: Fri, 09 Jun 2023 20:27:54 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaea62cab8cb4df9762d75fbb422abbe8ec46cad4120c2639b267e45bfc9b25`  
		Last Modified: Fri, 09 Jun 2023 20:28:04 GMT  
		Size: 86.1 MB (86080567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f969f5c85911499f73e3f332c835f968b18d01ff67ecf9d8a724543f5e44937f`  
		Last Modified: Fri, 09 Jun 2023 20:27:54 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a097d827a377e20de0a2ef028ab549c4ae19e6648727269d35ca0f650826c48`  
		Last Modified: Fri, 09 Jun 2023 20:27:54 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:82a440caad4ea71f23840babafd266fbf7159373bfb42173de30a7fb16c2cd49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134277140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f36efd7c55a47e0f3d544862860a2ec09f7a1352e2e28e2e560170747befd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 22 May 2023 17:39:12 GMT
ARG RELEASE
# Mon, 22 May 2023 17:39:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:39:16 GMT
ADD file:5b5967ce188eac9717526ca9f6cf6679cbae6ee4b17b207cc3d640c78d9a9788 in / 
# Mon, 22 May 2023 17:39:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:52:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 02 Jun 2023 00:52:55 GMT
ENV GOSU_VERSION=1.14
# Fri, 02 Jun 2023 00:52:56 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 02 Jun 2023 00:53:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Jun 2023 00:53:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Jun 2023 00:53:50 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jun 2023 21:23:19 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 09 Jun 2023 21:23:19 GMT
ARG MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Fri, 09 Jun 2023 21:23:19 GMT
ENV MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Fri, 09 Jun 2023 21:23:19 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
# Fri, 09 Jun 2023 21:23:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 09 Jun 2023 21:24:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 09 Jun 2023 21:24:21 GMT
VOLUME [/var/lib/mysql]
# Fri, 09 Jun 2023 21:24:21 GMT
COPY file:cee75098a882f7d33ad2c4c4325b29adc56fc66450e6cee3711d5a1af1bda714 in /usr/local/bin/healthcheck.sh 
# Fri, 09 Jun 2023 21:24:22 GMT
COPY file:cb2b72015a5493e1348f12f52b387586b863bcc87072708862e1aa2af0493eb9 in /usr/local/bin/ 
# Fri, 09 Jun 2023 21:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jun 2023 21:24:22 GMT
EXPOSE 3306
# Fri, 09 Jun 2023 21:24:23 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e39d2517f3d915af1b821fe306b14eba12466c4cae87efe57eaa0b749503166e`  
		Last Modified: Thu, 01 Jun 2023 23:48:51 GMT  
		Size: 35.7 MB (35712704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae535de25882dc500766d8c6be1fb20fd97d90dc3a52a7444c461520c31733`  
		Last Modified: Fri, 02 Jun 2023 01:01:13 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd64c95ab82d6c8ebe9a3a6cd0cf06a0b03eb01041b0e048943c783032c2b0af`  
		Last Modified: Fri, 02 Jun 2023 01:01:14 GMT  
		Size: 6.0 MB (6017762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7f7998247131a5d2e685a4f5966d34e0abe6c134ac739b5984f99901cfcc81`  
		Last Modified: Fri, 02 Jun 2023 01:01:10 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6182014ff5543de954be51c760182848c14e6fab7ce8a317fcdf07eaef7bd9a`  
		Last Modified: Fri, 09 Jun 2023 21:32:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93b33385661cb130f4dcad74093ea3c0d5599977e622856b3169b4bce0b8ee1`  
		Last Modified: Fri, 09 Jun 2023 21:33:18 GMT  
		Size: 92.5 MB (92533611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f354a36b67bc8d11b3e6e9c37e7833914b1bb4cf244c9fdaea8eb5a0238b12`  
		Last Modified: Fri, 09 Jun 2023 21:32:54 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae9bf0100261c9c98d61f38ae8a2a2da7be20f6f43792eb896c1a32d8fd14f9`  
		Last Modified: Fri, 09 Jun 2023 21:32:53 GMT  
		Size: 7.3 KB (7311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
