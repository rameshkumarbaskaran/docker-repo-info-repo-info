<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-jammy`](#mariadb10-jammy)
-	[`mariadb:10.10-rc`](#mariadb1010-rc)
-	[`mariadb:10.10-rc-jammy`](#mariadb1010-rc-jammy)
-	[`mariadb:10.10.1-rc`](#mariadb10101-rc)
-	[`mariadb:10.10.1-rc-jammy`](#mariadb10101-rc-jammy)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.36`](#mariadb10336)
-	[`mariadb:10.3.36-focal`](#mariadb10336-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.26`](#mariadb10426)
-	[`mariadb:10.4.26-focal`](#mariadb10426-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.17`](#mariadb10517)
-	[`mariadb:10.5.17-focal`](#mariadb10517-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.9`](#mariadb1069)
-	[`mariadb:10.6.9-focal`](#mariadb1069-focal)
-	[`mariadb:10.7`](#mariadb107)
-	[`mariadb:10.7-focal`](#mariadb107-focal)
-	[`mariadb:10.7.5`](#mariadb1075)
-	[`mariadb:10.7.5-focal`](#mariadb1075-focal)
-	[`mariadb:10.8`](#mariadb108)
-	[`mariadb:10.8-jammy`](#mariadb108-jammy)
-	[`mariadb:10.8.4`](#mariadb1084)
-	[`mariadb:10.8.4-jammy`](#mariadb1084-jammy)
-	[`mariadb:10.9`](#mariadb109)
-	[`mariadb:10.9-jammy`](#mariadb109-jammy)
-	[`mariadb:10.9.2`](#mariadb1092)
-	[`mariadb:10.9.2-jammy`](#mariadb1092-jammy)
-	[`mariadb:jammy`](#mariadbjammy)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:cbcf33d6dab0a014dfc9450148f3dcf42c8ae77635b3c8e948e3af09562a989e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:3b4bcc98c0982745a30b013e8b66233c7313496eae9de6b691963a737f614d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124029543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d138caf7d0f7680129a9dd134f363a23da6be5d76449a93bb5906598d0e06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:02 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:23 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:24 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:24 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710253f0933b7c0e3be3f7a4b4b77cb5ba9ece744177ccbb68472b8b46ce122b`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d5115199c9aa41cc86312e841f5ac0ff84a38ead396deb3ee0a54b01b973b`  
		Last Modified: Wed, 24 Aug 2022 00:07:58 GMT  
		Size: 85.5 MB (85531548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f43d7b59b546061df8a538a2cd4376a400245c54955445749e405d33098d73`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7032a660a4eef799097fd44e9d6a7ae89c6f5a3bb148c9f6515f8b1f800f46`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1f011a0b21919b39058355d972fea445857869ad1f867eb56bd1d274fd969e88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102470825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f8da7eeabb6549ac946f2b45ffe497556f6ad227d0bd4d41e09e73e6b34097`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:32:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:32:16 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:32:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:32:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:32:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:32:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:33:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:29 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:30 GMT
ARG MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:31 GMT
ENV MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
# Tue, 02 Aug 2022 18:33:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:33:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:33:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:33:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:33:55 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:33:56 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:33:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5bedaed5f8e5343fee312eb2f21894d7b4026a0c692da89fe4f30a432e48b4`  
		Last Modified: Tue, 02 Aug 2022 18:41:32 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f07d81dfa02553c544d772dc3aa04ed6a2e6ad5b810ca742eee9a918786e5f`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 3.6 MB (3594051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b8a20cb609d07274a17b8dd4ae810b6a98f76cf0ad513aa0c03eda46fcbce`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 1.9 MB (1899200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d39cfcf2768f9c1165cc0d3764c3649542f541a1ed3f18bec6283d58553e00`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d230566e80222a9242f97419a6018684f4e324420ee89e4c0395f8107a124c91`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 2.2 MB (2211614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c8c9abaef706c6185822ae21205ab5bc569494c4492a89eef44d8a855315c5`  
		Last Modified: Tue, 02 Aug 2022 18:41:27 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bff43ba5b5f6479659a8a7496d4156615c3cd9439c46779dd3feed3c4511ae`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cb73ef10f93c31f677c6818187b24c6bb65b4cb76ad5ed05e5b31853ef1b73`  
		Last Modified: Tue, 02 Aug 2022 18:42:08 GMT  
		Size: 66.4 MB (66369985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b16804fca7957e5cc3538c9a1a58af3e8e7a9eb0ee3318ffa413c7ebf4c76d4`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffad21dfd527f8685de9b3c864738e88bb8791db49ecdeb988d9d194a20d7cc`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b68e6672e1dfd013fc5b4fb42b368c534af7e07fce685f287b3a99296e09b2bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117038959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d753a037ef6f672b98d11a6b2b3ddd116a81dea34be15c6b9a40c05fecbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:12:28 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:12:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:13:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:13:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:13:16 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caabbd107834c8bff1673ba81491e0983e459aabc2855d3cf78188307c813365`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3bd7204dda4f3ab271317d058dfb5ef33dfcf95bf4b663c30432f03f3fc3fc`  
		Last Modified: Tue, 23 Aug 2022 22:23:28 GMT  
		Size: 72.5 MB (72476332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c727c5cc2517b4755a4205d2b008e2454929862a191ba73a55c1dca7f58e1`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714083977b193354161a308393ac0d56d68efc4be6cb3d26edfff12859e0a23e`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; s390x

```console
$ docker pull mariadb@sha256:c7116a14d5deca65bec93cec3a99662a47f1d1c85330b3aefa2b5610f932d26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105140532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ac87f204e8050170fd16b50ad4652cc817bd6d937b569cb01e04580d15fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:01 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:56:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:56:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:56:36 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:56:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab6e11c25e790046065da17a078d6f1068e0d5f9988a46f3ec1a381810189c`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6ddbdfd315c17604dd29c4cceec21edcd2a1f5b6de90cb34814ec25f1d944`  
		Last Modified: Tue, 23 Aug 2022 23:05:50 GMT  
		Size: 68.6 MB (68634999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814afb85a75d500819281410f8832949cdfeb711ca835ef097214003f8f058a8`  
		Last Modified: Tue, 23 Aug 2022 23:05:41 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673619860a5c62749b0f25f505cc892fb9cc9d5cedfb493a12a10520c01b57d8`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:cbcf33d6dab0a014dfc9450148f3dcf42c8ae77635b3c8e948e3af09562a989e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:3b4bcc98c0982745a30b013e8b66233c7313496eae9de6b691963a737f614d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124029543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d138caf7d0f7680129a9dd134f363a23da6be5d76449a93bb5906598d0e06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:02 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:23 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:24 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:24 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710253f0933b7c0e3be3f7a4b4b77cb5ba9ece744177ccbb68472b8b46ce122b`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d5115199c9aa41cc86312e841f5ac0ff84a38ead396deb3ee0a54b01b973b`  
		Last Modified: Wed, 24 Aug 2022 00:07:58 GMT  
		Size: 85.5 MB (85531548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f43d7b59b546061df8a538a2cd4376a400245c54955445749e405d33098d73`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7032a660a4eef799097fd44e9d6a7ae89c6f5a3bb148c9f6515f8b1f800f46`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1f011a0b21919b39058355d972fea445857869ad1f867eb56bd1d274fd969e88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102470825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f8da7eeabb6549ac946f2b45ffe497556f6ad227d0bd4d41e09e73e6b34097`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:32:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:32:16 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:32:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:32:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:32:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:32:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:33:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:29 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:30 GMT
ARG MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:31 GMT
ENV MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
# Tue, 02 Aug 2022 18:33:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:33:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:33:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:33:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:33:55 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:33:56 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:33:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5bedaed5f8e5343fee312eb2f21894d7b4026a0c692da89fe4f30a432e48b4`  
		Last Modified: Tue, 02 Aug 2022 18:41:32 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f07d81dfa02553c544d772dc3aa04ed6a2e6ad5b810ca742eee9a918786e5f`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 3.6 MB (3594051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b8a20cb609d07274a17b8dd4ae810b6a98f76cf0ad513aa0c03eda46fcbce`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 1.9 MB (1899200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d39cfcf2768f9c1165cc0d3764c3649542f541a1ed3f18bec6283d58553e00`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d230566e80222a9242f97419a6018684f4e324420ee89e4c0395f8107a124c91`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 2.2 MB (2211614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c8c9abaef706c6185822ae21205ab5bc569494c4492a89eef44d8a855315c5`  
		Last Modified: Tue, 02 Aug 2022 18:41:27 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bff43ba5b5f6479659a8a7496d4156615c3cd9439c46779dd3feed3c4511ae`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cb73ef10f93c31f677c6818187b24c6bb65b4cb76ad5ed05e5b31853ef1b73`  
		Last Modified: Tue, 02 Aug 2022 18:42:08 GMT  
		Size: 66.4 MB (66369985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b16804fca7957e5cc3538c9a1a58af3e8e7a9eb0ee3318ffa413c7ebf4c76d4`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffad21dfd527f8685de9b3c864738e88bb8791db49ecdeb988d9d194a20d7cc`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b68e6672e1dfd013fc5b4fb42b368c534af7e07fce685f287b3a99296e09b2bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117038959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d753a037ef6f672b98d11a6b2b3ddd116a81dea34be15c6b9a40c05fecbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:12:28 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:12:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:13:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:13:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:13:16 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caabbd107834c8bff1673ba81491e0983e459aabc2855d3cf78188307c813365`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3bd7204dda4f3ab271317d058dfb5ef33dfcf95bf4b663c30432f03f3fc3fc`  
		Last Modified: Tue, 23 Aug 2022 22:23:28 GMT  
		Size: 72.5 MB (72476332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c727c5cc2517b4755a4205d2b008e2454929862a191ba73a55c1dca7f58e1`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714083977b193354161a308393ac0d56d68efc4be6cb3d26edfff12859e0a23e`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:c7116a14d5deca65bec93cec3a99662a47f1d1c85330b3aefa2b5610f932d26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105140532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ac87f204e8050170fd16b50ad4652cc817bd6d937b569cb01e04580d15fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:01 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:56:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:56:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:56:36 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:56:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab6e11c25e790046065da17a078d6f1068e0d5f9988a46f3ec1a381810189c`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6ddbdfd315c17604dd29c4cceec21edcd2a1f5b6de90cb34814ec25f1d944`  
		Last Modified: Tue, 23 Aug 2022 23:05:50 GMT  
		Size: 68.6 MB (68634999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814afb85a75d500819281410f8832949cdfeb711ca835ef097214003f8f058a8`  
		Last Modified: Tue, 23 Aug 2022 23:05:41 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673619860a5c62749b0f25f505cc892fb9cc9d5cedfb493a12a10520c01b57d8`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.10-rc`

```console
$ docker pull mariadb@sha256:427035b910d6238bda799b2b4c3ac1b26bf7499e0a5292e1793ee3960dd844e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.10-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:64c8be6e656a4320829ba9d3b3f052160ef1c74a122508fb0cc3a1096f8204d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127882774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87138b3733ac59872ce10b5672310dd342a8e99a06e924c65bd5562d4ece2062`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:01:07 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 24 Aug 2022 00:01:07 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 24 Aug 2022 00:01:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:01:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:01:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:01:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:01:46 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:01:46 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:01:46 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:01:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546f9ab3e5294f2a9e4fafebec90eb3f2e00b9ddae9a7d9fb1465138c796654b`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2775b6ec4359a5f65feeaccbbcc05e71c3745b980a86999df48517794f113`  
		Last Modified: Wed, 24 Aug 2022 00:07:28 GMT  
		Size: 89.4 MB (89384778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff7285ea135356895fa1d5cbb2e6b4480bb62783db0122a0b782b9c94b176a`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cf514781d25f30c03bd0220623043030a9af007c47b904ab2b6819ae94207f`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:dba83e82253f9bf189703dd3af384e15ecb267fa6671db8b40c3dc5e5a714db0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118887052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ea742e5e3f1f3420b83c5650a9f95b58f01529dc2cd7589386cf6826709d68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:11:03 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:11:04 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:11:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:11:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:12:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:12:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:12:08 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:12:09 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:12:09 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:12:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7b4cc95f92e441659596c4d0878320d0c5cd80061c3d233972aa82e0f7e3e3`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dcec4c0e04471040b07c0643cea7ebd8e8adf437e91cd27d6e21a79de5c5a`  
		Last Modified: Tue, 23 Aug 2022 22:22:49 GMT  
		Size: 74.3 MB (74324420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b393e87ea77fc26b71f39e35967ec34476c38b48ce37913c881ffbcbda1317b`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30fec2e86bc42a5a4fc17e149b9888260f554af5a2f8796fbd229bcbf6200dc`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:13b6dfbb1aeb2c969bcd533558ef4af12f0a2965ddca74710917d5a5e0599975
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107319252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b29b6aff2ff879e146054daf8d3b7807f0953f2c7b30393391208c0e108c91d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:55:14 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:55:14 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:55:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:55:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:55:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:55:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:55:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:55:53 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:55:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:55:53 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:55:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dabf875364e913a9aba468f2303f59542f64ba670d572b487e1ec7d265d6ed`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a8c88e4b34df16ec6072c968fb1006132cbc5b379e021bfc3350d152ea5934`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 70.8 MB (70813712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7033fb7bb94aa0c5824fe0d9e941e424a4d7c5d3c7252fe9c272be40b7d7463a`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d87b1d01bc5cc67fdbaeb45d10978783445ccb387bbbaf90a34a42a78921c83`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.10-rc-jammy`

```console
$ docker pull mariadb@sha256:427035b910d6238bda799b2b4c3ac1b26bf7499e0a5292e1793ee3960dd844e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.10-rc-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:64c8be6e656a4320829ba9d3b3f052160ef1c74a122508fb0cc3a1096f8204d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127882774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87138b3733ac59872ce10b5672310dd342a8e99a06e924c65bd5562d4ece2062`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:01:07 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 24 Aug 2022 00:01:07 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 24 Aug 2022 00:01:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:01:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:01:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:01:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:01:46 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:01:46 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:01:46 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:01:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546f9ab3e5294f2a9e4fafebec90eb3f2e00b9ddae9a7d9fb1465138c796654b`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2775b6ec4359a5f65feeaccbbcc05e71c3745b980a86999df48517794f113`  
		Last Modified: Wed, 24 Aug 2022 00:07:28 GMT  
		Size: 89.4 MB (89384778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff7285ea135356895fa1d5cbb2e6b4480bb62783db0122a0b782b9c94b176a`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cf514781d25f30c03bd0220623043030a9af007c47b904ab2b6819ae94207f`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:dba83e82253f9bf189703dd3af384e15ecb267fa6671db8b40c3dc5e5a714db0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118887052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ea742e5e3f1f3420b83c5650a9f95b58f01529dc2cd7589386cf6826709d68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:11:03 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:11:04 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:11:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:11:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:12:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:12:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:12:08 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:12:09 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:12:09 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:12:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7b4cc95f92e441659596c4d0878320d0c5cd80061c3d233972aa82e0f7e3e3`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dcec4c0e04471040b07c0643cea7ebd8e8adf437e91cd27d6e21a79de5c5a`  
		Last Modified: Tue, 23 Aug 2022 22:22:49 GMT  
		Size: 74.3 MB (74324420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b393e87ea77fc26b71f39e35967ec34476c38b48ce37913c881ffbcbda1317b`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30fec2e86bc42a5a4fc17e149b9888260f554af5a2f8796fbd229bcbf6200dc`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:13b6dfbb1aeb2c969bcd533558ef4af12f0a2965ddca74710917d5a5e0599975
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107319252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b29b6aff2ff879e146054daf8d3b7807f0953f2c7b30393391208c0e108c91d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:55:14 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:55:14 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:55:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:55:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:55:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:55:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:55:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:55:53 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:55:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:55:53 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:55:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dabf875364e913a9aba468f2303f59542f64ba670d572b487e1ec7d265d6ed`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a8c88e4b34df16ec6072c968fb1006132cbc5b379e021bfc3350d152ea5934`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 70.8 MB (70813712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7033fb7bb94aa0c5824fe0d9e941e424a4d7c5d3c7252fe9c272be40b7d7463a`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d87b1d01bc5cc67fdbaeb45d10978783445ccb387bbbaf90a34a42a78921c83`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.10.1-rc`

```console
$ docker pull mariadb@sha256:427035b910d6238bda799b2b4c3ac1b26bf7499e0a5292e1793ee3960dd844e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.10.1-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:64c8be6e656a4320829ba9d3b3f052160ef1c74a122508fb0cc3a1096f8204d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127882774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87138b3733ac59872ce10b5672310dd342a8e99a06e924c65bd5562d4ece2062`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:01:07 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 24 Aug 2022 00:01:07 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 24 Aug 2022 00:01:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:01:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:01:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:01:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:01:46 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:01:46 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:01:46 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:01:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546f9ab3e5294f2a9e4fafebec90eb3f2e00b9ddae9a7d9fb1465138c796654b`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2775b6ec4359a5f65feeaccbbcc05e71c3745b980a86999df48517794f113`  
		Last Modified: Wed, 24 Aug 2022 00:07:28 GMT  
		Size: 89.4 MB (89384778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff7285ea135356895fa1d5cbb2e6b4480bb62783db0122a0b782b9c94b176a`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cf514781d25f30c03bd0220623043030a9af007c47b904ab2b6819ae94207f`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:dba83e82253f9bf189703dd3af384e15ecb267fa6671db8b40c3dc5e5a714db0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118887052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ea742e5e3f1f3420b83c5650a9f95b58f01529dc2cd7589386cf6826709d68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:11:03 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:11:04 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:11:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:11:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:12:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:12:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:12:08 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:12:09 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:12:09 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:12:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7b4cc95f92e441659596c4d0878320d0c5cd80061c3d233972aa82e0f7e3e3`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dcec4c0e04471040b07c0643cea7ebd8e8adf437e91cd27d6e21a79de5c5a`  
		Last Modified: Tue, 23 Aug 2022 22:22:49 GMT  
		Size: 74.3 MB (74324420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b393e87ea77fc26b71f39e35967ec34476c38b48ce37913c881ffbcbda1317b`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30fec2e86bc42a5a4fc17e149b9888260f554af5a2f8796fbd229bcbf6200dc`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:13b6dfbb1aeb2c969bcd533558ef4af12f0a2965ddca74710917d5a5e0599975
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107319252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b29b6aff2ff879e146054daf8d3b7807f0953f2c7b30393391208c0e108c91d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:55:14 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:55:14 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:55:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:55:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:55:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:55:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:55:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:55:53 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:55:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:55:53 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:55:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dabf875364e913a9aba468f2303f59542f64ba670d572b487e1ec7d265d6ed`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a8c88e4b34df16ec6072c968fb1006132cbc5b379e021bfc3350d152ea5934`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 70.8 MB (70813712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7033fb7bb94aa0c5824fe0d9e941e424a4d7c5d3c7252fe9c272be40b7d7463a`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d87b1d01bc5cc67fdbaeb45d10978783445ccb387bbbaf90a34a42a78921c83`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.10.1-rc-jammy`

```console
$ docker pull mariadb@sha256:427035b910d6238bda799b2b4c3ac1b26bf7499e0a5292e1793ee3960dd844e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.10.1-rc-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:64c8be6e656a4320829ba9d3b3f052160ef1c74a122508fb0cc3a1096f8204d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127882774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87138b3733ac59872ce10b5672310dd342a8e99a06e924c65bd5562d4ece2062`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:01:07 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 24 Aug 2022 00:01:07 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 24 Aug 2022 00:01:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:01:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:01:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:01:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:01:46 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:01:46 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:01:46 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:01:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546f9ab3e5294f2a9e4fafebec90eb3f2e00b9ddae9a7d9fb1465138c796654b`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2775b6ec4359a5f65feeaccbbcc05e71c3745b980a86999df48517794f113`  
		Last Modified: Wed, 24 Aug 2022 00:07:28 GMT  
		Size: 89.4 MB (89384778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff7285ea135356895fa1d5cbb2e6b4480bb62783db0122a0b782b9c94b176a`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cf514781d25f30c03bd0220623043030a9af007c47b904ab2b6819ae94207f`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:dba83e82253f9bf189703dd3af384e15ecb267fa6671db8b40c3dc5e5a714db0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118887052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ea742e5e3f1f3420b83c5650a9f95b58f01529dc2cd7589386cf6826709d68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:11:03 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:11:04 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:11:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:11:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:12:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:12:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:12:08 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:12:09 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:12:09 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:12:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7b4cc95f92e441659596c4d0878320d0c5cd80061c3d233972aa82e0f7e3e3`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dcec4c0e04471040b07c0643cea7ebd8e8adf437e91cd27d6e21a79de5c5a`  
		Last Modified: Tue, 23 Aug 2022 22:22:49 GMT  
		Size: 74.3 MB (74324420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b393e87ea77fc26b71f39e35967ec34476c38b48ce37913c881ffbcbda1317b`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30fec2e86bc42a5a4fc17e149b9888260f554af5a2f8796fbd229bcbf6200dc`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:13b6dfbb1aeb2c969bcd533558ef4af12f0a2965ddca74710917d5a5e0599975
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107319252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b29b6aff2ff879e146054daf8d3b7807f0953f2c7b30393391208c0e108c91d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:55:14 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:55:14 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Tue, 23 Aug 2022 22:55:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:55:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:55:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:55:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:55:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:55:53 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:55:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:55:53 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:55:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dabf875364e913a9aba468f2303f59542f64ba670d572b487e1ec7d265d6ed`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a8c88e4b34df16ec6072c968fb1006132cbc5b379e021bfc3350d152ea5934`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 70.8 MB (70813712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7033fb7bb94aa0c5824fe0d9e941e424a4d7c5d3c7252fe9c272be40b7d7463a`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d87b1d01bc5cc67fdbaeb45d10978783445ccb387bbbaf90a34a42a78921c83`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:e55a5365cdfd180f8a7b9fe44d45ae6f8e62bee58adb0e171611ac3a14001e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:7587392a0197a9dda40786830ea70f928cb611f6fe5323c7a51172148415490f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120237612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5180fe03860c4c69121bed9ae035e078a19a6c07d11e76a965af5b8e8694d3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:06:06 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 24 Aug 2022 00:06:06 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 24 Aug 2022 00:06:06 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 24 Aug 2022 00:06:06 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 24 Aug 2022 00:06:06 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:06:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:06:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:06:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:06:36 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:06:36 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:06:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Aug 2022 00:06:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:06:37 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:06:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a05a8e93401aafba6e7266d20e1c04218d15d3f3d0917663728871cf3f27f91`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a045152b690b07c180cfde4114c21c292ed71c2fdfdc382cc5e78a2d7f367c`  
		Last Modified: Wed, 24 Aug 2022 00:11:04 GMT  
		Size: 80.3 MB (80306580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81449c6b091b0e52ccce11a589c1ed0c74beee02e70f0e7ae06868066e152e`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 3.5 KB (3498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a098796feadda72dfdd7e905e055c3bb35011fa62fe9ec5e3390932734dfd6f`  
		Last Modified: Wed, 24 Aug 2022 00:10:51 GMT  
		Size: 6.7 KB (6696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04bde84aa33b4c23d115bea0349073383fe680978ffd614c2f515191ea0ea76`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:18549782c1a9df3a37ab79f67e538a6863da0f70d9852e7b599845b7ad024d4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117652395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c5915a308fc62e110563674a326679102264146f728b6f4c10fc1ad56c78aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:37:31 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 02 Aug 2022 18:37:32 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 02 Aug 2022 18:37:33 GMT
ARG MARIADB_VERSION=1:10.3.35+maria~focal
# Tue, 02 Aug 2022 18:37:34 GMT
ENV MARIADB_VERSION=1:10.3.35+maria~focal
# Tue, 02 Aug 2022 18:37:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.35/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:37:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.35/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:38:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.35/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:38:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:38:09 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:38:10 GMT
COPY file:8104832da3dca41b18cf5ee1150e1522c4186f2e9a7f0fdf71d0277ac04ea849 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:38:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.35/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 02 Aug 2022 18:38:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:38:12 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:38:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4c6aca326cfd011967dc8cb41ffb93985998d801314ee6f71eae226c38b05f`  
		Last Modified: Tue, 02 Aug 2022 18:44:52 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d04251488d4f1aaccf2214e3ec64d06665fb736d5340f4eda42256e4763e0b6`  
		Last Modified: Tue, 02 Aug 2022 18:45:05 GMT  
		Size: 79.6 MB (79552791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b467d949890eaaa3738bc5f2fe0fa7b5a3f2cc0da3de58c4c67d172a5b4b18`  
		Last Modified: Tue, 02 Aug 2022 18:44:52 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9c894b5b7813a8c73743f44905b618b8a3676dcd6fe043766c67296088df78`  
		Last Modified: Tue, 02 Aug 2022 18:44:52 GMT  
		Size: 6.7 KB (6691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b4305bbf6f97e7b626d11ee17c5a49af91e459e8efe2a43933e66b0d81ca0b`  
		Last Modified: Tue, 02 Aug 2022 18:44:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:900c2cd2b2f99c051c6e19fcc7de85daa06fd00abe41321f7cce1389f1c759c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131124241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97417f4fbf7907f9c484edf6b5cb19cc7a15593ccc0add47e05702701d555aaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:20:00 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 23 Aug 2022 22:20:00 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 23 Aug 2022 22:20:00 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 23 Aug 2022 22:20:01 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 23 Aug 2022 22:20:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:20:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:20:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:20:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:20:54 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:20:54 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:20:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 23 Aug 2022 22:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:20:56 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:20:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ac726788ee94c6dac27a3bc1cd060198fb6a70e29ae290cf028db39a004251`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af6d0c7d8bb1fb0bb3604b0e597587cbfa9bcf624942437f24d845effc928a`  
		Last Modified: Tue, 23 Aug 2022 22:28:08 GMT  
		Size: 84.9 MB (84907437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f088b14a05532d1b38f828b2e01678ae9fb005f44de1e19c0c23413ffbf81ce9`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07aee49157f22d647b69df59a878c2b5b7cb44890fe74181a191eef636870c7`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb4ad0c14e4129175671257a8e1c55ebea759510b499e94d12c36b6d1a9c75f`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:e55a5365cdfd180f8a7b9fe44d45ae6f8e62bee58adb0e171611ac3a14001e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7587392a0197a9dda40786830ea70f928cb611f6fe5323c7a51172148415490f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120237612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5180fe03860c4c69121bed9ae035e078a19a6c07d11e76a965af5b8e8694d3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:06:06 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 24 Aug 2022 00:06:06 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 24 Aug 2022 00:06:06 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 24 Aug 2022 00:06:06 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 24 Aug 2022 00:06:06 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:06:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:06:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:06:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:06:36 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:06:36 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:06:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Aug 2022 00:06:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:06:37 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:06:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a05a8e93401aafba6e7266d20e1c04218d15d3f3d0917663728871cf3f27f91`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a045152b690b07c180cfde4114c21c292ed71c2fdfdc382cc5e78a2d7f367c`  
		Last Modified: Wed, 24 Aug 2022 00:11:04 GMT  
		Size: 80.3 MB (80306580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81449c6b091b0e52ccce11a589c1ed0c74beee02e70f0e7ae06868066e152e`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 3.5 KB (3498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a098796feadda72dfdd7e905e055c3bb35011fa62fe9ec5e3390932734dfd6f`  
		Last Modified: Wed, 24 Aug 2022 00:10:51 GMT  
		Size: 6.7 KB (6696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04bde84aa33b4c23d115bea0349073383fe680978ffd614c2f515191ea0ea76`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:18549782c1a9df3a37ab79f67e538a6863da0f70d9852e7b599845b7ad024d4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117652395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c5915a308fc62e110563674a326679102264146f728b6f4c10fc1ad56c78aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:37:31 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 02 Aug 2022 18:37:32 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 02 Aug 2022 18:37:33 GMT
ARG MARIADB_VERSION=1:10.3.35+maria~focal
# Tue, 02 Aug 2022 18:37:34 GMT
ENV MARIADB_VERSION=1:10.3.35+maria~focal
# Tue, 02 Aug 2022 18:37:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.35/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:37:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.35/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:38:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.35/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:38:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:38:09 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:38:10 GMT
COPY file:8104832da3dca41b18cf5ee1150e1522c4186f2e9a7f0fdf71d0277ac04ea849 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:38:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.35/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 02 Aug 2022 18:38:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:38:12 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:38:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4c6aca326cfd011967dc8cb41ffb93985998d801314ee6f71eae226c38b05f`  
		Last Modified: Tue, 02 Aug 2022 18:44:52 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d04251488d4f1aaccf2214e3ec64d06665fb736d5340f4eda42256e4763e0b6`  
		Last Modified: Tue, 02 Aug 2022 18:45:05 GMT  
		Size: 79.6 MB (79552791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b467d949890eaaa3738bc5f2fe0fa7b5a3f2cc0da3de58c4c67d172a5b4b18`  
		Last Modified: Tue, 02 Aug 2022 18:44:52 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9c894b5b7813a8c73743f44905b618b8a3676dcd6fe043766c67296088df78`  
		Last Modified: Tue, 02 Aug 2022 18:44:52 GMT  
		Size: 6.7 KB (6691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b4305bbf6f97e7b626d11ee17c5a49af91e459e8efe2a43933e66b0d81ca0b`  
		Last Modified: Tue, 02 Aug 2022 18:44:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:900c2cd2b2f99c051c6e19fcc7de85daa06fd00abe41321f7cce1389f1c759c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131124241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97417f4fbf7907f9c484edf6b5cb19cc7a15593ccc0add47e05702701d555aaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:20:00 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 23 Aug 2022 22:20:00 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 23 Aug 2022 22:20:00 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 23 Aug 2022 22:20:01 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 23 Aug 2022 22:20:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:20:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:20:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:20:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:20:54 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:20:54 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:20:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 23 Aug 2022 22:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:20:56 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:20:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ac726788ee94c6dac27a3bc1cd060198fb6a70e29ae290cf028db39a004251`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af6d0c7d8bb1fb0bb3604b0e597587cbfa9bcf624942437f24d845effc928a`  
		Last Modified: Tue, 23 Aug 2022 22:28:08 GMT  
		Size: 84.9 MB (84907437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f088b14a05532d1b38f828b2e01678ae9fb005f44de1e19c0c23413ffbf81ce9`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07aee49157f22d647b69df59a878c2b5b7cb44890fe74181a191eef636870c7`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb4ad0c14e4129175671257a8e1c55ebea759510b499e94d12c36b6d1a9c75f`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.36`

```console
$ docker pull mariadb@sha256:b50c1017dfe27187f1fdee0f3d46c77a2d3ece66083ad616d179a9ac9ccb2843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `mariadb:10.3.36` - linux; amd64

```console
$ docker pull mariadb@sha256:7587392a0197a9dda40786830ea70f928cb611f6fe5323c7a51172148415490f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120237612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5180fe03860c4c69121bed9ae035e078a19a6c07d11e76a965af5b8e8694d3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:06:06 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 24 Aug 2022 00:06:06 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 24 Aug 2022 00:06:06 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 24 Aug 2022 00:06:06 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 24 Aug 2022 00:06:06 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:06:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:06:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:06:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:06:36 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:06:36 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:06:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Aug 2022 00:06:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:06:37 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:06:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a05a8e93401aafba6e7266d20e1c04218d15d3f3d0917663728871cf3f27f91`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a045152b690b07c180cfde4114c21c292ed71c2fdfdc382cc5e78a2d7f367c`  
		Last Modified: Wed, 24 Aug 2022 00:11:04 GMT  
		Size: 80.3 MB (80306580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81449c6b091b0e52ccce11a589c1ed0c74beee02e70f0e7ae06868066e152e`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 3.5 KB (3498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a098796feadda72dfdd7e905e055c3bb35011fa62fe9ec5e3390932734dfd6f`  
		Last Modified: Wed, 24 Aug 2022 00:10:51 GMT  
		Size: 6.7 KB (6696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04bde84aa33b4c23d115bea0349073383fe680978ffd614c2f515191ea0ea76`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.36` - linux; ppc64le

```console
$ docker pull mariadb@sha256:900c2cd2b2f99c051c6e19fcc7de85daa06fd00abe41321f7cce1389f1c759c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131124241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97417f4fbf7907f9c484edf6b5cb19cc7a15593ccc0add47e05702701d555aaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:20:00 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 23 Aug 2022 22:20:00 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 23 Aug 2022 22:20:00 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 23 Aug 2022 22:20:01 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 23 Aug 2022 22:20:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:20:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:20:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:20:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:20:54 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:20:54 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:20:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 23 Aug 2022 22:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:20:56 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:20:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ac726788ee94c6dac27a3bc1cd060198fb6a70e29ae290cf028db39a004251`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af6d0c7d8bb1fb0bb3604b0e597587cbfa9bcf624942437f24d845effc928a`  
		Last Modified: Tue, 23 Aug 2022 22:28:08 GMT  
		Size: 84.9 MB (84907437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f088b14a05532d1b38f828b2e01678ae9fb005f44de1e19c0c23413ffbf81ce9`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07aee49157f22d647b69df59a878c2b5b7cb44890fe74181a191eef636870c7`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb4ad0c14e4129175671257a8e1c55ebea759510b499e94d12c36b6d1a9c75f`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.36-focal`

```console
$ docker pull mariadb@sha256:b50c1017dfe27187f1fdee0f3d46c77a2d3ece66083ad616d179a9ac9ccb2843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `mariadb:10.3.36-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7587392a0197a9dda40786830ea70f928cb611f6fe5323c7a51172148415490f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120237612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5180fe03860c4c69121bed9ae035e078a19a6c07d11e76a965af5b8e8694d3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:06:06 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 24 Aug 2022 00:06:06 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 24 Aug 2022 00:06:06 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 24 Aug 2022 00:06:06 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 24 Aug 2022 00:06:06 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:06:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:06:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:06:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:06:36 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:06:36 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:06:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Aug 2022 00:06:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:06:37 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:06:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a05a8e93401aafba6e7266d20e1c04218d15d3f3d0917663728871cf3f27f91`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a045152b690b07c180cfde4114c21c292ed71c2fdfdc382cc5e78a2d7f367c`  
		Last Modified: Wed, 24 Aug 2022 00:11:04 GMT  
		Size: 80.3 MB (80306580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81449c6b091b0e52ccce11a589c1ed0c74beee02e70f0e7ae06868066e152e`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 3.5 KB (3498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a098796feadda72dfdd7e905e055c3bb35011fa62fe9ec5e3390932734dfd6f`  
		Last Modified: Wed, 24 Aug 2022 00:10:51 GMT  
		Size: 6.7 KB (6696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04bde84aa33b4c23d115bea0349073383fe680978ffd614c2f515191ea0ea76`  
		Last Modified: Wed, 24 Aug 2022 00:10:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.36-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:900c2cd2b2f99c051c6e19fcc7de85daa06fd00abe41321f7cce1389f1c759c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131124241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97417f4fbf7907f9c484edf6b5cb19cc7a15593ccc0add47e05702701d555aaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:20:00 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 23 Aug 2022 22:20:00 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 23 Aug 2022 22:20:00 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 23 Aug 2022 22:20:01 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 23 Aug 2022 22:20:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:20:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:20:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:20:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:20:54 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:20:54 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:20:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 23 Aug 2022 22:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:20:56 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:20:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ac726788ee94c6dac27a3bc1cd060198fb6a70e29ae290cf028db39a004251`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af6d0c7d8bb1fb0bb3604b0e597587cbfa9bcf624942437f24d845effc928a`  
		Last Modified: Tue, 23 Aug 2022 22:28:08 GMT  
		Size: 84.9 MB (84907437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f088b14a05532d1b38f828b2e01678ae9fb005f44de1e19c0c23413ffbf81ce9`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07aee49157f22d647b69df59a878c2b5b7cb44890fe74181a191eef636870c7`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb4ad0c14e4129175671257a8e1c55ebea759510b499e94d12c36b6d1a9c75f`  
		Last Modified: Tue, 23 Aug 2022 22:27:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:a3e0999fe37bdeb74118c4f380273ff26d07597403e9e87c1252559f1b6013f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:25154234172a82f7ee134b73b88db334f4ddec7230a94a209ebe8533ecd91ec3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125849013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552982c09ae73a35c77cb3e759e7c74cbc7e0899c752564c32df7d8bb0ca9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:05:32 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 24 Aug 2022 00:05:32 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 24 Aug 2022 00:05:32 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 24 Aug 2022 00:05:32 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 24 Aug 2022 00:05:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:05:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:58 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:58 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Aug 2022 00:05:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:59 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2552b41fd3170763cd6730bcd526f3708ccb29467f639d6ab97da75dc824e744`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12978af61d05a88717c8d70e6aa301362a8a06581fcf1708b25f8af93f71635c`  
		Last Modified: Wed, 24 Aug 2022 00:10:35 GMT  
		Size: 85.9 MB (85917988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270fdaafcd3dd5ed5868e8e8469da32743b512afa5cea9c550e1b5817a7a9cb`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf7a36b65c8bfd8da4d79232754bd7281091a2da2fc88a1c73d8513a01beab3`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9a9a4751d9df1490ea3fab14b9bedb903439b71b3375fcb9e7b851c97149fc`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:97897537f890e470e3a7806246da3e8b691f6d09d27fcd11d1bd54c3bdba03b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123180506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe065923b0e402aa9415226696adc919ccf6b73dab5c241051009043354aa1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:36:47 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 02 Aug 2022 18:36:48 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 02 Aug 2022 18:36:49 GMT
ARG MARIADB_VERSION=1:10.4.25+maria~focal
# Tue, 02 Aug 2022 18:36:50 GMT
ENV MARIADB_VERSION=1:10.4.25+maria~focal
# Tue, 02 Aug 2022 18:36:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.25/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:36:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.25/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:37:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.25/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:37:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:37:21 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:37:22 GMT
COPY file:8104832da3dca41b18cf5ee1150e1522c4186f2e9a7f0fdf71d0277ac04ea849 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:37:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.25/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 02 Aug 2022 18:37:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:37:24 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:37:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46350097da153c5f72fd94bcc96a40c6dffea0abdbcd8cd65797ed11dda312b`  
		Last Modified: Tue, 02 Aug 2022 18:44:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920d4559b118ac750a4b59f7b885180e7a59ecb12cc6cdbe60548297af15b90f`  
		Last Modified: Tue, 02 Aug 2022 18:44:33 GMT  
		Size: 85.1 MB (85080897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b324fa9127800969dc3e44a1af4b2bdd04bf1ea54c4040cae76ac608fff2ec6`  
		Last Modified: Tue, 02 Aug 2022 18:44:20 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c5507189d9fdc9e229de8b6283cad1935c0dd407d89d09bd6d7a58803cc39`  
		Last Modified: Tue, 02 Aug 2022 18:44:20 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce51aa6efeb81f3e9cb4a09f171f97ca8f97f25c54f096905dc29ed804b4b555`  
		Last Modified: Tue, 02 Aug 2022 18:44:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9ba179c3b6bfce9dcc63e9f12938128ba61a0529b89cfb5c3fda5c2b5e2f33f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136729982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57bf80669b30252d5eefeb57bec49ca941a83d6e5bbebf9fe056af5f757cf08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:19:00 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 23 Aug 2022 22:19:00 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 23 Aug 2022 22:19:01 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 23 Aug 2022 22:19:01 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 23 Aug 2022 22:19:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:19:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:19:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:19:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:19:50 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 23 Aug 2022 22:19:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:19:51 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:19:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9ad18639cccfbccb4dcc7a09c6050ea48c5b9f8e795c062b1946ab1c727abd`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1688cc9a72c89fa2f204e50578120ecca3f506c79d9e7643a981c3cf67e91`  
		Last Modified: Tue, 23 Aug 2022 22:27:26 GMT  
		Size: 90.5 MB (90513182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316641a00525632b25b2447646ba7c59966b14b1ff85a04078652c518a33fb63`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c63de9a17e18fbe1dfbb8cc1a07bb79453133877eb20c68f5d5af9bb63434d`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fa2f5694db7fe16ca23232121acb69c189afd2a17ea4db5beaf4f626cb0618`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:a3e0999fe37bdeb74118c4f380273ff26d07597403e9e87c1252559f1b6013f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:25154234172a82f7ee134b73b88db334f4ddec7230a94a209ebe8533ecd91ec3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125849013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552982c09ae73a35c77cb3e759e7c74cbc7e0899c752564c32df7d8bb0ca9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:05:32 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 24 Aug 2022 00:05:32 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 24 Aug 2022 00:05:32 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 24 Aug 2022 00:05:32 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 24 Aug 2022 00:05:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:05:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:58 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:58 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Aug 2022 00:05:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:59 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2552b41fd3170763cd6730bcd526f3708ccb29467f639d6ab97da75dc824e744`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12978af61d05a88717c8d70e6aa301362a8a06581fcf1708b25f8af93f71635c`  
		Last Modified: Wed, 24 Aug 2022 00:10:35 GMT  
		Size: 85.9 MB (85917988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270fdaafcd3dd5ed5868e8e8469da32743b512afa5cea9c550e1b5817a7a9cb`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf7a36b65c8bfd8da4d79232754bd7281091a2da2fc88a1c73d8513a01beab3`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9a9a4751d9df1490ea3fab14b9bedb903439b71b3375fcb9e7b851c97149fc`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:97897537f890e470e3a7806246da3e8b691f6d09d27fcd11d1bd54c3bdba03b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123180506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe065923b0e402aa9415226696adc919ccf6b73dab5c241051009043354aa1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:36:47 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 02 Aug 2022 18:36:48 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 02 Aug 2022 18:36:49 GMT
ARG MARIADB_VERSION=1:10.4.25+maria~focal
# Tue, 02 Aug 2022 18:36:50 GMT
ENV MARIADB_VERSION=1:10.4.25+maria~focal
# Tue, 02 Aug 2022 18:36:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.25/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:36:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.25/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:37:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.25/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:37:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:37:21 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:37:22 GMT
COPY file:8104832da3dca41b18cf5ee1150e1522c4186f2e9a7f0fdf71d0277ac04ea849 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:37:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.25/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 02 Aug 2022 18:37:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:37:24 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:37:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46350097da153c5f72fd94bcc96a40c6dffea0abdbcd8cd65797ed11dda312b`  
		Last Modified: Tue, 02 Aug 2022 18:44:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920d4559b118ac750a4b59f7b885180e7a59ecb12cc6cdbe60548297af15b90f`  
		Last Modified: Tue, 02 Aug 2022 18:44:33 GMT  
		Size: 85.1 MB (85080897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b324fa9127800969dc3e44a1af4b2bdd04bf1ea54c4040cae76ac608fff2ec6`  
		Last Modified: Tue, 02 Aug 2022 18:44:20 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c5507189d9fdc9e229de8b6283cad1935c0dd407d89d09bd6d7a58803cc39`  
		Last Modified: Tue, 02 Aug 2022 18:44:20 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce51aa6efeb81f3e9cb4a09f171f97ca8f97f25c54f096905dc29ed804b4b555`  
		Last Modified: Tue, 02 Aug 2022 18:44:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9ba179c3b6bfce9dcc63e9f12938128ba61a0529b89cfb5c3fda5c2b5e2f33f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136729982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57bf80669b30252d5eefeb57bec49ca941a83d6e5bbebf9fe056af5f757cf08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:19:00 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 23 Aug 2022 22:19:00 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 23 Aug 2022 22:19:01 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 23 Aug 2022 22:19:01 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 23 Aug 2022 22:19:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:19:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:19:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:19:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:19:50 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 23 Aug 2022 22:19:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:19:51 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:19:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9ad18639cccfbccb4dcc7a09c6050ea48c5b9f8e795c062b1946ab1c727abd`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1688cc9a72c89fa2f204e50578120ecca3f506c79d9e7643a981c3cf67e91`  
		Last Modified: Tue, 23 Aug 2022 22:27:26 GMT  
		Size: 90.5 MB (90513182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316641a00525632b25b2447646ba7c59966b14b1ff85a04078652c518a33fb63`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c63de9a17e18fbe1dfbb8cc1a07bb79453133877eb20c68f5d5af9bb63434d`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fa2f5694db7fe16ca23232121acb69c189afd2a17ea4db5beaf4f626cb0618`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.26`

```console
$ docker pull mariadb@sha256:d6d0a78efa4cd1035a471659667a9c4ef1449aeb7856122e828cddeebb21483a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `mariadb:10.4.26` - linux; amd64

```console
$ docker pull mariadb@sha256:25154234172a82f7ee134b73b88db334f4ddec7230a94a209ebe8533ecd91ec3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125849013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552982c09ae73a35c77cb3e759e7c74cbc7e0899c752564c32df7d8bb0ca9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:05:32 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 24 Aug 2022 00:05:32 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 24 Aug 2022 00:05:32 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 24 Aug 2022 00:05:32 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 24 Aug 2022 00:05:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:05:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:58 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:58 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Aug 2022 00:05:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:59 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2552b41fd3170763cd6730bcd526f3708ccb29467f639d6ab97da75dc824e744`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12978af61d05a88717c8d70e6aa301362a8a06581fcf1708b25f8af93f71635c`  
		Last Modified: Wed, 24 Aug 2022 00:10:35 GMT  
		Size: 85.9 MB (85917988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270fdaafcd3dd5ed5868e8e8469da32743b512afa5cea9c550e1b5817a7a9cb`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf7a36b65c8bfd8da4d79232754bd7281091a2da2fc88a1c73d8513a01beab3`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9a9a4751d9df1490ea3fab14b9bedb903439b71b3375fcb9e7b851c97149fc`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.26` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9ba179c3b6bfce9dcc63e9f12938128ba61a0529b89cfb5c3fda5c2b5e2f33f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136729982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57bf80669b30252d5eefeb57bec49ca941a83d6e5bbebf9fe056af5f757cf08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:19:00 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 23 Aug 2022 22:19:00 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 23 Aug 2022 22:19:01 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 23 Aug 2022 22:19:01 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 23 Aug 2022 22:19:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:19:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:19:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:19:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:19:50 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 23 Aug 2022 22:19:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:19:51 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:19:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9ad18639cccfbccb4dcc7a09c6050ea48c5b9f8e795c062b1946ab1c727abd`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1688cc9a72c89fa2f204e50578120ecca3f506c79d9e7643a981c3cf67e91`  
		Last Modified: Tue, 23 Aug 2022 22:27:26 GMT  
		Size: 90.5 MB (90513182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316641a00525632b25b2447646ba7c59966b14b1ff85a04078652c518a33fb63`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c63de9a17e18fbe1dfbb8cc1a07bb79453133877eb20c68f5d5af9bb63434d`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fa2f5694db7fe16ca23232121acb69c189afd2a17ea4db5beaf4f626cb0618`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.26-focal`

```console
$ docker pull mariadb@sha256:d6d0a78efa4cd1035a471659667a9c4ef1449aeb7856122e828cddeebb21483a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `mariadb:10.4.26-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:25154234172a82f7ee134b73b88db334f4ddec7230a94a209ebe8533ecd91ec3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125849013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552982c09ae73a35c77cb3e759e7c74cbc7e0899c752564c32df7d8bb0ca9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:05:32 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 24 Aug 2022 00:05:32 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 24 Aug 2022 00:05:32 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 24 Aug 2022 00:05:32 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 24 Aug 2022 00:05:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:05:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:58 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:58 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Aug 2022 00:05:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:59 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2552b41fd3170763cd6730bcd526f3708ccb29467f639d6ab97da75dc824e744`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12978af61d05a88717c8d70e6aa301362a8a06581fcf1708b25f8af93f71635c`  
		Last Modified: Wed, 24 Aug 2022 00:10:35 GMT  
		Size: 85.9 MB (85917988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270fdaafcd3dd5ed5868e8e8469da32743b512afa5cea9c550e1b5817a7a9cb`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf7a36b65c8bfd8da4d79232754bd7281091a2da2fc88a1c73d8513a01beab3`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9a9a4751d9df1490ea3fab14b9bedb903439b71b3375fcb9e7b851c97149fc`  
		Last Modified: Wed, 24 Aug 2022 00:10:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.26-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9ba179c3b6bfce9dcc63e9f12938128ba61a0529b89cfb5c3fda5c2b5e2f33f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136729982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57bf80669b30252d5eefeb57bec49ca941a83d6e5bbebf9fe056af5f757cf08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:19:00 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 23 Aug 2022 22:19:00 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 23 Aug 2022 22:19:01 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 23 Aug 2022 22:19:01 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 23 Aug 2022 22:19:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:19:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:19:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:19:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:19:50 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:19:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 23 Aug 2022 22:19:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:19:51 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:19:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9ad18639cccfbccb4dcc7a09c6050ea48c5b9f8e795c062b1946ab1c727abd`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1688cc9a72c89fa2f204e50578120ecca3f506c79d9e7643a981c3cf67e91`  
		Last Modified: Tue, 23 Aug 2022 22:27:26 GMT  
		Size: 90.5 MB (90513182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316641a00525632b25b2447646ba7c59966b14b1ff85a04078652c518a33fb63`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c63de9a17e18fbe1dfbb8cc1a07bb79453133877eb20c68f5d5af9bb63434d`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fa2f5694db7fe16ca23232121acb69c189afd2a17ea4db5beaf4f626cb0618`  
		Last Modified: Tue, 23 Aug 2022 22:27:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:9993a5c7bdd272f3d23f0b8fe892fab8b8bca2638ff33de6fd3cfbb5feb686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:81fddfb9e720dab6ec04fdfb18404ac18670fe167a31d1239f7b693feef497c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128149865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccda2dddb6f80fe36ae056da0a7cccc4035de579c29c39a2339fc54299ef4b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:05:04 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 24 Aug 2022 00:05:04 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 24 Aug 2022 00:05:04 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 24 Aug 2022 00:05:04 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 24 Aug 2022 00:05:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:05:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:29 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:29 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:29 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6691d7f6adee381afc9d4d314f7637d83bf2e0fe70e20367aa712369f5d08ea`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94af741c6194d329aba944a401b0a648e28c60f15eb3a69e6352bb2b78f9885c`  
		Last Modified: Wed, 24 Aug 2022 00:10:05 GMT  
		Size: 88.2 MB (88218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fdb9c66fb5f9ce80221e2e4eb7cb12e3716507e84dec2246a1d0b8d30c84be`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2114e556255ea8ad33591210e8a17b28231cbc9e72b447d07c584414075e172a`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 6.7 KB (6692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:598ef479e99feea2749a234780c80def9b7ae5bc9b5f5a62400052f480b70ce3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125345920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ff76a6fdcb615fc7a9e59ea1fb855f5844aafc946634f62d70a60f43ef6875`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:36:10 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 02 Aug 2022 18:36:10 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 02 Aug 2022 18:36:11 GMT
ARG MARIADB_VERSION=1:10.5.16+maria~focal
# Tue, 02 Aug 2022 18:36:12 GMT
ENV MARIADB_VERSION=1:10.5.16+maria~focal
# Tue, 02 Aug 2022 18:36:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.16/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:36:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.16/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:36:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.16/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:36:36 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:36:38 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:36:39 GMT
COPY file:8104832da3dca41b18cf5ee1150e1522c4186f2e9a7f0fdf71d0277ac04ea849 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:36:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:36:40 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:36:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aa7230fd929e56b7fcd0d101bdd8d8b73add7b2720289ed00e6674a544ab1e`  
		Last Modified: Tue, 02 Aug 2022 18:43:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea1eeff7908e7408838d82d32ed8cb66888856b2921cec73825eeaa4a69f4e2`  
		Last Modified: Tue, 02 Aug 2022 18:43:58 GMT  
		Size: 87.2 MB (87246433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679315a9b306139817f609532ddfbd3b84d9b45e98992e4394e27c2aff6a432`  
		Last Modified: Tue, 02 Aug 2022 18:43:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74c1d7b93dc0c7ec4f06651ead1e8661eb86245a1a2f321e2f24509aa29721b`  
		Last Modified: Tue, 02 Aug 2022 18:43:45 GMT  
		Size: 6.7 KB (6692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:157fec64111a52fc2cfbaf5266e08cf5717cee2889b7388c25fc7e46a0c7a9e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139003968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7295a9fac6430bebdfa902cd910709aceeec14bdaf270d653fc0435dc5c98885`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:18:00 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:18:01 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:18:01 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:18:01 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:18:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:18:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:18:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:18:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:18:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:18:49 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:18:49 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:18:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b133d4f0ec8f84ed744d953b45c9aabbf93e623e4755870d4d01b1f94cf8b294`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a956d492c4a0ef2ee94d0b158b21ad1bc92ab1ed1db412e3d7989cdc59c593d`  
		Last Modified: Tue, 23 Aug 2022 22:26:41 GMT  
		Size: 92.8 MB (92787291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c12ee8bc68e45a474cd378d2cf47305884458cb918140f8677ae465b7362517`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0890efea0b238ba6d42d6d0cce09ab28c9fe275fff82bcf86be479d2b126f6b7`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 6.7 KB (6694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:9c1d326b8a032cd9f76c9154d466f98732d42efc24d4f561264b7fb3c5b8af9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127366738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e580c6d254bf14fc5cd5fba2607dd4e5cd732307d4ebd32e3d7ed4665f3ed69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:59:48 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:59:48 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:59:49 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:59:49 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:59:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:59:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 23:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 23:00:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 23:00:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 23:00:49 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 23:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 23:00:50 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 23:00:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e5ce27f8f25a0844bb97a243fa1163416d7f9f24d07f253d5db95c16798ab`  
		Last Modified: Tue, 23 Aug 2022 23:19:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c084be3dfe747df64b34478d369a5136126529e3eebd4ee2bf4f38ff42b401e`  
		Last Modified: Tue, 23 Aug 2022 23:19:52 GMT  
		Size: 89.5 MB (89509543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312bc47786b12ce9a3d80bd8d11f5009ecc62e7797dfb7b0ad1165b26873708`  
		Last Modified: Tue, 23 Aug 2022 23:19:40 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e518bbdf7633214c876cfbda75fbaa46e04712d455aea0775bb26844ddd3a227`  
		Last Modified: Tue, 23 Aug 2022 23:19:39 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:9993a5c7bdd272f3d23f0b8fe892fab8b8bca2638ff33de6fd3cfbb5feb686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:81fddfb9e720dab6ec04fdfb18404ac18670fe167a31d1239f7b693feef497c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128149865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccda2dddb6f80fe36ae056da0a7cccc4035de579c29c39a2339fc54299ef4b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:05:04 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 24 Aug 2022 00:05:04 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 24 Aug 2022 00:05:04 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 24 Aug 2022 00:05:04 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 24 Aug 2022 00:05:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:05:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:29 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:29 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:29 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6691d7f6adee381afc9d4d314f7637d83bf2e0fe70e20367aa712369f5d08ea`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94af741c6194d329aba944a401b0a648e28c60f15eb3a69e6352bb2b78f9885c`  
		Last Modified: Wed, 24 Aug 2022 00:10:05 GMT  
		Size: 88.2 MB (88218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fdb9c66fb5f9ce80221e2e4eb7cb12e3716507e84dec2246a1d0b8d30c84be`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2114e556255ea8ad33591210e8a17b28231cbc9e72b447d07c584414075e172a`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 6.7 KB (6692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:598ef479e99feea2749a234780c80def9b7ae5bc9b5f5a62400052f480b70ce3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125345920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ff76a6fdcb615fc7a9e59ea1fb855f5844aafc946634f62d70a60f43ef6875`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:36:10 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 02 Aug 2022 18:36:10 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 02 Aug 2022 18:36:11 GMT
ARG MARIADB_VERSION=1:10.5.16+maria~focal
# Tue, 02 Aug 2022 18:36:12 GMT
ENV MARIADB_VERSION=1:10.5.16+maria~focal
# Tue, 02 Aug 2022 18:36:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.16/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:36:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.16/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:36:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.16/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:36:36 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:36:38 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:36:39 GMT
COPY file:8104832da3dca41b18cf5ee1150e1522c4186f2e9a7f0fdf71d0277ac04ea849 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:36:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:36:40 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:36:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aa7230fd929e56b7fcd0d101bdd8d8b73add7b2720289ed00e6674a544ab1e`  
		Last Modified: Tue, 02 Aug 2022 18:43:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea1eeff7908e7408838d82d32ed8cb66888856b2921cec73825eeaa4a69f4e2`  
		Last Modified: Tue, 02 Aug 2022 18:43:58 GMT  
		Size: 87.2 MB (87246433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679315a9b306139817f609532ddfbd3b84d9b45e98992e4394e27c2aff6a432`  
		Last Modified: Tue, 02 Aug 2022 18:43:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74c1d7b93dc0c7ec4f06651ead1e8661eb86245a1a2f321e2f24509aa29721b`  
		Last Modified: Tue, 02 Aug 2022 18:43:45 GMT  
		Size: 6.7 KB (6692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:157fec64111a52fc2cfbaf5266e08cf5717cee2889b7388c25fc7e46a0c7a9e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139003968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7295a9fac6430bebdfa902cd910709aceeec14bdaf270d653fc0435dc5c98885`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:18:00 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:18:01 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:18:01 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:18:01 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:18:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:18:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:18:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:18:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:18:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:18:49 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:18:49 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:18:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b133d4f0ec8f84ed744d953b45c9aabbf93e623e4755870d4d01b1f94cf8b294`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a956d492c4a0ef2ee94d0b158b21ad1bc92ab1ed1db412e3d7989cdc59c593d`  
		Last Modified: Tue, 23 Aug 2022 22:26:41 GMT  
		Size: 92.8 MB (92787291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c12ee8bc68e45a474cd378d2cf47305884458cb918140f8677ae465b7362517`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0890efea0b238ba6d42d6d0cce09ab28c9fe275fff82bcf86be479d2b126f6b7`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 6.7 KB (6694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:9c1d326b8a032cd9f76c9154d466f98732d42efc24d4f561264b7fb3c5b8af9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127366738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e580c6d254bf14fc5cd5fba2607dd4e5cd732307d4ebd32e3d7ed4665f3ed69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:59:48 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:59:48 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:59:49 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:59:49 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:59:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:59:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 23:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 23:00:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 23:00:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 23:00:49 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 23:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 23:00:50 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 23:00:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e5ce27f8f25a0844bb97a243fa1163416d7f9f24d07f253d5db95c16798ab`  
		Last Modified: Tue, 23 Aug 2022 23:19:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c084be3dfe747df64b34478d369a5136126529e3eebd4ee2bf4f38ff42b401e`  
		Last Modified: Tue, 23 Aug 2022 23:19:52 GMT  
		Size: 89.5 MB (89509543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312bc47786b12ce9a3d80bd8d11f5009ecc62e7797dfb7b0ad1165b26873708`  
		Last Modified: Tue, 23 Aug 2022 23:19:40 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e518bbdf7633214c876cfbda75fbaa46e04712d455aea0775bb26844ddd3a227`  
		Last Modified: Tue, 23 Aug 2022 23:19:39 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.17`

```console
$ docker pull mariadb@sha256:ee617df6a460abc8078b6911986bf3af1e1e44c740fc0e5a9e79d04f47170fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.17` - linux; amd64

```console
$ docker pull mariadb@sha256:81fddfb9e720dab6ec04fdfb18404ac18670fe167a31d1239f7b693feef497c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128149865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccda2dddb6f80fe36ae056da0a7cccc4035de579c29c39a2339fc54299ef4b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:05:04 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 24 Aug 2022 00:05:04 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 24 Aug 2022 00:05:04 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 24 Aug 2022 00:05:04 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 24 Aug 2022 00:05:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:05:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:29 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:29 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:29 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6691d7f6adee381afc9d4d314f7637d83bf2e0fe70e20367aa712369f5d08ea`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94af741c6194d329aba944a401b0a648e28c60f15eb3a69e6352bb2b78f9885c`  
		Last Modified: Wed, 24 Aug 2022 00:10:05 GMT  
		Size: 88.2 MB (88218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fdb9c66fb5f9ce80221e2e4eb7cb12e3716507e84dec2246a1d0b8d30c84be`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2114e556255ea8ad33591210e8a17b28231cbc9e72b447d07c584414075e172a`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 6.7 KB (6692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.17` - linux; ppc64le

```console
$ docker pull mariadb@sha256:157fec64111a52fc2cfbaf5266e08cf5717cee2889b7388c25fc7e46a0c7a9e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139003968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7295a9fac6430bebdfa902cd910709aceeec14bdaf270d653fc0435dc5c98885`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:18:00 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:18:01 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:18:01 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:18:01 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:18:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:18:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:18:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:18:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:18:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:18:49 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:18:49 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:18:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b133d4f0ec8f84ed744d953b45c9aabbf93e623e4755870d4d01b1f94cf8b294`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a956d492c4a0ef2ee94d0b158b21ad1bc92ab1ed1db412e3d7989cdc59c593d`  
		Last Modified: Tue, 23 Aug 2022 22:26:41 GMT  
		Size: 92.8 MB (92787291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c12ee8bc68e45a474cd378d2cf47305884458cb918140f8677ae465b7362517`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0890efea0b238ba6d42d6d0cce09ab28c9fe275fff82bcf86be479d2b126f6b7`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 6.7 KB (6694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.17` - linux; s390x

```console
$ docker pull mariadb@sha256:9c1d326b8a032cd9f76c9154d466f98732d42efc24d4f561264b7fb3c5b8af9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127366738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e580c6d254bf14fc5cd5fba2607dd4e5cd732307d4ebd32e3d7ed4665f3ed69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:59:48 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:59:48 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:59:49 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:59:49 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:59:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:59:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 23:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 23:00:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 23:00:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 23:00:49 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 23:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 23:00:50 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 23:00:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e5ce27f8f25a0844bb97a243fa1163416d7f9f24d07f253d5db95c16798ab`  
		Last Modified: Tue, 23 Aug 2022 23:19:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c084be3dfe747df64b34478d369a5136126529e3eebd4ee2bf4f38ff42b401e`  
		Last Modified: Tue, 23 Aug 2022 23:19:52 GMT  
		Size: 89.5 MB (89509543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312bc47786b12ce9a3d80bd8d11f5009ecc62e7797dfb7b0ad1165b26873708`  
		Last Modified: Tue, 23 Aug 2022 23:19:40 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e518bbdf7633214c876cfbda75fbaa46e04712d455aea0775bb26844ddd3a227`  
		Last Modified: Tue, 23 Aug 2022 23:19:39 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.17-focal`

```console
$ docker pull mariadb@sha256:ee617df6a460abc8078b6911986bf3af1e1e44c740fc0e5a9e79d04f47170fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.17-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:81fddfb9e720dab6ec04fdfb18404ac18670fe167a31d1239f7b693feef497c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128149865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccda2dddb6f80fe36ae056da0a7cccc4035de579c29c39a2339fc54299ef4b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:05:04 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 24 Aug 2022 00:05:04 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 24 Aug 2022 00:05:04 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 24 Aug 2022 00:05:04 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 24 Aug 2022 00:05:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:05:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:29 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:29 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:29 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6691d7f6adee381afc9d4d314f7637d83bf2e0fe70e20367aa712369f5d08ea`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94af741c6194d329aba944a401b0a648e28c60f15eb3a69e6352bb2b78f9885c`  
		Last Modified: Wed, 24 Aug 2022 00:10:05 GMT  
		Size: 88.2 MB (88218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fdb9c66fb5f9ce80221e2e4eb7cb12e3716507e84dec2246a1d0b8d30c84be`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2114e556255ea8ad33591210e8a17b28231cbc9e72b447d07c584414075e172a`  
		Last Modified: Wed, 24 Aug 2022 00:09:52 GMT  
		Size: 6.7 KB (6692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.17-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:157fec64111a52fc2cfbaf5266e08cf5717cee2889b7388c25fc7e46a0c7a9e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139003968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7295a9fac6430bebdfa902cd910709aceeec14bdaf270d653fc0435dc5c98885`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:18:00 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:18:01 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:18:01 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:18:01 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:18:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:18:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:18:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:18:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:18:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:18:49 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:18:49 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:18:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b133d4f0ec8f84ed744d953b45c9aabbf93e623e4755870d4d01b1f94cf8b294`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a956d492c4a0ef2ee94d0b158b21ad1bc92ab1ed1db412e3d7989cdc59c593d`  
		Last Modified: Tue, 23 Aug 2022 22:26:41 GMT  
		Size: 92.8 MB (92787291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c12ee8bc68e45a474cd378d2cf47305884458cb918140f8677ae465b7362517`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0890efea0b238ba6d42d6d0cce09ab28c9fe275fff82bcf86be479d2b126f6b7`  
		Last Modified: Tue, 23 Aug 2022 22:26:17 GMT  
		Size: 6.7 KB (6694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.17-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:9c1d326b8a032cd9f76c9154d466f98732d42efc24d4f561264b7fb3c5b8af9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127366738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e580c6d254bf14fc5cd5fba2607dd4e5cd732307d4ebd32e3d7ed4665f3ed69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:59:48 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:59:48 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 23 Aug 2022 22:59:49 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:59:49 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 23 Aug 2022 22:59:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:59:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 23:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 23:00:48 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 23:00:49 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 23:00:49 GMT
COPY file:e0d9e49f1adbc1c1e2354d2dcc8c48beb9502a927b871b6815dba1ac953e0d0a in /usr/local/bin/ 
# Tue, 23 Aug 2022 23:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 23:00:50 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 23:00:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e5ce27f8f25a0844bb97a243fa1163416d7f9f24d07f253d5db95c16798ab`  
		Last Modified: Tue, 23 Aug 2022 23:19:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c084be3dfe747df64b34478d369a5136126529e3eebd4ee2bf4f38ff42b401e`  
		Last Modified: Tue, 23 Aug 2022 23:19:52 GMT  
		Size: 89.5 MB (89509543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312bc47786b12ce9a3d80bd8d11f5009ecc62e7797dfb7b0ad1165b26873708`  
		Last Modified: Tue, 23 Aug 2022 23:19:40 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e518bbdf7633214c876cfbda75fbaa46e04712d455aea0775bb26844ddd3a227`  
		Last Modified: Tue, 23 Aug 2022 23:19:39 GMT  
		Size: 6.7 KB (6695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:325326f6cc14d4fa856fd5cfa7b17bc016c43f036b467ed178a4cc053beac9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:9a0b0c98f7cb458e768928459f1a22b3f3480bfabab1084c22929a835c0a2679
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128415990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf92f2794a63f03b065ff74ef89eb3a301afdfa64be6ff7b4b097700ae289167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:04:36 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 24 Aug 2022 00:04:36 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 24 Aug 2022 00:04:36 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Wed, 24 Aug 2022 00:04:36 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Wed, 24 Aug 2022 00:04:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:04:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:01 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:01 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:01 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4866e3e5315791938be55c14a6f3560ca3e8c0aeef42847477eac81100f910c9`  
		Last Modified: Wed, 24 Aug 2022 00:09:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a861124bd790e1cd7848486b8e49b4ccc66cfe7989a0ce7fb0b4708977de0f`  
		Last Modified: Wed, 24 Aug 2022 00:09:36 GMT  
		Size: 88.5 MB (88485082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144c4ccfd133dde9d7a1be65d9d3302ff244d913322bc6db18091c04a4d43d1a`  
		Last Modified: Wed, 24 Aug 2022 00:09:23 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d573cb21ae7c47bc852ff65af9643288c773d32631dde4e2f1f8def594c513`  
		Last Modified: Wed, 24 Aug 2022 00:09:23 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1c8211242687771ba8775fd77e617f44d50de51af10ba1a60b6c1a12c3aa0a73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125424161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ca1eb53e914808b68c4be26966b4b26341224b78cdc44174451506c480b96b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:35:32 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 02 Aug 2022 18:35:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 02 Aug 2022 18:35:33 GMT
ARG MARIADB_VERSION=1:10.6.8+maria~focal
# Tue, 02 Aug 2022 18:35:34 GMT
ENV MARIADB_VERSION=1:10.6.8+maria~focal
# Tue, 02 Aug 2022 18:35:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.8/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:35:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.8/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:35:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.8/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:35:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:36:00 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:36:01 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:36:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:36:02 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:36:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae7307cb02fdd519b5d7db3c1f30d412779b83c0f83d4a7f158dc041a6b04a3`  
		Last Modified: Tue, 02 Aug 2022 18:43:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df60df6710cca87a5d1e1be55009d96bcfee6713469124932f98d485d5ab8199`  
		Last Modified: Tue, 02 Aug 2022 18:43:26 GMT  
		Size: 87.3 MB (87324673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb82d118ee8fca5b9a0db692402b5f23e230f67088b3b572096a838a27218041`  
		Last Modified: Tue, 02 Aug 2022 18:43:13 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce2f3952ce52f25a2e27142678fb9c50087932d4ae71476b13f8728b0a42ef9`  
		Last Modified: Tue, 02 Aug 2022 18:43:13 GMT  
		Size: 6.7 KB (6696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4637ffdf2d1610d0f9413d948cc4feb227a355086825d0b48929ba2bbc8d2e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139097005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c12ce58b000c941b7d7c0d54584c3725777c3a355af444302f5e098014c40d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:16:59 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:17:00 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:17:00 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:17:00 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:17:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:17:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:17:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:17:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:17:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:17:53 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:17:53 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b157e8207559c1da76c0ea78740d96704971913b9b789aaf8154b6c9bdb3534`  
		Last Modified: Tue, 23 Aug 2022 22:25:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ee00c40ee0679e037ef95ff1aad2d6b8110e8bb6b9bd09a0b335e8db65f0e1`  
		Last Modified: Tue, 23 Aug 2022 22:25:55 GMT  
		Size: 92.9 MB (92880322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e060d4c28d0cda90e6b8bc4af2129b8eb9407840e46f8c2caf25acc0a90452`  
		Last Modified: Tue, 23 Aug 2022 22:25:31 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04149a4f126765f1f8e50edfaf9285c923d872a3315f586e9dd6866cb333a1b`  
		Last Modified: Tue, 23 Aug 2022 22:25:30 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; s390x

```console
$ docker pull mariadb@sha256:0ac2ad5a7f25b0006de4188ef501984bcc765f7677f9183159d75c8a300eb942
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127400451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275e84b6b620cef7c86cf2693e137855cedaf0bdeac649507ab291c60da4b56c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:59:10 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:59:10 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:59:10 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:59:10 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:59:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:59:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:59:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:59:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:59:40 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:59:40 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:59:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:59:40 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:59:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da02ce96af42d84214763157c7a094763beb0d6fbeff3ffe43c54de14849496`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8936db79ad2a17f4b06c07dd6baafb7c955491fd8d842ad966902192ebb1ae2`  
		Last Modified: Tue, 23 Aug 2022 23:17:08 GMT  
		Size: 89.5 MB (89543255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d316a872d273e2ad89e8636c7d0a06be1d9a8029a6203b51bf25aa7aedf8b236`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e65642b303b6b959ef5a8d189433aaabab7078317871a4b0921e53a8166b78`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:325326f6cc14d4fa856fd5cfa7b17bc016c43f036b467ed178a4cc053beac9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:9a0b0c98f7cb458e768928459f1a22b3f3480bfabab1084c22929a835c0a2679
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128415990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf92f2794a63f03b065ff74ef89eb3a301afdfa64be6ff7b4b097700ae289167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:04:36 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 24 Aug 2022 00:04:36 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 24 Aug 2022 00:04:36 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Wed, 24 Aug 2022 00:04:36 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Wed, 24 Aug 2022 00:04:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:04:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:01 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:01 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:01 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4866e3e5315791938be55c14a6f3560ca3e8c0aeef42847477eac81100f910c9`  
		Last Modified: Wed, 24 Aug 2022 00:09:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a861124bd790e1cd7848486b8e49b4ccc66cfe7989a0ce7fb0b4708977de0f`  
		Last Modified: Wed, 24 Aug 2022 00:09:36 GMT  
		Size: 88.5 MB (88485082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144c4ccfd133dde9d7a1be65d9d3302ff244d913322bc6db18091c04a4d43d1a`  
		Last Modified: Wed, 24 Aug 2022 00:09:23 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d573cb21ae7c47bc852ff65af9643288c773d32631dde4e2f1f8def594c513`  
		Last Modified: Wed, 24 Aug 2022 00:09:23 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1c8211242687771ba8775fd77e617f44d50de51af10ba1a60b6c1a12c3aa0a73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125424161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ca1eb53e914808b68c4be26966b4b26341224b78cdc44174451506c480b96b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:35:32 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 02 Aug 2022 18:35:32 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 02 Aug 2022 18:35:33 GMT
ARG MARIADB_VERSION=1:10.6.8+maria~focal
# Tue, 02 Aug 2022 18:35:34 GMT
ENV MARIADB_VERSION=1:10.6.8+maria~focal
# Tue, 02 Aug 2022 18:35:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.8/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:35:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.8/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:35:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.8/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:35:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:36:00 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:36:01 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:36:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:36:02 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:36:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae7307cb02fdd519b5d7db3c1f30d412779b83c0f83d4a7f158dc041a6b04a3`  
		Last Modified: Tue, 02 Aug 2022 18:43:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df60df6710cca87a5d1e1be55009d96bcfee6713469124932f98d485d5ab8199`  
		Last Modified: Tue, 02 Aug 2022 18:43:26 GMT  
		Size: 87.3 MB (87324673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb82d118ee8fca5b9a0db692402b5f23e230f67088b3b572096a838a27218041`  
		Last Modified: Tue, 02 Aug 2022 18:43:13 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce2f3952ce52f25a2e27142678fb9c50087932d4ae71476b13f8728b0a42ef9`  
		Last Modified: Tue, 02 Aug 2022 18:43:13 GMT  
		Size: 6.7 KB (6696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4637ffdf2d1610d0f9413d948cc4feb227a355086825d0b48929ba2bbc8d2e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139097005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c12ce58b000c941b7d7c0d54584c3725777c3a355af444302f5e098014c40d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:16:59 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:17:00 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:17:00 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:17:00 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:17:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:17:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:17:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:17:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:17:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:17:53 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:17:53 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b157e8207559c1da76c0ea78740d96704971913b9b789aaf8154b6c9bdb3534`  
		Last Modified: Tue, 23 Aug 2022 22:25:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ee00c40ee0679e037ef95ff1aad2d6b8110e8bb6b9bd09a0b335e8db65f0e1`  
		Last Modified: Tue, 23 Aug 2022 22:25:55 GMT  
		Size: 92.9 MB (92880322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e060d4c28d0cda90e6b8bc4af2129b8eb9407840e46f8c2caf25acc0a90452`  
		Last Modified: Tue, 23 Aug 2022 22:25:31 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04149a4f126765f1f8e50edfaf9285c923d872a3315f586e9dd6866cb333a1b`  
		Last Modified: Tue, 23 Aug 2022 22:25:30 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:0ac2ad5a7f25b0006de4188ef501984bcc765f7677f9183159d75c8a300eb942
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127400451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275e84b6b620cef7c86cf2693e137855cedaf0bdeac649507ab291c60da4b56c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:59:10 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:59:10 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:59:10 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:59:10 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:59:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:59:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:59:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:59:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:59:40 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:59:40 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:59:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:59:40 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:59:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da02ce96af42d84214763157c7a094763beb0d6fbeff3ffe43c54de14849496`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8936db79ad2a17f4b06c07dd6baafb7c955491fd8d842ad966902192ebb1ae2`  
		Last Modified: Tue, 23 Aug 2022 23:17:08 GMT  
		Size: 89.5 MB (89543255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d316a872d273e2ad89e8636c7d0a06be1d9a8029a6203b51bf25aa7aedf8b236`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e65642b303b6b959ef5a8d189433aaabab7078317871a4b0921e53a8166b78`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.9`

```console
$ docker pull mariadb@sha256:62f73944398ea991f809785c0bf69fe00706c6bb7d9bca42dcbd0d5ef556e1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.9` - linux; amd64

```console
$ docker pull mariadb@sha256:9a0b0c98f7cb458e768928459f1a22b3f3480bfabab1084c22929a835c0a2679
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128415990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf92f2794a63f03b065ff74ef89eb3a301afdfa64be6ff7b4b097700ae289167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:04:36 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 24 Aug 2022 00:04:36 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 24 Aug 2022 00:04:36 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Wed, 24 Aug 2022 00:04:36 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Wed, 24 Aug 2022 00:04:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:04:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:01 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:01 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:01 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4866e3e5315791938be55c14a6f3560ca3e8c0aeef42847477eac81100f910c9`  
		Last Modified: Wed, 24 Aug 2022 00:09:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a861124bd790e1cd7848486b8e49b4ccc66cfe7989a0ce7fb0b4708977de0f`  
		Last Modified: Wed, 24 Aug 2022 00:09:36 GMT  
		Size: 88.5 MB (88485082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144c4ccfd133dde9d7a1be65d9d3302ff244d913322bc6db18091c04a4d43d1a`  
		Last Modified: Wed, 24 Aug 2022 00:09:23 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d573cb21ae7c47bc852ff65af9643288c773d32631dde4e2f1f8def594c513`  
		Last Modified: Wed, 24 Aug 2022 00:09:23 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.9` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4637ffdf2d1610d0f9413d948cc4feb227a355086825d0b48929ba2bbc8d2e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139097005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c12ce58b000c941b7d7c0d54584c3725777c3a355af444302f5e098014c40d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:16:59 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:17:00 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:17:00 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:17:00 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:17:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:17:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:17:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:17:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:17:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:17:53 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:17:53 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b157e8207559c1da76c0ea78740d96704971913b9b789aaf8154b6c9bdb3534`  
		Last Modified: Tue, 23 Aug 2022 22:25:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ee00c40ee0679e037ef95ff1aad2d6b8110e8bb6b9bd09a0b335e8db65f0e1`  
		Last Modified: Tue, 23 Aug 2022 22:25:55 GMT  
		Size: 92.9 MB (92880322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e060d4c28d0cda90e6b8bc4af2129b8eb9407840e46f8c2caf25acc0a90452`  
		Last Modified: Tue, 23 Aug 2022 22:25:31 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04149a4f126765f1f8e50edfaf9285c923d872a3315f586e9dd6866cb333a1b`  
		Last Modified: Tue, 23 Aug 2022 22:25:30 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.9` - linux; s390x

```console
$ docker pull mariadb@sha256:0ac2ad5a7f25b0006de4188ef501984bcc765f7677f9183159d75c8a300eb942
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127400451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275e84b6b620cef7c86cf2693e137855cedaf0bdeac649507ab291c60da4b56c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:59:10 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:59:10 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:59:10 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:59:10 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:59:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:59:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:59:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:59:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:59:40 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:59:40 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:59:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:59:40 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:59:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da02ce96af42d84214763157c7a094763beb0d6fbeff3ffe43c54de14849496`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8936db79ad2a17f4b06c07dd6baafb7c955491fd8d842ad966902192ebb1ae2`  
		Last Modified: Tue, 23 Aug 2022 23:17:08 GMT  
		Size: 89.5 MB (89543255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d316a872d273e2ad89e8636c7d0a06be1d9a8029a6203b51bf25aa7aedf8b236`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e65642b303b6b959ef5a8d189433aaabab7078317871a4b0921e53a8166b78`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.9-focal`

```console
$ docker pull mariadb@sha256:62f73944398ea991f809785c0bf69fe00706c6bb7d9bca42dcbd0d5ef556e1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.9-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:9a0b0c98f7cb458e768928459f1a22b3f3480bfabab1084c22929a835c0a2679
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128415990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf92f2794a63f03b065ff74ef89eb3a301afdfa64be6ff7b4b097700ae289167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:04:36 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 24 Aug 2022 00:04:36 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 24 Aug 2022 00:04:36 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Wed, 24 Aug 2022 00:04:36 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Wed, 24 Aug 2022 00:04:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:04:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:05:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:05:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:05:01 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:05:01 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:05:01 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:05:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4866e3e5315791938be55c14a6f3560ca3e8c0aeef42847477eac81100f910c9`  
		Last Modified: Wed, 24 Aug 2022 00:09:22 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a861124bd790e1cd7848486b8e49b4ccc66cfe7989a0ce7fb0b4708977de0f`  
		Last Modified: Wed, 24 Aug 2022 00:09:36 GMT  
		Size: 88.5 MB (88485082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144c4ccfd133dde9d7a1be65d9d3302ff244d913322bc6db18091c04a4d43d1a`  
		Last Modified: Wed, 24 Aug 2022 00:09:23 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d573cb21ae7c47bc852ff65af9643288c773d32631dde4e2f1f8def594c513`  
		Last Modified: Wed, 24 Aug 2022 00:09:23 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.9-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4637ffdf2d1610d0f9413d948cc4feb227a355086825d0b48929ba2bbc8d2e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139097005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c12ce58b000c941b7d7c0d54584c3725777c3a355af444302f5e098014c40d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:16:59 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:17:00 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:17:00 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:17:00 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:17:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:17:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:17:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:17:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:17:53 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:17:53 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:17:53 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b157e8207559c1da76c0ea78740d96704971913b9b789aaf8154b6c9bdb3534`  
		Last Modified: Tue, 23 Aug 2022 22:25:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ee00c40ee0679e037ef95ff1aad2d6b8110e8bb6b9bd09a0b335e8db65f0e1`  
		Last Modified: Tue, 23 Aug 2022 22:25:55 GMT  
		Size: 92.9 MB (92880322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e060d4c28d0cda90e6b8bc4af2129b8eb9407840e46f8c2caf25acc0a90452`  
		Last Modified: Tue, 23 Aug 2022 22:25:31 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04149a4f126765f1f8e50edfaf9285c923d872a3315f586e9dd6866cb333a1b`  
		Last Modified: Tue, 23 Aug 2022 22:25:30 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.9-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:0ac2ad5a7f25b0006de4188ef501984bcc765f7677f9183159d75c8a300eb942
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127400451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275e84b6b620cef7c86cf2693e137855cedaf0bdeac649507ab291c60da4b56c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:59:10 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:59:10 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 23 Aug 2022 22:59:10 GMT
ARG MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:59:10 GMT
ENV MARIADB_VERSION=1:10.6.9+maria~ubu2004
# Tue, 23 Aug 2022 22:59:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:59:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:59:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.9/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:59:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:59:40 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:59:40 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:59:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:59:40 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:59:41 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da02ce96af42d84214763157c7a094763beb0d6fbeff3ffe43c54de14849496`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8936db79ad2a17f4b06c07dd6baafb7c955491fd8d842ad966902192ebb1ae2`  
		Last Modified: Tue, 23 Aug 2022 23:17:08 GMT  
		Size: 89.5 MB (89543255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d316a872d273e2ad89e8636c7d0a06be1d9a8029a6203b51bf25aa7aedf8b236`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e65642b303b6b959ef5a8d189433aaabab7078317871a4b0921e53a8166b78`  
		Last Modified: Tue, 23 Aug 2022 23:16:55 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7`

```console
$ docker pull mariadb@sha256:b06be3c02bf4175a34b785c0d7202654ed7577d2bc02811ebdb42e97dffec463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7` - linux; amd64

```console
$ docker pull mariadb@sha256:7c7d4d132e73070cdcc75873259f1336562d4549d61be396c738a4dc3eca42ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128891379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0408ef424b96e9c898cb70ac2e0af8fd2f1cfccc6f6dc4de74707f981f7ebd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:03:53 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 24 Aug 2022 00:03:54 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 24 Aug 2022 00:03:54 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Wed, 24 Aug 2022 00:03:54 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Wed, 24 Aug 2022 00:03:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:03:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:04:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:04:32 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:04:32 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:04:32 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:04:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:04:32 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:04:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7088cfcbf9ba1e15e1a95eff249ad7ff93d52d00f5f9c41485b18edc0663f9c8`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421ee1a925a408afc1d71e6ae166a4043c9204031e38f710ea0399ef7caf8e6d`  
		Last Modified: Wed, 24 Aug 2022 00:09:07 GMT  
		Size: 89.0 MB (88960470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6a900d8b5623a9bdfba44ebc8e5683d3b2c5000eb4924309d5c5c90e68628c`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb0d276753f0e2e011db5e76319a5e36938a247d231b923a56912d06b7590ec`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4f5af175bc868d273bf03b138dd75c7299b5f33cd5789b5c4fc2798fab2ff753
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125907158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f873d0c6cf12bfd2b3f5d8e9d839d07115a3ba465664129691aceb82895ae343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:34:46 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 02 Aug 2022 18:34:47 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 02 Aug 2022 18:34:48 GMT
ARG MARIADB_VERSION=1:10.7.4+maria~focal
# Tue, 02 Aug 2022 18:34:49 GMT
ENV MARIADB_VERSION=1:10.7.4+maria~focal
# Tue, 02 Aug 2022 18:34:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.4/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:34:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:35:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:35:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:35:16 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:35:17 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:35:18 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:35:19 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de3bd4d6fac28344afff3704daa788ce9fb41f278768ad4628667013073f385`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a757a0c4be796915a937cf877cfd9b2c286ec749d6069fd498ad56d6c1fc6f`  
		Last Modified: Tue, 02 Aug 2022 18:42:54 GMT  
		Size: 87.8 MB (87807667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef2ca41942f4d6ff9406a58ca9a1109a04ce810b4081eb3da6f765b1241da7`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da936e34985dde60992a2acbf865e29dee94677edd25978ca769aa6a25a367`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 6.7 KB (6698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:610a9f4f4d3cea66995d0a09f18e5bc3fa3010cfeda514e2bbf9c4ffcb02cd15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139790233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75800e81e43640c8033f21e13b432e6602f0e175152e7acba6f543d3a04c4ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:15:46 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:15:46 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:15:46 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:15:47 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:15:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:15:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:16:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:16:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:16:51 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:16:51 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:16:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:16:52 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:16:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42febfb98ecc8a66f40a8f856a81e144fc28eeb2afd3dc4aca5e9ae85be2a08`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8225b8c3b7dfeaab2271eb74cbace84a4fda35e481e63e6c5b7bd119baf9dfb7`  
		Last Modified: Tue, 23 Aug 2022 22:25:09 GMT  
		Size: 93.6 MB (93573548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655afe279efd4aaf7eb1aacb38bf00f95b1e4c5b0bc5f6cdf17903e12e8fd040`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65faa25016d47ea42873d35e46cce826c2cebca0d92a05925ac79cfc37195671`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; s390x

```console
$ docker pull mariadb@sha256:3f36216f8a079e11f12f8d1fab5c23ad70ec84d185b125370821e5ddfbc47dbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127912674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bd3edbd39365c6bf114cf7e7e618b72e4248dda8b5b5471af694971844699e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:58:23 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:58:23 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:58:23 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:58:23 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:58:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:58:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:58:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:58:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:58:59 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:59:00 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:59:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:59:00 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:59:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeffee1279d4ef5e63b6e059c358a2b42952ea6b75f1395d8d8b948838cf286`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c7d419c87038024b21fc0e976d2635165aa4e3f72fc63a5f65b967f4325241`  
		Last Modified: Tue, 23 Aug 2022 23:14:11 GMT  
		Size: 90.1 MB (90055478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31538ee4ae1037f4f7d4c5b03229cca0b454a77e46c739d5f5dc41ee8379a043`  
		Last Modified: Tue, 23 Aug 2022 23:14:02 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d8b04b18ea64a339d3ef09afe0bb16c8618446467bf0763ed79195fdd612e7`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 6.7 KB (6702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7-focal`

```console
$ docker pull mariadb@sha256:b06be3c02bf4175a34b785c0d7202654ed7577d2bc02811ebdb42e97dffec463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7c7d4d132e73070cdcc75873259f1336562d4549d61be396c738a4dc3eca42ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128891379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0408ef424b96e9c898cb70ac2e0af8fd2f1cfccc6f6dc4de74707f981f7ebd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:03:53 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 24 Aug 2022 00:03:54 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 24 Aug 2022 00:03:54 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Wed, 24 Aug 2022 00:03:54 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Wed, 24 Aug 2022 00:03:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:03:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:04:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:04:32 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:04:32 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:04:32 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:04:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:04:32 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:04:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7088cfcbf9ba1e15e1a95eff249ad7ff93d52d00f5f9c41485b18edc0663f9c8`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421ee1a925a408afc1d71e6ae166a4043c9204031e38f710ea0399ef7caf8e6d`  
		Last Modified: Wed, 24 Aug 2022 00:09:07 GMT  
		Size: 89.0 MB (88960470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6a900d8b5623a9bdfba44ebc8e5683d3b2c5000eb4924309d5c5c90e68628c`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb0d276753f0e2e011db5e76319a5e36938a247d231b923a56912d06b7590ec`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4f5af175bc868d273bf03b138dd75c7299b5f33cd5789b5c4fc2798fab2ff753
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125907158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f873d0c6cf12bfd2b3f5d8e9d839d07115a3ba465664129691aceb82895ae343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:34:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:34:17 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:34:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:34:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:34:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:34:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:34:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:34:46 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 02 Aug 2022 18:34:47 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 02 Aug 2022 18:34:48 GMT
ARG MARIADB_VERSION=1:10.7.4+maria~focal
# Tue, 02 Aug 2022 18:34:49 GMT
ENV MARIADB_VERSION=1:10.7.4+maria~focal
# Tue, 02 Aug 2022 18:34:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.4/repo/ubuntu/ focal main
# Tue, 02 Aug 2022 18:34:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:35:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:35:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:35:16 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:35:17 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:35:18 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:35:19 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d70702fc52aefacc8ccbff1968c3548d6400deb5e6c53d75f6dbc14905cb7`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ffe290feb53a390aea694e16a663c4a420a71b1ebcd8053b07a44579782bbe`  
		Last Modified: Tue, 02 Aug 2022 18:42:44 GMT  
		Size: 5.3 MB (5321787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430076265be6d7113b835ac1ab3e08dab46e41fff7e3ed070286125f1dbf6d`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 3.4 MB (3367877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c880491c15580752404cccf2db4534a2d79f5b5cd1df18b3f6ea2754809020`  
		Last Modified: Tue, 02 Aug 2022 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca8382cebf14e057456cd5ec8096f0053cdfe6029503875b74003df35d8c5e`  
		Last Modified: Tue, 02 Aug 2022 18:42:43 GMT  
		Size: 2.2 MB (2203204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88502488cc76b679835db628ad4d0f65e09a69018881918c6765cfb9e071feed`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de3bd4d6fac28344afff3704daa788ce9fb41f278768ad4628667013073f385`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a757a0c4be796915a937cf877cfd9b2c286ec749d6069fd498ad56d6c1fc6f`  
		Last Modified: Tue, 02 Aug 2022 18:42:54 GMT  
		Size: 87.8 MB (87807667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef2ca41942f4d6ff9406a58ca9a1109a04ce810b4081eb3da6f765b1241da7`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da936e34985dde60992a2acbf865e29dee94677edd25978ca769aa6a25a367`  
		Last Modified: Tue, 02 Aug 2022 18:42:40 GMT  
		Size: 6.7 KB (6698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:610a9f4f4d3cea66995d0a09f18e5bc3fa3010cfeda514e2bbf9c4ffcb02cd15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139790233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75800e81e43640c8033f21e13b432e6602f0e175152e7acba6f543d3a04c4ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:15:46 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:15:46 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:15:46 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:15:47 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:15:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:15:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:16:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:16:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:16:51 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:16:51 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:16:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:16:52 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:16:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42febfb98ecc8a66f40a8f856a81e144fc28eeb2afd3dc4aca5e9ae85be2a08`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8225b8c3b7dfeaab2271eb74cbace84a4fda35e481e63e6c5b7bd119baf9dfb7`  
		Last Modified: Tue, 23 Aug 2022 22:25:09 GMT  
		Size: 93.6 MB (93573548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655afe279efd4aaf7eb1aacb38bf00f95b1e4c5b0bc5f6cdf17903e12e8fd040`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65faa25016d47ea42873d35e46cce826c2cebca0d92a05925ac79cfc37195671`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:3f36216f8a079e11f12f8d1fab5c23ad70ec84d185b125370821e5ddfbc47dbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127912674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bd3edbd39365c6bf114cf7e7e618b72e4248dda8b5b5471af694971844699e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:58:23 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:58:23 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:58:23 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:58:23 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:58:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:58:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:58:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:58:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:58:59 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:59:00 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:59:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:59:00 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:59:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeffee1279d4ef5e63b6e059c358a2b42952ea6b75f1395d8d8b948838cf286`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c7d419c87038024b21fc0e976d2635165aa4e3f72fc63a5f65b967f4325241`  
		Last Modified: Tue, 23 Aug 2022 23:14:11 GMT  
		Size: 90.1 MB (90055478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31538ee4ae1037f4f7d4c5b03229cca0b454a77e46c739d5f5dc41ee8379a043`  
		Last Modified: Tue, 23 Aug 2022 23:14:02 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d8b04b18ea64a339d3ef09afe0bb16c8618446467bf0763ed79195fdd612e7`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 6.7 KB (6702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.5`

```console
$ docker pull mariadb@sha256:29c4722ec338df28649b0591ac541f7b6506514a04d21a0edad145708e62ed30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.5` - linux; amd64

```console
$ docker pull mariadb@sha256:7c7d4d132e73070cdcc75873259f1336562d4549d61be396c738a4dc3eca42ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128891379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0408ef424b96e9c898cb70ac2e0af8fd2f1cfccc6f6dc4de74707f981f7ebd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:03:53 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 24 Aug 2022 00:03:54 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 24 Aug 2022 00:03:54 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Wed, 24 Aug 2022 00:03:54 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Wed, 24 Aug 2022 00:03:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:03:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:04:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:04:32 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:04:32 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:04:32 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:04:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:04:32 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:04:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7088cfcbf9ba1e15e1a95eff249ad7ff93d52d00f5f9c41485b18edc0663f9c8`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421ee1a925a408afc1d71e6ae166a4043c9204031e38f710ea0399ef7caf8e6d`  
		Last Modified: Wed, 24 Aug 2022 00:09:07 GMT  
		Size: 89.0 MB (88960470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6a900d8b5623a9bdfba44ebc8e5683d3b2c5000eb4924309d5c5c90e68628c`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb0d276753f0e2e011db5e76319a5e36938a247d231b923a56912d06b7590ec`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:610a9f4f4d3cea66995d0a09f18e5bc3fa3010cfeda514e2bbf9c4ffcb02cd15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139790233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75800e81e43640c8033f21e13b432e6602f0e175152e7acba6f543d3a04c4ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:15:46 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:15:46 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:15:46 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:15:47 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:15:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:15:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:16:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:16:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:16:51 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:16:51 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:16:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:16:52 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:16:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42febfb98ecc8a66f40a8f856a81e144fc28eeb2afd3dc4aca5e9ae85be2a08`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8225b8c3b7dfeaab2271eb74cbace84a4fda35e481e63e6c5b7bd119baf9dfb7`  
		Last Modified: Tue, 23 Aug 2022 22:25:09 GMT  
		Size: 93.6 MB (93573548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655afe279efd4aaf7eb1aacb38bf00f95b1e4c5b0bc5f6cdf17903e12e8fd040`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65faa25016d47ea42873d35e46cce826c2cebca0d92a05925ac79cfc37195671`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.5` - linux; s390x

```console
$ docker pull mariadb@sha256:3f36216f8a079e11f12f8d1fab5c23ad70ec84d185b125370821e5ddfbc47dbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127912674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bd3edbd39365c6bf114cf7e7e618b72e4248dda8b5b5471af694971844699e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:58:23 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:58:23 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:58:23 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:58:23 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:58:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:58:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:58:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:58:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:58:59 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:59:00 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:59:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:59:00 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:59:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeffee1279d4ef5e63b6e059c358a2b42952ea6b75f1395d8d8b948838cf286`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c7d419c87038024b21fc0e976d2635165aa4e3f72fc63a5f65b967f4325241`  
		Last Modified: Tue, 23 Aug 2022 23:14:11 GMT  
		Size: 90.1 MB (90055478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31538ee4ae1037f4f7d4c5b03229cca0b454a77e46c739d5f5dc41ee8379a043`  
		Last Modified: Tue, 23 Aug 2022 23:14:02 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d8b04b18ea64a339d3ef09afe0bb16c8618446467bf0763ed79195fdd612e7`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 6.7 KB (6702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.5-focal`

```console
$ docker pull mariadb@sha256:29c4722ec338df28649b0591ac541f7b6506514a04d21a0edad145708e62ed30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7c7d4d132e73070cdcc75873259f1336562d4549d61be396c738a4dc3eca42ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128891379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0408ef424b96e9c898cb70ac2e0af8fd2f1cfccc6f6dc4de74707f981f7ebd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:21:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:03:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:03:43 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:03:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:03:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:03:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:03:53 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 24 Aug 2022 00:03:54 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 24 Aug 2022 00:03:54 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Wed, 24 Aug 2022 00:03:54 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Wed, 24 Aug 2022 00:03:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Wed, 24 Aug 2022 00:03:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:04:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:04:32 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:04:32 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:04:32 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:04:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:04:32 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:04:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19669910bc06b914ac5d4512b9aa15623df49e4ef03d20277f4a8fda0cf5631`  
		Last Modified: Tue, 02 Aug 2022 20:27:42 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f44a1c933f42d531ea16720703f4d291ed4554d6246570d7287a3131bc62c3`  
		Last Modified: Wed, 24 Aug 2022 00:08:57 GMT  
		Size: 5.5 MB (5489009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d39ce0fa46b4a071988727786348b97ce1e0f92daaebb5e8030edfcc06ff32`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 3.6 MB (3581817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285e5d2c99416f18f10db9a2569d4f9e9b53709b344c1704ebe12b91443b55ab`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020d5354f4a0293ec110c30146e4a1ed710aec7781a1b7bca73a4d782502f63`  
		Last Modified: Wed, 24 Aug 2022 00:08:56 GMT  
		Size: 2.3 MB (2272576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e283bdcdaad633e99ac79680c2aeef76ffd524cee0c4ca0bf1c3013a8728d8b`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7088cfcbf9ba1e15e1a95eff249ad7ff93d52d00f5f9c41485b18edc0663f9c8`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421ee1a925a408afc1d71e6ae166a4043c9204031e38f710ea0399ef7caf8e6d`  
		Last Modified: Wed, 24 Aug 2022 00:09:07 GMT  
		Size: 89.0 MB (88960470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6a900d8b5623a9bdfba44ebc8e5683d3b2c5000eb4924309d5c5c90e68628c`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb0d276753f0e2e011db5e76319a5e36938a247d231b923a56912d06b7590ec`  
		Last Modified: Wed, 24 Aug 2022 00:08:53 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:610a9f4f4d3cea66995d0a09f18e5bc3fa3010cfeda514e2bbf9c4ffcb02cd15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139790233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75800e81e43640c8033f21e13b432e6602f0e175152e7acba6f543d3a04c4ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:01 GMT
ADD file:75dd7889d4feb83b8504153b5ea6873e4ab0e616a4f4489ea81fd055b6ce9def in / 
# Tue, 02 Aug 2022 01:31:03 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:33:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:15:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:05 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:15:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:15:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:15:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:15:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:15:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:15:46 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:15:46 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:15:46 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:15:47 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:15:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:15:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:16:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:16:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:16:51 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:16:51 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:16:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:16:52 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:16:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bf47d2be67f1a301865e78e8f78cc69c55dcc389921b4ba187dc0d333cbfd63b`  
		Last Modified: Tue, 02 Aug 2022 01:33:30 GMT  
		Size: 33.3 MB (33295352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481bc43c771217829dcc78384d81402be7256c3fabe0fb95c0ad844e20eb486`  
		Last Modified: Wed, 03 Aug 2022 04:45:28 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aae52dac855f56977c1bf6a45b01e71291ccb0f67bfc31999a30c12e9a5a1c`  
		Last Modified: Tue, 23 Aug 2022 22:24:49 GMT  
		Size: 6.7 MB (6667828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cc9eafaca53bbf2e4038bba0125b9116b352d57eb8010465d20d76b02a270`  
		Last Modified: Tue, 23 Aug 2022 22:24:48 GMT  
		Size: 3.7 MB (3669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba57b703348e0048399e249a72d70e1a08fd9af89b8305663ebe25c3063cd6`  
		Last Modified: Tue, 23 Aug 2022 22:24:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976724f57de2918e17fd5ed19c682120db46049840be078b9019a1501d0f26d4`  
		Last Modified: Tue, 23 Aug 2022 22:24:47 GMT  
		Size: 2.6 MB (2568682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e1eb1ce8da09bb61f2180258346fe1aea225af9d3f81bb57ed736a74e72d43`  
		Last Modified: Tue, 23 Aug 2022 22:24:45 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42febfb98ecc8a66f40a8f856a81e144fc28eeb2afd3dc4aca5e9ae85be2a08`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8225b8c3b7dfeaab2271eb74cbace84a4fda35e481e63e6c5b7bd119baf9dfb7`  
		Last Modified: Tue, 23 Aug 2022 22:25:09 GMT  
		Size: 93.6 MB (93573548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655afe279efd4aaf7eb1aacb38bf00f95b1e4c5b0bc5f6cdf17903e12e8fd040`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65faa25016d47ea42873d35e46cce826c2cebca0d92a05925ac79cfc37195671`  
		Last Modified: Tue, 23 Aug 2022 22:24:44 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:3f36216f8a079e11f12f8d1fab5c23ad70ec84d185b125370821e5ddfbc47dbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127912674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bd3edbd39365c6bf114cf7e7e618b72e4248dda8b5b5471af694971844699e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:51 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:57:44 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:57:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:58:10 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:58:18 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:58:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:58:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:58:23 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:58:23 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 23 Aug 2022 22:58:23 GMT
ARG MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:58:23 GMT
ENV MARIADB_VERSION=1:10.7.5+maria~ubu2004
# Tue, 23 Aug 2022 22:58:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
# Tue, 23 Aug 2022 22:58:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:58:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:58:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:58:59 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:59:00 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:59:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:59:00 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:59:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b542230411fae56efa86753d30f5439f912d60eabb26102f6570d97473c7573`  
		Last Modified: Tue, 02 Aug 2022 13:01:52 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06785d284e9376587c13a8de64dab74f5b1bd54b1e1f6ed942b0343f76d22ee4`  
		Last Modified: Tue, 23 Aug 2022 23:14:23 GMT  
		Size: 5.4 MB (5372740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b507cca3b143808baee6b93497016aca4a7e401c08f7c1d365225efbce6190a`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 3.2 MB (3240263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32a92ab3b03c1a83290817e4ed7e87c8312bcdd38373f9bd03df22df0d8b57`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a8ef0ca8617903ac3bb27fa476830b58f50ccc573ed31757c2a2d1a3db3ad`  
		Last Modified: Tue, 23 Aug 2022 23:14:15 GMT  
		Size: 2.2 MB (2183918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc567984664c763fbe4d7171bc9068e215f5cbb1ac0259014824f9981efc9d55`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeffee1279d4ef5e63b6e059c358a2b42952ea6b75f1395d8d8b948838cf286`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c7d419c87038024b21fc0e976d2635165aa4e3f72fc63a5f65b967f4325241`  
		Last Modified: Tue, 23 Aug 2022 23:14:11 GMT  
		Size: 90.1 MB (90055478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31538ee4ae1037f4f7d4c5b03229cca0b454a77e46c739d5f5dc41ee8379a043`  
		Last Modified: Tue, 23 Aug 2022 23:14:02 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d8b04b18ea64a339d3ef09afe0bb16c8618446467bf0763ed79195fdd612e7`  
		Last Modified: Tue, 23 Aug 2022 23:13:58 GMT  
		Size: 6.7 KB (6702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8`

```console
$ docker pull mariadb@sha256:b6dc0b99dac3f9e7abe0a98a9f504f29f8dea671f19707a10b770ea6ec8eae3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8` - linux; amd64

```console
$ docker pull mariadb@sha256:d025e1305839b80f3ac44f94bb218c61eb11fd62f9a2e01fff3cf4000a7541fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123938825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e7d13b47b89060a190dd8989796ccdec7705abae43b3e49b7b97bda1bd782f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:30 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 24 Aug 2022 00:02:30 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 24 Aug 2022 00:02:30 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Wed, 24 Aug 2022 00:02:30 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Wed, 24 Aug 2022 00:02:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:54 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:54 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:55 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac50cb207c741b71e7af0e6ff1c929815edb3601a71425f4235b151419c7547`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266e4baee040bf4cfc41fb75bd6f54bd16a04db896e52c0bf1d789ea2401c72`  
		Last Modified: Wed, 24 Aug 2022 00:08:37 GMT  
		Size: 85.4 MB (85440831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c8b5b2463c3b1e5c861dd816638ff90550d57d87c71ad68ada44ff85c8b750`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5f306ebe904fbd8db760f565fc8b7e6dfe681a1b244e54c4b8d6efc18cd24c`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1f011a0b21919b39058355d972fea445857869ad1f867eb56bd1d274fd969e88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102470825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f8da7eeabb6549ac946f2b45ffe497556f6ad227d0bd4d41e09e73e6b34097`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:32:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:32:16 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:32:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:32:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:32:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:32:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:33:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:29 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:30 GMT
ARG MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:31 GMT
ENV MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
# Tue, 02 Aug 2022 18:33:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:33:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:33:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:33:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:33:55 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:33:56 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:33:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5bedaed5f8e5343fee312eb2f21894d7b4026a0c692da89fe4f30a432e48b4`  
		Last Modified: Tue, 02 Aug 2022 18:41:32 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f07d81dfa02553c544d772dc3aa04ed6a2e6ad5b810ca742eee9a918786e5f`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 3.6 MB (3594051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b8a20cb609d07274a17b8dd4ae810b6a98f76cf0ad513aa0c03eda46fcbce`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 1.9 MB (1899200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d39cfcf2768f9c1165cc0d3764c3649542f541a1ed3f18bec6283d58553e00`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d230566e80222a9242f97419a6018684f4e324420ee89e4c0395f8107a124c91`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 2.2 MB (2211614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c8c9abaef706c6185822ae21205ab5bc569494c4492a89eef44d8a855315c5`  
		Last Modified: Tue, 02 Aug 2022 18:41:27 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bff43ba5b5f6479659a8a7496d4156615c3cd9439c46779dd3feed3c4511ae`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cb73ef10f93c31f677c6818187b24c6bb65b4cb76ad5ed05e5b31853ef1b73`  
		Last Modified: Tue, 02 Aug 2022 18:42:08 GMT  
		Size: 66.4 MB (66369985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b16804fca7957e5cc3538c9a1a58af3e8e7a9eb0ee3318ffa413c7ebf4c76d4`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffad21dfd527f8685de9b3c864738e88bb8791db49ecdeb988d9d194a20d7cc`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a337dc2d7268d765d648d1e9f00c1bd0141c4ebd97517af6e70a1ae769570fc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116914307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bf1d980307868c5285fb41eb5cb60b704d968123cf0ca47ee53714c7645df2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:13:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:13:28 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:13:29 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:13:29 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:13:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:13:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:14:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:14:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:14:11 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:14:12 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:14:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:14:12 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:14:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae80fa4a705d67389589017094f9ce1f353ab854515898da65e9038b1fcc6eaa`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834882ca1c206aea80fbcb1d5d74046cf818f46a56d7a432eaf0798626a07c69`  
		Last Modified: Tue, 23 Aug 2022 22:24:23 GMT  
		Size: 72.4 MB (72351677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a1b3d4ea228007ec52b61b5059f528b2d83b73655172c0f96b757258392eaa`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12605c90d2820db47e3ce2394d21b5e9de5c220b37947b24c7e356b29f369283`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8` - linux; s390x

```console
$ docker pull mariadb@sha256:90b47f090b353f8cf17bdd7ac84f8b20b4ac429e55a9720452da05c9fa1d4e66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105054403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317f193d8bc5732ac7b96e4632a52f720e66edac49e5e2884107c6fbcde399d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:45 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:56:45 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:56:45 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:56:45 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:56:45 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:57:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:57:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:57:13 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:57:13 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:57:14 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:57:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d963003499efb47d350dd16f1bdf62576658cbd1439a5746a688e0e52ff3ba5`  
		Last Modified: Tue, 23 Aug 2022 23:11:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee3ca001c631f58001b7c458cf6f06ac997dd1fc315114d17a56abf8c301688`  
		Last Modified: Tue, 23 Aug 2022 23:11:14 GMT  
		Size: 68.5 MB (68548867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177cbd11589739b81938cdcfabca35e5d4baa8a454cb47796731d5ef65088bcb`  
		Last Modified: Tue, 23 Aug 2022 23:11:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626aa0b7d36807a4b170bdb52a39df0f233f36079f3f3b12e3212dcbc44a23ad`  
		Last Modified: Tue, 23 Aug 2022 23:11:05 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-jammy`

```console
$ docker pull mariadb@sha256:b6dc0b99dac3f9e7abe0a98a9f504f29f8dea671f19707a10b770ea6ec8eae3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:d025e1305839b80f3ac44f94bb218c61eb11fd62f9a2e01fff3cf4000a7541fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123938825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e7d13b47b89060a190dd8989796ccdec7705abae43b3e49b7b97bda1bd782f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:30 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 24 Aug 2022 00:02:30 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 24 Aug 2022 00:02:30 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Wed, 24 Aug 2022 00:02:30 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Wed, 24 Aug 2022 00:02:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:54 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:54 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:55 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac50cb207c741b71e7af0e6ff1c929815edb3601a71425f4235b151419c7547`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266e4baee040bf4cfc41fb75bd6f54bd16a04db896e52c0bf1d789ea2401c72`  
		Last Modified: Wed, 24 Aug 2022 00:08:37 GMT  
		Size: 85.4 MB (85440831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c8b5b2463c3b1e5c861dd816638ff90550d57d87c71ad68ada44ff85c8b750`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5f306ebe904fbd8db760f565fc8b7e6dfe681a1b244e54c4b8d6efc18cd24c`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1f011a0b21919b39058355d972fea445857869ad1f867eb56bd1d274fd969e88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102470825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f8da7eeabb6549ac946f2b45ffe497556f6ad227d0bd4d41e09e73e6b34097`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:32:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:32:16 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:32:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:32:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:32:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:32:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:33:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:29 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:30 GMT
ARG MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:31 GMT
ENV MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
# Tue, 02 Aug 2022 18:33:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:33:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:33:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:33:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:33:55 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:33:56 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:33:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5bedaed5f8e5343fee312eb2f21894d7b4026a0c692da89fe4f30a432e48b4`  
		Last Modified: Tue, 02 Aug 2022 18:41:32 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f07d81dfa02553c544d772dc3aa04ed6a2e6ad5b810ca742eee9a918786e5f`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 3.6 MB (3594051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b8a20cb609d07274a17b8dd4ae810b6a98f76cf0ad513aa0c03eda46fcbce`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 1.9 MB (1899200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d39cfcf2768f9c1165cc0d3764c3649542f541a1ed3f18bec6283d58553e00`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d230566e80222a9242f97419a6018684f4e324420ee89e4c0395f8107a124c91`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 2.2 MB (2211614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c8c9abaef706c6185822ae21205ab5bc569494c4492a89eef44d8a855315c5`  
		Last Modified: Tue, 02 Aug 2022 18:41:27 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bff43ba5b5f6479659a8a7496d4156615c3cd9439c46779dd3feed3c4511ae`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cb73ef10f93c31f677c6818187b24c6bb65b4cb76ad5ed05e5b31853ef1b73`  
		Last Modified: Tue, 02 Aug 2022 18:42:08 GMT  
		Size: 66.4 MB (66369985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b16804fca7957e5cc3538c9a1a58af3e8e7a9eb0ee3318ffa413c7ebf4c76d4`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffad21dfd527f8685de9b3c864738e88bb8791db49ecdeb988d9d194a20d7cc`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a337dc2d7268d765d648d1e9f00c1bd0141c4ebd97517af6e70a1ae769570fc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116914307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bf1d980307868c5285fb41eb5cb60b704d968123cf0ca47ee53714c7645df2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:13:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:13:28 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:13:29 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:13:29 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:13:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:13:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:14:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:14:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:14:11 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:14:12 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:14:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:14:12 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:14:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae80fa4a705d67389589017094f9ce1f353ab854515898da65e9038b1fcc6eaa`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834882ca1c206aea80fbcb1d5d74046cf818f46a56d7a432eaf0798626a07c69`  
		Last Modified: Tue, 23 Aug 2022 22:24:23 GMT  
		Size: 72.4 MB (72351677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a1b3d4ea228007ec52b61b5059f528b2d83b73655172c0f96b757258392eaa`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12605c90d2820db47e3ce2394d21b5e9de5c220b37947b24c7e356b29f369283`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:90b47f090b353f8cf17bdd7ac84f8b20b4ac429e55a9720452da05c9fa1d4e66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105054403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317f193d8bc5732ac7b96e4632a52f720e66edac49e5e2884107c6fbcde399d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:45 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:56:45 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:56:45 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:56:45 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:56:45 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:57:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:57:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:57:13 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:57:13 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:57:14 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:57:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d963003499efb47d350dd16f1bdf62576658cbd1439a5746a688e0e52ff3ba5`  
		Last Modified: Tue, 23 Aug 2022 23:11:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee3ca001c631f58001b7c458cf6f06ac997dd1fc315114d17a56abf8c301688`  
		Last Modified: Tue, 23 Aug 2022 23:11:14 GMT  
		Size: 68.5 MB (68548867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177cbd11589739b81938cdcfabca35e5d4baa8a454cb47796731d5ef65088bcb`  
		Last Modified: Tue, 23 Aug 2022 23:11:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626aa0b7d36807a4b170bdb52a39df0f233f36079f3f3b12e3212dcbc44a23ad`  
		Last Modified: Tue, 23 Aug 2022 23:11:05 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.4`

```console
$ docker pull mariadb@sha256:82b394b4f0ba430948841f7a32d9fb117c489553e0dd112fcba4633211146066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.4` - linux; amd64

```console
$ docker pull mariadb@sha256:d025e1305839b80f3ac44f94bb218c61eb11fd62f9a2e01fff3cf4000a7541fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123938825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e7d13b47b89060a190dd8989796ccdec7705abae43b3e49b7b97bda1bd782f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:30 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 24 Aug 2022 00:02:30 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 24 Aug 2022 00:02:30 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Wed, 24 Aug 2022 00:02:30 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Wed, 24 Aug 2022 00:02:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:54 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:54 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:55 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac50cb207c741b71e7af0e6ff1c929815edb3601a71425f4235b151419c7547`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266e4baee040bf4cfc41fb75bd6f54bd16a04db896e52c0bf1d789ea2401c72`  
		Last Modified: Wed, 24 Aug 2022 00:08:37 GMT  
		Size: 85.4 MB (85440831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c8b5b2463c3b1e5c861dd816638ff90550d57d87c71ad68ada44ff85c8b750`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5f306ebe904fbd8db760f565fc8b7e6dfe681a1b244e54c4b8d6efc18cd24c`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a337dc2d7268d765d648d1e9f00c1bd0141c4ebd97517af6e70a1ae769570fc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116914307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bf1d980307868c5285fb41eb5cb60b704d968123cf0ca47ee53714c7645df2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:13:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:13:28 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:13:29 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:13:29 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:13:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:13:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:14:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:14:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:14:11 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:14:12 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:14:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:14:12 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:14:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae80fa4a705d67389589017094f9ce1f353ab854515898da65e9038b1fcc6eaa`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834882ca1c206aea80fbcb1d5d74046cf818f46a56d7a432eaf0798626a07c69`  
		Last Modified: Tue, 23 Aug 2022 22:24:23 GMT  
		Size: 72.4 MB (72351677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a1b3d4ea228007ec52b61b5059f528b2d83b73655172c0f96b757258392eaa`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12605c90d2820db47e3ce2394d21b5e9de5c220b37947b24c7e356b29f369283`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.4` - linux; s390x

```console
$ docker pull mariadb@sha256:90b47f090b353f8cf17bdd7ac84f8b20b4ac429e55a9720452da05c9fa1d4e66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105054403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317f193d8bc5732ac7b96e4632a52f720e66edac49e5e2884107c6fbcde399d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:45 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:56:45 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:56:45 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:56:45 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:56:45 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:57:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:57:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:57:13 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:57:13 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:57:14 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:57:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d963003499efb47d350dd16f1bdf62576658cbd1439a5746a688e0e52ff3ba5`  
		Last Modified: Tue, 23 Aug 2022 23:11:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee3ca001c631f58001b7c458cf6f06ac997dd1fc315114d17a56abf8c301688`  
		Last Modified: Tue, 23 Aug 2022 23:11:14 GMT  
		Size: 68.5 MB (68548867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177cbd11589739b81938cdcfabca35e5d4baa8a454cb47796731d5ef65088bcb`  
		Last Modified: Tue, 23 Aug 2022 23:11:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626aa0b7d36807a4b170bdb52a39df0f233f36079f3f3b12e3212dcbc44a23ad`  
		Last Modified: Tue, 23 Aug 2022 23:11:05 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.4-jammy`

```console
$ docker pull mariadb@sha256:82b394b4f0ba430948841f7a32d9fb117c489553e0dd112fcba4633211146066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.4-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:d025e1305839b80f3ac44f94bb218c61eb11fd62f9a2e01fff3cf4000a7541fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123938825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e7d13b47b89060a190dd8989796ccdec7705abae43b3e49b7b97bda1bd782f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:30 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 24 Aug 2022 00:02:30 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 24 Aug 2022 00:02:30 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Wed, 24 Aug 2022 00:02:30 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Wed, 24 Aug 2022 00:02:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:54 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:54 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:55 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac50cb207c741b71e7af0e6ff1c929815edb3601a71425f4235b151419c7547`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266e4baee040bf4cfc41fb75bd6f54bd16a04db896e52c0bf1d789ea2401c72`  
		Last Modified: Wed, 24 Aug 2022 00:08:37 GMT  
		Size: 85.4 MB (85440831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c8b5b2463c3b1e5c861dd816638ff90550d57d87c71ad68ada44ff85c8b750`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5f306ebe904fbd8db760f565fc8b7e6dfe681a1b244e54c4b8d6efc18cd24c`  
		Last Modified: Wed, 24 Aug 2022 00:08:25 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.4-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a337dc2d7268d765d648d1e9f00c1bd0141c4ebd97517af6e70a1ae769570fc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116914307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bf1d980307868c5285fb41eb5cb60b704d968123cf0ca47ee53714c7645df2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:13:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:13:28 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:13:29 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:13:29 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:13:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:13:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:14:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:14:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:14:11 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:14:12 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:14:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:14:12 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:14:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae80fa4a705d67389589017094f9ce1f353ab854515898da65e9038b1fcc6eaa`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834882ca1c206aea80fbcb1d5d74046cf818f46a56d7a432eaf0798626a07c69`  
		Last Modified: Tue, 23 Aug 2022 22:24:23 GMT  
		Size: 72.4 MB (72351677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a1b3d4ea228007ec52b61b5059f528b2d83b73655172c0f96b757258392eaa`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12605c90d2820db47e3ce2394d21b5e9de5c220b37947b24c7e356b29f369283`  
		Last Modified: Tue, 23 Aug 2022 22:24:05 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.4-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:90b47f090b353f8cf17bdd7ac84f8b20b4ac429e55a9720452da05c9fa1d4e66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105054403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317f193d8bc5732ac7b96e4632a52f720e66edac49e5e2884107c6fbcde399d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:45 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:56:45 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 23 Aug 2022 22:56:45 GMT
ARG MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:56:45 GMT
ENV MARIADB_VERSION=1:10.8.4+maria~ubu2204
# Tue, 23 Aug 2022 22:56:45 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:57:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:57:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:57:13 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:57:13 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:57:14 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:57:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d963003499efb47d350dd16f1bdf62576658cbd1439a5746a688e0e52ff3ba5`  
		Last Modified: Tue, 23 Aug 2022 23:11:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee3ca001c631f58001b7c458cf6f06ac997dd1fc315114d17a56abf8c301688`  
		Last Modified: Tue, 23 Aug 2022 23:11:14 GMT  
		Size: 68.5 MB (68548867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177cbd11589739b81938cdcfabca35e5d4baa8a454cb47796731d5ef65088bcb`  
		Last Modified: Tue, 23 Aug 2022 23:11:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626aa0b7d36807a4b170bdb52a39df0f233f36079f3f3b12e3212dcbc44a23ad`  
		Last Modified: Tue, 23 Aug 2022 23:11:05 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.9`

```console
$ docker pull mariadb@sha256:c1c533e138ba659003dfb631948a55c7007a377e374e2d6d518de9bb591b8539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.9` - linux; amd64

```console
$ docker pull mariadb@sha256:3b4bcc98c0982745a30b013e8b66233c7313496eae9de6b691963a737f614d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124029543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d138caf7d0f7680129a9dd134f363a23da6be5d76449a93bb5906598d0e06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:02 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:23 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:24 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:24 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710253f0933b7c0e3be3f7a4b4b77cb5ba9ece744177ccbb68472b8b46ce122b`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d5115199c9aa41cc86312e841f5ac0ff84a38ead396deb3ee0a54b01b973b`  
		Last Modified: Wed, 24 Aug 2022 00:07:58 GMT  
		Size: 85.5 MB (85531548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f43d7b59b546061df8a538a2cd4376a400245c54955445749e405d33098d73`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7032a660a4eef799097fd44e9d6a7ae89c6f5a3bb148c9f6515f8b1f800f46`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b68e6672e1dfd013fc5b4fb42b368c534af7e07fce685f287b3a99296e09b2bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117038959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d753a037ef6f672b98d11a6b2b3ddd116a81dea34be15c6b9a40c05fecbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:12:28 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:12:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:13:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:13:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:13:16 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caabbd107834c8bff1673ba81491e0983e459aabc2855d3cf78188307c813365`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3bd7204dda4f3ab271317d058dfb5ef33dfcf95bf4b663c30432f03f3fc3fc`  
		Last Modified: Tue, 23 Aug 2022 22:23:28 GMT  
		Size: 72.5 MB (72476332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c727c5cc2517b4755a4205d2b008e2454929862a191ba73a55c1dca7f58e1`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714083977b193354161a308393ac0d56d68efc4be6cb3d26edfff12859e0a23e`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9` - linux; s390x

```console
$ docker pull mariadb@sha256:c7116a14d5deca65bec93cec3a99662a47f1d1c85330b3aefa2b5610f932d26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105140532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ac87f204e8050170fd16b50ad4652cc817bd6d937b569cb01e04580d15fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:01 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:56:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:56:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:56:36 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:56:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab6e11c25e790046065da17a078d6f1068e0d5f9988a46f3ec1a381810189c`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6ddbdfd315c17604dd29c4cceec21edcd2a1f5b6de90cb34814ec25f1d944`  
		Last Modified: Tue, 23 Aug 2022 23:05:50 GMT  
		Size: 68.6 MB (68634999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814afb85a75d500819281410f8832949cdfeb711ca835ef097214003f8f058a8`  
		Last Modified: Tue, 23 Aug 2022 23:05:41 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673619860a5c62749b0f25f505cc892fb9cc9d5cedfb493a12a10520c01b57d8`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.9-jammy`

```console
$ docker pull mariadb@sha256:c1c533e138ba659003dfb631948a55c7007a377e374e2d6d518de9bb591b8539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.9-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:3b4bcc98c0982745a30b013e8b66233c7313496eae9de6b691963a737f614d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124029543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d138caf7d0f7680129a9dd134f363a23da6be5d76449a93bb5906598d0e06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:02 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:23 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:24 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:24 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710253f0933b7c0e3be3f7a4b4b77cb5ba9ece744177ccbb68472b8b46ce122b`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d5115199c9aa41cc86312e841f5ac0ff84a38ead396deb3ee0a54b01b973b`  
		Last Modified: Wed, 24 Aug 2022 00:07:58 GMT  
		Size: 85.5 MB (85531548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f43d7b59b546061df8a538a2cd4376a400245c54955445749e405d33098d73`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7032a660a4eef799097fd44e9d6a7ae89c6f5a3bb148c9f6515f8b1f800f46`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b68e6672e1dfd013fc5b4fb42b368c534af7e07fce685f287b3a99296e09b2bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117038959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d753a037ef6f672b98d11a6b2b3ddd116a81dea34be15c6b9a40c05fecbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:12:28 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:12:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:13:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:13:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:13:16 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caabbd107834c8bff1673ba81491e0983e459aabc2855d3cf78188307c813365`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3bd7204dda4f3ab271317d058dfb5ef33dfcf95bf4b663c30432f03f3fc3fc`  
		Last Modified: Tue, 23 Aug 2022 22:23:28 GMT  
		Size: 72.5 MB (72476332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c727c5cc2517b4755a4205d2b008e2454929862a191ba73a55c1dca7f58e1`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714083977b193354161a308393ac0d56d68efc4be6cb3d26edfff12859e0a23e`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:c7116a14d5deca65bec93cec3a99662a47f1d1c85330b3aefa2b5610f932d26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105140532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ac87f204e8050170fd16b50ad4652cc817bd6d937b569cb01e04580d15fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:01 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:56:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:56:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:56:36 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:56:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab6e11c25e790046065da17a078d6f1068e0d5f9988a46f3ec1a381810189c`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6ddbdfd315c17604dd29c4cceec21edcd2a1f5b6de90cb34814ec25f1d944`  
		Last Modified: Tue, 23 Aug 2022 23:05:50 GMT  
		Size: 68.6 MB (68634999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814afb85a75d500819281410f8832949cdfeb711ca835ef097214003f8f058a8`  
		Last Modified: Tue, 23 Aug 2022 23:05:41 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673619860a5c62749b0f25f505cc892fb9cc9d5cedfb493a12a10520c01b57d8`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.9.2`

```console
$ docker pull mariadb@sha256:c1c533e138ba659003dfb631948a55c7007a377e374e2d6d518de9bb591b8539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.9.2` - linux; amd64

```console
$ docker pull mariadb@sha256:3b4bcc98c0982745a30b013e8b66233c7313496eae9de6b691963a737f614d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124029543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d138caf7d0f7680129a9dd134f363a23da6be5d76449a93bb5906598d0e06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:02 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:23 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:24 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:24 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710253f0933b7c0e3be3f7a4b4b77cb5ba9ece744177ccbb68472b8b46ce122b`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d5115199c9aa41cc86312e841f5ac0ff84a38ead396deb3ee0a54b01b973b`  
		Last Modified: Wed, 24 Aug 2022 00:07:58 GMT  
		Size: 85.5 MB (85531548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f43d7b59b546061df8a538a2cd4376a400245c54955445749e405d33098d73`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7032a660a4eef799097fd44e9d6a7ae89c6f5a3bb148c9f6515f8b1f800f46`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b68e6672e1dfd013fc5b4fb42b368c534af7e07fce685f287b3a99296e09b2bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117038959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d753a037ef6f672b98d11a6b2b3ddd116a81dea34be15c6b9a40c05fecbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:12:28 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:12:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:13:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:13:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:13:16 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caabbd107834c8bff1673ba81491e0983e459aabc2855d3cf78188307c813365`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3bd7204dda4f3ab271317d058dfb5ef33dfcf95bf4b663c30432f03f3fc3fc`  
		Last Modified: Tue, 23 Aug 2022 22:23:28 GMT  
		Size: 72.5 MB (72476332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c727c5cc2517b4755a4205d2b008e2454929862a191ba73a55c1dca7f58e1`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714083977b193354161a308393ac0d56d68efc4be6cb3d26edfff12859e0a23e`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9.2` - linux; s390x

```console
$ docker pull mariadb@sha256:c7116a14d5deca65bec93cec3a99662a47f1d1c85330b3aefa2b5610f932d26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105140532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ac87f204e8050170fd16b50ad4652cc817bd6d937b569cb01e04580d15fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:01 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:56:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:56:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:56:36 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:56:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab6e11c25e790046065da17a078d6f1068e0d5f9988a46f3ec1a381810189c`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6ddbdfd315c17604dd29c4cceec21edcd2a1f5b6de90cb34814ec25f1d944`  
		Last Modified: Tue, 23 Aug 2022 23:05:50 GMT  
		Size: 68.6 MB (68634999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814afb85a75d500819281410f8832949cdfeb711ca835ef097214003f8f058a8`  
		Last Modified: Tue, 23 Aug 2022 23:05:41 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673619860a5c62749b0f25f505cc892fb9cc9d5cedfb493a12a10520c01b57d8`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.9.2-jammy`

```console
$ docker pull mariadb@sha256:c1c533e138ba659003dfb631948a55c7007a377e374e2d6d518de9bb591b8539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.9.2-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:3b4bcc98c0982745a30b013e8b66233c7313496eae9de6b691963a737f614d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124029543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d138caf7d0f7680129a9dd134f363a23da6be5d76449a93bb5906598d0e06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:02 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:23 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:24 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:24 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710253f0933b7c0e3be3f7a4b4b77cb5ba9ece744177ccbb68472b8b46ce122b`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d5115199c9aa41cc86312e841f5ac0ff84a38ead396deb3ee0a54b01b973b`  
		Last Modified: Wed, 24 Aug 2022 00:07:58 GMT  
		Size: 85.5 MB (85531548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f43d7b59b546061df8a538a2cd4376a400245c54955445749e405d33098d73`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7032a660a4eef799097fd44e9d6a7ae89c6f5a3bb148c9f6515f8b1f800f46`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9.2-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b68e6672e1dfd013fc5b4fb42b368c534af7e07fce685f287b3a99296e09b2bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117038959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d753a037ef6f672b98d11a6b2b3ddd116a81dea34be15c6b9a40c05fecbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:12:28 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:12:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:13:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:13:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:13:16 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caabbd107834c8bff1673ba81491e0983e459aabc2855d3cf78188307c813365`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3bd7204dda4f3ab271317d058dfb5ef33dfcf95bf4b663c30432f03f3fc3fc`  
		Last Modified: Tue, 23 Aug 2022 22:23:28 GMT  
		Size: 72.5 MB (72476332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c727c5cc2517b4755a4205d2b008e2454929862a191ba73a55c1dca7f58e1`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714083977b193354161a308393ac0d56d68efc4be6cb3d26edfff12859e0a23e`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9.2-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:c7116a14d5deca65bec93cec3a99662a47f1d1c85330b3aefa2b5610f932d26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105140532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ac87f204e8050170fd16b50ad4652cc817bd6d937b569cb01e04580d15fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:01 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:56:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:56:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:56:36 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:56:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab6e11c25e790046065da17a078d6f1068e0d5f9988a46f3ec1a381810189c`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6ddbdfd315c17604dd29c4cceec21edcd2a1f5b6de90cb34814ec25f1d944`  
		Last Modified: Tue, 23 Aug 2022 23:05:50 GMT  
		Size: 68.6 MB (68634999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814afb85a75d500819281410f8832949cdfeb711ca835ef097214003f8f058a8`  
		Last Modified: Tue, 23 Aug 2022 23:05:41 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673619860a5c62749b0f25f505cc892fb9cc9d5cedfb493a12a10520c01b57d8`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:jammy`

```console
$ docker pull mariadb@sha256:cbcf33d6dab0a014dfc9450148f3dcf42c8ae77635b3c8e948e3af09562a989e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:3b4bcc98c0982745a30b013e8b66233c7313496eae9de6b691963a737f614d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124029543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d138caf7d0f7680129a9dd134f363a23da6be5d76449a93bb5906598d0e06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:02 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:23 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:24 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:24 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710253f0933b7c0e3be3f7a4b4b77cb5ba9ece744177ccbb68472b8b46ce122b`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d5115199c9aa41cc86312e841f5ac0ff84a38ead396deb3ee0a54b01b973b`  
		Last Modified: Wed, 24 Aug 2022 00:07:58 GMT  
		Size: 85.5 MB (85531548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f43d7b59b546061df8a538a2cd4376a400245c54955445749e405d33098d73`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7032a660a4eef799097fd44e9d6a7ae89c6f5a3bb148c9f6515f8b1f800f46`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1f011a0b21919b39058355d972fea445857869ad1f867eb56bd1d274fd969e88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102470825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f8da7eeabb6549ac946f2b45ffe497556f6ad227d0bd4d41e09e73e6b34097`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:32:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:32:16 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:32:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:32:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:32:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:32:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:33:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:29 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:30 GMT
ARG MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:31 GMT
ENV MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
# Tue, 02 Aug 2022 18:33:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:33:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:33:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:33:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:33:55 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:33:56 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:33:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5bedaed5f8e5343fee312eb2f21894d7b4026a0c692da89fe4f30a432e48b4`  
		Last Modified: Tue, 02 Aug 2022 18:41:32 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f07d81dfa02553c544d772dc3aa04ed6a2e6ad5b810ca742eee9a918786e5f`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 3.6 MB (3594051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b8a20cb609d07274a17b8dd4ae810b6a98f76cf0ad513aa0c03eda46fcbce`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 1.9 MB (1899200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d39cfcf2768f9c1165cc0d3764c3649542f541a1ed3f18bec6283d58553e00`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d230566e80222a9242f97419a6018684f4e324420ee89e4c0395f8107a124c91`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 2.2 MB (2211614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c8c9abaef706c6185822ae21205ab5bc569494c4492a89eef44d8a855315c5`  
		Last Modified: Tue, 02 Aug 2022 18:41:27 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bff43ba5b5f6479659a8a7496d4156615c3cd9439c46779dd3feed3c4511ae`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cb73ef10f93c31f677c6818187b24c6bb65b4cb76ad5ed05e5b31853ef1b73`  
		Last Modified: Tue, 02 Aug 2022 18:42:08 GMT  
		Size: 66.4 MB (66369985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b16804fca7957e5cc3538c9a1a58af3e8e7a9eb0ee3318ffa413c7ebf4c76d4`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffad21dfd527f8685de9b3c864738e88bb8791db49ecdeb988d9d194a20d7cc`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b68e6672e1dfd013fc5b4fb42b368c534af7e07fce685f287b3a99296e09b2bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117038959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d753a037ef6f672b98d11a6b2b3ddd116a81dea34be15c6b9a40c05fecbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:12:28 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:12:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:13:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:13:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:13:16 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caabbd107834c8bff1673ba81491e0983e459aabc2855d3cf78188307c813365`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3bd7204dda4f3ab271317d058dfb5ef33dfcf95bf4b663c30432f03f3fc3fc`  
		Last Modified: Tue, 23 Aug 2022 22:23:28 GMT  
		Size: 72.5 MB (72476332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c727c5cc2517b4755a4205d2b008e2454929862a191ba73a55c1dca7f58e1`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714083977b193354161a308393ac0d56d68efc4be6cb3d26edfff12859e0a23e`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:c7116a14d5deca65bec93cec3a99662a47f1d1c85330b3aefa2b5610f932d26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105140532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ac87f204e8050170fd16b50ad4652cc817bd6d937b569cb01e04580d15fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:01 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:56:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:56:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:56:36 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:56:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab6e11c25e790046065da17a078d6f1068e0d5f9988a46f3ec1a381810189c`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6ddbdfd315c17604dd29c4cceec21edcd2a1f5b6de90cb34814ec25f1d944`  
		Last Modified: Tue, 23 Aug 2022 23:05:50 GMT  
		Size: 68.6 MB (68634999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814afb85a75d500819281410f8832949cdfeb711ca835ef097214003f8f058a8`  
		Last Modified: Tue, 23 Aug 2022 23:05:41 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673619860a5c62749b0f25f505cc892fb9cc9d5cedfb493a12a10520c01b57d8`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:cbcf33d6dab0a014dfc9450148f3dcf42c8ae77635b3c8e948e3af09562a989e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:3b4bcc98c0982745a30b013e8b66233c7313496eae9de6b691963a737f614d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124029543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d138caf7d0f7680129a9dd134f363a23da6be5d76449a93bb5906598d0e06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:19:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 24 Aug 2022 00:00:46 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:00:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 00:00:57 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 00:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 00:01:06 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 00:01:06 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 24 Aug 2022 00:01:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 24 Aug 2022 00:02:02 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Wed, 24 Aug 2022 00:02:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Wed, 24 Aug 2022 00:02:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 24 Aug 2022 00:02:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 24 Aug 2022 00:02:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Aug 2022 00:02:23 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 24 Aug 2022 00:02:24 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Wed, 24 Aug 2022 00:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 00:02:24 GMT
EXPOSE 3306
# Wed, 24 Aug 2022 00:02:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587559f9b58dcc08ed5b9fc08cc82b80ce995a37000098b1cdca2c199ae89f8`  
		Last Modified: Tue, 02 Aug 2022 20:26:32 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7f01dd8c9789fcbc319a914f6dc80a08b62652311d6222d8aa94300f1215`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 3.8 MB (3765804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5f1b1e214ad49dd5fe9fc6d3877b978b07b3508878e514b5d03443036acdd3`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.0 MB (1992926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab08b1f4c596f5c08df73d1e28460d993642f257ddfb44b794b375dbf8c694`  
		Last Modified: Wed, 24 Aug 2022 00:07:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1093648eca210c840879dc3b45d99ebac1345e4ff58a9c348db3833f7f404a70`  
		Last Modified: Wed, 24 Aug 2022 00:07:17 GMT  
		Size: 2.3 MB (2298217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc76be63b2b96be82d3c6529ca763fc892caebed7f4cad06bc16f60e84333c`  
		Last Modified: Wed, 24 Aug 2022 00:07:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710253f0933b7c0e3be3f7a4b4b77cb5ba9ece744177ccbb68472b8b46ce122b`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d5115199c9aa41cc86312e841f5ac0ff84a38ead396deb3ee0a54b01b973b`  
		Last Modified: Wed, 24 Aug 2022 00:07:58 GMT  
		Size: 85.5 MB (85531548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f43d7b59b546061df8a538a2cd4376a400245c54955445749e405d33098d73`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7032a660a4eef799097fd44e9d6a7ae89c6f5a3bb148c9f6515f8b1f800f46`  
		Last Modified: Wed, 24 Aug 2022 00:07:45 GMT  
		Size: 6.7 KB (6701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1f011a0b21919b39058355d972fea445857869ad1f867eb56bd1d274fd969e88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102470825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f8da7eeabb6549ac946f2b45ffe497556f6ad227d0bd4d41e09e73e6b34097`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:32:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 18:32:16 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 18:32:33 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:32:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:32:42 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:32:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Aug 2022 18:32:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 02 Aug 2022 18:33:28 GMT
ARG MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:29 GMT
ENV MARIADB_MAJOR=10.8
# Tue, 02 Aug 2022 18:33:30 GMT
ARG MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:31 GMT
ENV MARIADB_VERSION=1:10.8.3+maria~jammy
# Tue, 02 Aug 2022 18:33:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
# Tue, 02 Aug 2022 18:33:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 02 Aug 2022 18:33:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 02 Aug 2022 18:33:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 18:33:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 02 Aug 2022 18:33:55 GMT
COPY file:e4da674ce3a4afd5069ca1fdb1c5969db396f58ba4a9105ee3e377f2391b91c5 in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:33:56 GMT
EXPOSE 3306
# Tue, 02 Aug 2022 18:33:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5bedaed5f8e5343fee312eb2f21894d7b4026a0c692da89fe4f30a432e48b4`  
		Last Modified: Tue, 02 Aug 2022 18:41:32 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f07d81dfa02553c544d772dc3aa04ed6a2e6ad5b810ca742eee9a918786e5f`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 3.6 MB (3594051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b8a20cb609d07274a17b8dd4ae810b6a98f76cf0ad513aa0c03eda46fcbce`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 1.9 MB (1899200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d39cfcf2768f9c1165cc0d3764c3649542f541a1ed3f18bec6283d58553e00`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d230566e80222a9242f97419a6018684f4e324420ee89e4c0395f8107a124c91`  
		Last Modified: Tue, 02 Aug 2022 18:41:30 GMT  
		Size: 2.2 MB (2211614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c8c9abaef706c6185822ae21205ab5bc569494c4492a89eef44d8a855315c5`  
		Last Modified: Tue, 02 Aug 2022 18:41:27 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bff43ba5b5f6479659a8a7496d4156615c3cd9439c46779dd3feed3c4511ae`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cb73ef10f93c31f677c6818187b24c6bb65b4cb76ad5ed05e5b31853ef1b73`  
		Last Modified: Tue, 02 Aug 2022 18:42:08 GMT  
		Size: 66.4 MB (66369985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b16804fca7957e5cc3538c9a1a58af3e8e7a9eb0ee3318ffa413c7ebf4c76d4`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffad21dfd527f8685de9b3c864738e88bb8791db49ecdeb988d9d194a20d7cc`  
		Last Modified: Tue, 02 Aug 2022 18:41:57 GMT  
		Size: 6.7 KB (6699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b68e6672e1dfd013fc5b4fb42b368c534af7e07fce685f287b3a99296e09b2bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117038959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d753a037ef6f672b98d11a6b2b3ddd116a81dea34be15c6b9a40c05fecbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:30:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:10:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:10:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:10:46 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:10:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:11:00 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:11:01 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:11:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:12:28 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:12:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:12:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:13:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:13:15 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:13:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:13:16 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a119144d25c65194f5210a2c0785d96c4b9d92c955f354d54e971b66cf0f`  
		Last Modified: Wed, 03 Aug 2022 04:43:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb11655cae670a33415465d29bd89cb9938848c51e472440a30ea85e4f14418`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 4.5 MB (4503149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9f073bf34b13e2d6f3c1e5ece7ad5a8054000543be8679275166ef1b703c4`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 1.9 MB (1921728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459989f6209d8b80dbdf54d9f8ca199da71664fd354e4c5d76a2f5e2e3263cf1`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5255fb655e522ca09ddba8c75ee7be501bdcfbba3fa47fbea1281cca82e669`  
		Last Modified: Tue, 23 Aug 2022 22:22:33 GMT  
		Size: 2.4 MB (2404843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c101d18c7d52ad1f948a16ef3d50a8b748a9ac1d37e114d9971f75f85ef2a9e2`  
		Last Modified: Tue, 23 Aug 2022 22:22:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caabbd107834c8bff1673ba81491e0983e459aabc2855d3cf78188307c813365`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3bd7204dda4f3ab271317d058dfb5ef33dfcf95bf4b663c30432f03f3fc3fc`  
		Last Modified: Tue, 23 Aug 2022 22:23:28 GMT  
		Size: 72.5 MB (72476332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c727c5cc2517b4755a4205d2b008e2454929862a191ba73a55c1dca7f58e1`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714083977b193354161a308393ac0d56d68efc4be6cb3d26edfff12859e0a23e`  
		Last Modified: Tue, 23 Aug 2022 22:23:10 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:c7116a14d5deca65bec93cec3a99662a47f1d1c85330b3aefa2b5610f932d26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105140532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ac87f204e8050170fd16b50ad4652cc817bd6d937b569cb01e04580d15fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:55:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 23 Aug 2022 22:54:31 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:54:31 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 22:55:01 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 22:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 22:55:08 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 22:55:08 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 23 Aug 2022 22:55:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 23 Aug 2022 22:56:01 GMT
ARG MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ENV MARIADB_VERSION=1:10.9.2+maria~ubu2204
# Tue, 23 Aug 2022 22:56:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
# Tue, 23 Aug 2022 22:56:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 23 Aug 2022 22:56:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 23 Aug 2022 22:56:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 23 Aug 2022 22:56:35 GMT
COPY file:7032e58fbba6784f90935fcf1ff3c389e5b2936aa9e1c6b8b291cbb26774ee2e in /usr/local/bin/ 
# Tue, 23 Aug 2022 22:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 22:56:36 GMT
EXPOSE 3306
# Tue, 23 Aug 2022 22:56:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518030038f927b55f39a26dbee5d8d6e8c31cc0ddf7f23268b3dee3f001182c2`  
		Last Modified: Tue, 02 Aug 2022 13:01:03 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8cabf22db4899159613c30bfc0b438ddb1815c02db35a1dd11ec92f073730`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 3.7 MB (3675110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11923e077f6acedb8075b3c2ac4c921b04aefc98f94d3c478948f39dd3e12c38`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 2.0 MB (1955983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69b48e6f7faa35ab401ba6f1d74dd64e4d2e7cf6dcb9a4cd810b423c7cfd5c`  
		Last Modified: Tue, 23 Aug 2022 23:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1adb7f976d562dce7286f9edda1ece0a76de472846be206e78ca740bf1a73e`  
		Last Modified: Tue, 23 Aug 2022 23:02:42 GMT  
		Size: 2.2 MB (2216749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03447a3c7a2a54f12139adee8ceaffc55556a01e73baa2110aacd6a8633e4b4`  
		Last Modified: Tue, 23 Aug 2022 23:02:33 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab6e11c25e790046065da17a078d6f1068e0d5f9988a46f3ec1a381810189c`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6ddbdfd315c17604dd29c4cceec21edcd2a1f5b6de90cb34814ec25f1d944`  
		Last Modified: Tue, 23 Aug 2022 23:05:50 GMT  
		Size: 68.6 MB (68634999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814afb85a75d500819281410f8832949cdfeb711ca835ef097214003f8f058a8`  
		Last Modified: Tue, 23 Aug 2022 23:05:41 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673619860a5c62749b0f25f505cc892fb9cc9d5cedfb493a12a10520c01b57d8`  
		Last Modified: Tue, 23 Aug 2022 23:05:45 GMT  
		Size: 6.7 KB (6697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
