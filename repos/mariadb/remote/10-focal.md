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
