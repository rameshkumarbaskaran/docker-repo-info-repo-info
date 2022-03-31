## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:041a3f0b3d58771afc64762b46289385f2b9126a14ab7b5895e83b87fd26f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:39b3c2650e24da10a4cb31f589e4e4aff70f2f732283ccd05390781e19cec5e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133160323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca4d64ca8783b3263c6bd28f186b4b909b01afa6c06b4a0ce41cc693d0b2ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:47 GMT
ADD file:eaa532cad071c531a759e73fd0fd381f440f180ab45b05a74314f10b0374df67 in / 
# Tue, 29 Mar 2022 18:35:47 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:10:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:10:42 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:11:06 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 31 Mar 2022 02:11:07 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 31 Mar 2022 02:11:07 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:11:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 31 Mar 2022 02:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 31 Mar 2022 02:11:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 31 Mar 2022 02:11:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Thu, 31 Mar 2022 02:12:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 31 Mar 2022 02:12:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 31 Mar 2022 02:12:06 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 31 Mar 2022 02:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:12:06 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:12:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4430e06691f65e516df7d62db0ee5393acea9ade644cc6bc620efef0956dd17`  
		Last Modified: Tue, 29 Mar 2022 18:36:53 GMT  
		Size: 42.1 MB (42113609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99677fe408e062a57b32fb00d5ff00e4eab318db52b12da3c7a4dbedf9ad6244`  
		Last Modified: Thu, 31 Mar 2022 02:13:48 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911aa3c638bfef7796ef2177249b0d29ad0e6fdada580629689c49a92f2fb602`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 928.8 KB (928834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a50ae0f36756838cc7b35ef9bfe9c1e123fd92120fa773506ba4a5dc44c35f2`  
		Last Modified: Thu, 31 Mar 2022 02:13:46 GMT  
		Size: 4.6 MB (4556552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e229cecb99fa4470f4b33d9c67dac8ec41c198b819f86b61f33239a56b07602`  
		Last Modified: Thu, 31 Mar 2022 02:13:45 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1790c22e04b08b7c8530b41dc5c1ae59f6bc59768164ec87cbf824042841602`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99e6dd61db9fba984084bd6bb56accf425a248ef7f296e8a852caca0aa863d3`  
		Last Modified: Thu, 31 Mar 2022 02:13:51 GMT  
		Size: 47.3 MB (47274212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb6c638025985d50b50df0eae62d65fa7b642cf514cfabca51641e862347de`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc8a66483d763edfb9ee13132e5bb5b6bbddff5a3cf58c6a88f00c9ac202eb`  
		Last Modified: Thu, 31 Mar 2022 02:13:50 GMT  
		Size: 38.3 MB (38277617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52190d1e6a3f83f9986a3a56ea49a2353f1dd7844356abef3c48c024069d4daa`  
		Last Modified: Thu, 31 Mar 2022 02:13:43 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a84c40eb932fc324b1232320a83a91bdd0e25292400e44690c956fc036a5826
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141174013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3f4a2767a37c46e2f5424f1f0e8e79ace6fad52400c3220a6b7f7092b52aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 19:36:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 30 Mar 2022 19:36:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 30 Mar 2022 19:36:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 30 Mar 2022 19:36:52 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 30 Mar 2022 19:36:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 30 Mar 2022 19:36:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 30 Mar 2022 19:36:56 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:36:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 30 Mar 2022 19:37:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 30 Mar 2022 19:37:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 30 Mar 2022 19:37:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:37:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 30 Mar 2022 19:37:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 30 Mar 2022 19:37:52 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 30 Mar 2022 19:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 19:37:53 GMT
EXPOSE 3306 33060
# Wed, 30 Mar 2022 19:37:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab860100fd06bf966bba43e945a81bc929141ededd09d9ac425c6f84f6e3e03`  
		Last Modified: Wed, 30 Mar 2022 19:38:24 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beca8ba6c49cf952f7d2a549637ac71b887bba93a5e30f8e8cf1858369fb67d`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c660f342d4fc90e2cae9584677828102e44965aac6e26780916a1e8ef2ff18ee`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 4.4 MB (4378770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ff8141a9459038f2bc38cd3ded605c6f405d4daf7d56cf6b4f52dd9a2cb5dd`  
		Last Modified: Wed, 30 Mar 2022 19:38:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de35ab51f9a083208854e695dc8879ecf7b9820ef90d9c2c356219ba2651fc`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fd10c0fb45dc51fe4815d510ad7c71fef44e80dd9393308f7ad1a475c465c`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 53.4 MB (53429900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42744cc7790693010c1abb7779bc759b995d9e50d8904bd37afebaf941dcf12b`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cc9d0d65fd6d9afa6e8bcca9941cd6fdaab5a37ee45ce68ea4def7528d673a`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 40.5 MB (40479681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f188c7be958b84ecc16d325c13dd32543ff1e126d9fe14bec3b8397ec173c`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
