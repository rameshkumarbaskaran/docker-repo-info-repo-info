## `mysql:oracle`

```console
$ docker pull mysql@sha256:ba3f6b2ae3caa82eac6c23aee3abd88381101f6e9a001d39466b2777fffdde06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dad4eee297ae4453beddfdf5921c001a26cb14be2bb1748f25e18747fcb3ba7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155439967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad405c51acf652c5191416adf3309de93f77ff0c9217d85f2f809d5f5d9a26a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 23:40:03 GMT
ADD file:b9db410ba951fb740a34187417442b96a27a7fd918b16023c16cb1b0777b292f in / 
# Thu, 23 Feb 2023 23:40:04 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 23:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 23:56:02 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 23:56:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 23:56:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 23:56:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 23:56:29 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 23:56:29 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 23:56:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 23:56:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 23:56:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 23:56:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 23:57:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 23:57:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 23:57:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 23:57:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 23:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 23:57:32 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 23:57:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fdf42ad2544e3a5379ea5e0050457e87df46409adba81dba4686a3efc595ccd2`  
		Last Modified: Thu, 23 Feb 2023 23:40:48 GMT  
		Size: 43.5 MB (43461050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923b645414f5105d2c3a1bf6b146916472842b362b5f10bb6276a3329b18e443`  
		Last Modified: Thu, 23 Feb 2023 23:57:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83902a79075e521165e1deaaae38fd0ff216b20ee1badaec8507e1931eca4589`  
		Last Modified: Thu, 23 Feb 2023 23:57:54 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb14f86bde28a9538763e04f7868abf6a284d5b6c6491aa445e673b5f426772`  
		Last Modified: Thu, 23 Feb 2023 23:57:53 GMT  
		Size: 4.5 MB (4458520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec26d0e9a62d3ed49503175473e68bf7a8981d8c29557484af67dbd66cc9ef8f`  
		Last Modified: Thu, 23 Feb 2023 23:57:52 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bde93ebd7c103f7655aeb5c229c0520c090531b0d93883e8e848e0ebac934f9`  
		Last Modified: Thu, 23 Feb 2023 23:57:52 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877e8353012d100c2909f8f797f2839371b6c28902bce5410a076e1002107115`  
		Last Modified: Thu, 23 Feb 2023 23:57:56 GMT  
		Size: 55.6 MB (55614337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a5fc068f835de1d7d6f2cb8083e162b6298a7982d44174491883cae67a0d77`  
		Last Modified: Thu, 23 Feb 2023 23:57:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6952f0e6afaa3499993b2e8d0744477f9d209076bd8b0538f96623c63589d472`  
		Last Modified: Thu, 23 Feb 2023 23:57:58 GMT  
		Size: 51.0 MB (50983391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e00194a8d15bb2de6954768582c366c22f5feee22a650e3713ea84a2a20f6d7`  
		Last Modified: Thu, 23 Feb 2023 23:57:51 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c604291c18fb6ce2f96e3c790a98517cb937ac104d09c251da307fc172a6a1`  
		Last Modified: Thu, 23 Feb 2023 23:57:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
