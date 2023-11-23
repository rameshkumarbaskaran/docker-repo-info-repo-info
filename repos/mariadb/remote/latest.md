## `mariadb:latest`

```console
$ docker pull mariadb@sha256:c222be005ac3f8183dd3c7d1930aebbc4cd8d05d42ba92578174b7a77123efa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:7c58576f7e85def1dab9bf216d2de666c72e724aa4a7cf8c8cd5f1f0935827aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123513127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc7b4dead186c33907b7bdc6416601b2c36cdebbeefc75619baa8fded3fe7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 03:13:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql
# Thu, 23 Nov 2023 10:29:17 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Nov 2023 10:29:17 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 23 Nov 2023 10:29:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Nov 2023 10:29:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Nov 2023 10:29:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Nov 2023 10:30:41 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 23 Nov 2023 10:30:41 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Thu, 23 Nov 2023 10:30:41 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Thu, 23 Nov 2023 10:30:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Thu, 23 Nov 2023 10:30:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 23 Nov 2023 10:30:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 23 Nov 2023 10:31:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Nov 2023 10:31:00 GMT
COPY file:9a446c99b3f95c0895b9c81c454dd5f21965ad984eb9becb89690f77b54d08ae in /usr/local/bin/healthcheck.sh 
# Thu, 23 Nov 2023 10:31:00 GMT
COPY file:96ebfe41373ea3f34aed860f1bdf37a922a980d7c3150314988a012b7b1e0ac1 in /usr/local/bin/ 
# Thu, 23 Nov 2023 10:31:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 10:31:00 GMT
EXPOSE 3306
# Thu, 23 Nov 2023 10:31:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db915624f10afb286704596b86e19742c9037b35a1a72d9c7b1d95a41ee26621`  
		Last Modified: Thu, 16 Nov 2023 03:20:40 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfad94d59a27eb05de2f8d6b8efce745d101b5187ac6798fdd0e52ae17dded01`  
		Last Modified: Thu, 23 Nov 2023 10:35:30 GMT  
		Size: 5.6 MB (5646031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598fd32a3b01d1d0b1d0a860062cd724081b030b04b9a29864753eb6b9087748`  
		Last Modified: Thu, 23 Nov 2023 10:35:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b7c589cbd33fcdbf870e48af2c6a4b5106d49627057aeee4ffaa0df9935d72`  
		Last Modified: Thu, 23 Nov 2023 10:35:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9400913ff3d0a245672792eb9a0261e0e9f46da3e6710a51a48683c8a52380f`  
		Last Modified: Thu, 23 Nov 2023 10:36:04 GMT  
		Size: 87.4 MB (87414283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9eaee49d0d3839ac310c290868466c6d4175be753f8bca4cdaea9898d14a05`  
		Last Modified: Thu, 23 Nov 2023 10:35:52 GMT  
		Size: 3.6 KB (3615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cb178b3bcae9c0b6b6e48556b86832da9de49a56cd1d1e65252d3259a8f874`  
		Last Modified: Thu, 23 Nov 2023 10:35:52 GMT  
		Size: 7.9 KB (7862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c16e82975c27f9606a32123b99bd41a48da66082b6bd75c9ac29743f8c9c6fc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118024134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578fc149b5b6cdcc71b11aa867b5e117fe613a6450e43230035723e48d4e2c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 02:40:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql
# Thu, 23 Nov 2023 09:47:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Nov 2023 09:47:16 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 23 Nov 2023 09:48:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Nov 2023 09:48:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Nov 2023 09:48:02 GMT
ENV LANG=C.UTF-8
# Thu, 23 Nov 2023 09:48:39 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 23 Nov 2023 09:48:39 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Thu, 23 Nov 2023 09:48:39 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Thu, 23 Nov 2023 09:48:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Thu, 23 Nov 2023 09:48:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 23 Nov 2023 09:48:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 23 Nov 2023 09:48:58 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Nov 2023 09:48:58 GMT
COPY file:9a446c99b3f95c0895b9c81c454dd5f21965ad984eb9becb89690f77b54d08ae in /usr/local/bin/healthcheck.sh 
# Thu, 23 Nov 2023 09:48:58 GMT
COPY file:96ebfe41373ea3f34aed860f1bdf37a922a980d7c3150314988a012b7b1e0ac1 in /usr/local/bin/ 
# Thu, 23 Nov 2023 09:48:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 09:48:58 GMT
EXPOSE 3306
# Thu, 23 Nov 2023 09:48:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bfd6232aacadb38909692f1216810e5f58bcc333b7736ed1cb7d166f87202c`  
		Last Modified: Thu, 16 Nov 2023 02:46:24 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9635f8643bf05e06695d05adb1ecbf464ae7a5cdf420d10592045759a5f233`  
		Last Modified: Thu, 23 Nov 2023 09:53:23 GMT  
		Size: 5.5 MB (5462238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18dcba3b402af596079e099146f92758bb602ed4bc4b6f9124a54a642a907a9`  
		Last Modified: Thu, 23 Nov 2023 09:53:21 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be30f636e870500e713f60165fbf5646ac440de6304a6ac5ad89556c11ce89bd`  
		Last Modified: Thu, 23 Nov 2023 09:53:44 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72566af8d2f83213b869e6be321b92ec07161eb0d2324b876aac4514b2955929`  
		Last Modified: Thu, 23 Nov 2023 09:53:53 GMT  
		Size: 84.2 MB (84156255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb99e22385cbe2902094df53ad0721e0e44e2157bac18804daf7cf73744232a`  
		Last Modified: Thu, 23 Nov 2023 09:53:44 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36ecf4cdc33fe6d153e4d4f485abccca9a9dde4b11a41104146a573a009d0ab`  
		Last Modified: Thu, 23 Nov 2023 09:53:44 GMT  
		Size: 7.9 KB (7861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0356ca06736a1239957abf3853ec3ea77a6d718834d211a2477865d96cf24a15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131894100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6af33a7174fafa3aa25e6b34e6edb0cfccc9a6c4cf9c65dd4e7d19127d334d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 05:57:29 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql
# Thu, 23 Nov 2023 10:19:42 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Nov 2023 10:19:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 23 Nov 2023 10:20:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Nov 2023 10:20:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Nov 2023 10:20:34 GMT
ENV LANG=C.UTF-8
# Thu, 23 Nov 2023 10:21:36 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 23 Nov 2023 10:21:37 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Thu, 23 Nov 2023 10:21:37 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Thu, 23 Nov 2023 10:21:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Thu, 23 Nov 2023 10:21:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 23 Nov 2023 10:22:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 23 Nov 2023 10:22:07 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Nov 2023 10:22:07 GMT
COPY file:9a446c99b3f95c0895b9c81c454dd5f21965ad984eb9becb89690f77b54d08ae in /usr/local/bin/healthcheck.sh 
# Thu, 23 Nov 2023 10:22:07 GMT
COPY file:96ebfe41373ea3f34aed860f1bdf37a922a980d7c3150314988a012b7b1e0ac1 in /usr/local/bin/ 
# Thu, 23 Nov 2023 10:22:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 10:22:08 GMT
EXPOSE 3306
# Thu, 23 Nov 2023 10:22:08 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0560a699c960cbb34e0a04f1977b7d4eacb4bf39a969f4799f4186e0d0190a`  
		Last Modified: Thu, 16 Nov 2023 06:05:23 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b388668e97223cd3dc0a7d95ed325016f75bb732f258a9e93c5815388d04f`  
		Last Modified: Thu, 23 Nov 2023 10:29:17 GMT  
		Size: 6.1 MB (6088371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3bdc5b7ed022319ef2adaa075c1dd0333b03f801b7f4cf376e204e1b75f011`  
		Last Modified: Thu, 23 Nov 2023 10:29:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97031bf6cd45b666044c0e9c15ba8462359cb4b74c06ccf5e9161e55ee194ccc`  
		Last Modified: Thu, 23 Nov 2023 10:29:44 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1760db5f65056535c968e44119b7f2fa3087ddf4f20fe4911346f2205a9a3c49`  
		Last Modified: Thu, 23 Nov 2023 10:29:59 GMT  
		Size: 90.1 MB (90109229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046f01702f76fc23ff7178542077ccb20995a8a9a0906809aa26c750bc810fe1`  
		Last Modified: Thu, 23 Nov 2023 10:29:44 GMT  
		Size: 3.6 KB (3616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99954a64311a7d9bd23c19b8ae9cb2301cdb5d8e4e08bf2d30a63a2f6b5f0693`  
		Last Modified: Thu, 23 Nov 2023 10:29:44 GMT  
		Size: 7.9 KB (7863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:0337ce54ff5e6437e8a745816931658938cc4fcae020bff2bf9fb7f6ff1a9cf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122042404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b68b887dac731330f4c34aec32e26cc0890d9ea705ab2f2ba614a43d575071`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Oct 2023 07:29:34 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:29:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:29:36 GMT
ADD file:d165475f8f027ab758a463da57c8c29f5d302f0a87a475ac68fdfae30005c7ac in / 
# Thu, 05 Oct 2023 07:29:36 GMT
CMD ["/bin/bash"]
# Thu, 16 Nov 2023 02:32:57 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql
# Thu, 23 Nov 2023 09:45:36 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Nov 2023 09:45:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 23 Nov 2023 09:46:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Nov 2023 09:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Nov 2023 09:46:06 GMT
ENV LANG=C.UTF-8
# Thu, 23 Nov 2023 09:46:48 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 23 Nov 2023 09:46:48 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Thu, 23 Nov 2023 09:46:48 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Thu, 23 Nov 2023 09:46:48 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Thu, 23 Nov 2023 09:46:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 23 Nov 2023 09:47:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 23 Nov 2023 09:47:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Nov 2023 09:47:12 GMT
COPY file:9a446c99b3f95c0895b9c81c454dd5f21965ad984eb9becb89690f77b54d08ae in /usr/local/bin/healthcheck.sh 
# Thu, 23 Nov 2023 09:47:12 GMT
COPY file:96ebfe41373ea3f34aed860f1bdf37a922a980d7c3150314988a012b7b1e0ac1 in /usr/local/bin/ 
# Thu, 23 Nov 2023 09:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 09:47:13 GMT
EXPOSE 3306
# Thu, 23 Nov 2023 09:47:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:818e4e246beb9ab026d2b95bf051fe9610b92dbc0a35b45d09b0cf237b6f3c2e`  
		Last Modified: Fri, 13 Oct 2023 10:16:45 GMT  
		Size: 28.7 MB (28650497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eaec34821d8eaa6a095ef6e70345e945d226da7e7f888f35a222e5c83c745d2`  
		Last Modified: Thu, 16 Nov 2023 02:39:29 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258384f677e518178732cb57eed82b31d899a71c665681a933fde0343583be7d`  
		Last Modified: Thu, 23 Nov 2023 09:51:57 GMT  
		Size: 5.5 MB (5530996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17aca596197aea45dac01473bb026bc2f0cb28a8bb23ce5721a4249cdef098e0`  
		Last Modified: Thu, 23 Nov 2023 09:51:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ae56e20f75f059fec5e36a582e08f863546e9cac08cf7c35857edf9fddbc41`  
		Last Modified: Thu, 23 Nov 2023 09:52:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c190239ad43d102237f2b7300d0f7f8a25936e288a8f74c6ccba139c0bcdb9e`  
		Last Modified: Thu, 23 Nov 2023 09:52:29 GMT  
		Size: 87.8 MB (87847206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f133c6dadb60999781c4dc650c0537263f4f0dfd3cc9d9c10fb27aa09e016e`  
		Last Modified: Thu, 23 Nov 2023 09:52:16 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb5b753949674f7fa412db8478873a68f71a8317de279fbfbd597640c4f241e`  
		Last Modified: Thu, 23 Nov 2023 09:52:16 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
