## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:dc83d453274ad202af2c283d63b6d1a6639de8af31fb4b9f47a4e02fb3eb7004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7393ba5c8671f58923b3798cf4bf1be4143830bd7d42f656befa3eade6d862b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133138390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396873955d6abc41308a7d35c3a1d23c775d7f13231a126848c73ce736f388e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 24 Mar 2022 01:39:10 GMT
ADD file:c0f0a367bc612431ac9286b506fef5505e0b5f3969515486d8052ec381524261 in / 
# Thu, 24 Mar 2022 01:39:10 GMT
CMD ["/bin/bash"]
# Thu, 24 Mar 2022 02:12:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 24 Mar 2022 02:12:04 GMT
ENV GOSU_VERSION=1.14
# Thu, 24 Mar 2022 02:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 24 Mar 2022 02:12:26 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 24 Mar 2022 02:12:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 24 Mar 2022 02:12:27 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 24 Mar 2022 02:12:27 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Thu, 24 Mar 2022 02:12:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 24 Mar 2022 02:12:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 24 Mar 2022 02:12:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 24 Mar 2022 02:12:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Thu, 24 Mar 2022 02:13:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 24 Mar 2022 02:13:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 24 Mar 2022 02:13:24 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 24 Mar 2022 02:13:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 02:13:24 GMT
EXPOSE 3306 33060
# Thu, 24 Mar 2022 02:13:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9d3d14d30b79ab021a558da3520be505bd2c5ab0f4c85aa07a3ed43524cea2f`  
		Last Modified: Thu, 24 Mar 2022 01:40:02 GMT  
		Size: 42.1 MB (42111482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c34c1c3d334fb2ab9c8d9c0195c46a22a08dc4d53f5cd8260dfa8c9130527c`  
		Last Modified: Thu, 24 Mar 2022 02:13:59 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edd8203272bf73c540c0edcdca1c2668dba76d53fed2a0ab5e67da19b7afe8c`  
		Last Modified: Thu, 24 Mar 2022 02:13:58 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4579ce2fbc2e8b1f50e6db4baccf038f1339415e4e4f205b6525ac976c896d`  
		Last Modified: Thu, 24 Mar 2022 02:13:58 GMT  
		Size: 4.5 MB (4546975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fbf1e34da756947373b1c081a452ca1bd648aee10625d68f255dfaa626c016`  
		Last Modified: Thu, 24 Mar 2022 02:13:57 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e1e95a4b5094db5db1154008980c898c0715849fbc8c4a5fc3dbed6073c2ef`  
		Last Modified: Thu, 24 Mar 2022 02:13:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0074abeebc046de5186ef3d222c170beb09629607dd93bfce85be128a9a07633`  
		Last Modified: Thu, 24 Mar 2022 02:14:03 GMT  
		Size: 47.3 MB (47267258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c727cb58a0450cb56a6d163e0b5418430e30f7c276592763809016e6f7e04f3e`  
		Last Modified: Thu, 24 Mar 2022 02:13:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fb1a877d961ee9a8d5ee2171e6167ca917f03075cda3e6d49e11ce5bc06cba`  
		Last Modified: Thu, 24 Mar 2022 02:14:02 GMT  
		Size: 38.3 MB (38274331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386346d38ca10d69f485b26793e5ba51e680934d8528ca250b7829a645a7d371`  
		Last Modified: Thu, 24 Mar 2022 02:13:55 GMT  
		Size: 5.1 KB (5145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45660786256eb018f00afeaaf09217c7f44964c6933930ed2d1134e5d929e7f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141175330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c014d8ea9ceba0f6f4814b90ee7e1aed99d3f5018f878ec2ed7af076f5709f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 24 Mar 2022 04:46:53 GMT
ADD file:9674a82df5b1239197195a2f3626b6e5eab1f7c671cdf25578626e3eb6692f53 in / 
# Thu, 24 Mar 2022 04:46:53 GMT
CMD ["/bin/bash"]
# Thu, 24 Mar 2022 10:13:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 24 Mar 2022 10:13:33 GMT
ENV GOSU_VERSION=1.14
# Thu, 24 Mar 2022 10:13:36 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 24 Mar 2022 10:13:57 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 24 Mar 2022 10:13:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 24 Mar 2022 10:14:00 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 24 Mar 2022 10:14:01 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Thu, 24 Mar 2022 10:14:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 24 Mar 2022 10:14:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 24 Mar 2022 10:14:26 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 24 Mar 2022 10:14:27 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Thu, 24 Mar 2022 10:14:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 24 Mar 2022 10:14:53 GMT
VOLUME [/var/lib/mysql]
# Thu, 24 Mar 2022 10:14:54 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 24 Mar 2022 10:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 10:14:55 GMT
EXPOSE 3306 33060
# Thu, 24 Mar 2022 10:14:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:443da1826734425262e1c8e7c345e160e645bcdffe66214c9b5584e7cefb32ae`  
		Last Modified: Thu, 24 Mar 2022 04:47:52 GMT  
		Size: 42.0 MB (42018766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f7cc106e22c5e95f89a2e4f2616d525752dfa7301842fd12901e957aa08789`  
		Last Modified: Thu, 24 Mar 2022 10:15:28 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2b80b92771acc1c9ae2b2516ed3c50f5923937fbc469bc0989821b87d98b2b`  
		Last Modified: Thu, 24 Mar 2022 10:15:26 GMT  
		Size: 857.2 KB (857153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6d2be09305ceacfcbedc46776e4a2758398f3cf135a30e49f9acacbf226cbf`  
		Last Modified: Thu, 24 Mar 2022 10:15:27 GMT  
		Size: 4.4 MB (4378867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ea35636bf9094f3efbedcda737775e8bcfc5e2704f7751086a101c842e879`  
		Last Modified: Thu, 24 Mar 2022 10:15:26 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5231775d2b4e41d85db4f105a1934364392d1772c814864c6eff083c3a19e630`  
		Last Modified: Thu, 24 Mar 2022 10:15:24 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e03756e98165702ff9372577ba8ff0105bafea3593fcc6480aed9a8d055c19`  
		Last Modified: Thu, 24 Mar 2022 10:15:32 GMT  
		Size: 53.4 MB (53430017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3441a4eec69f1ef17dbcd8d187d04ba63e523aaad0983916e7671bfbc9e384e6`  
		Last Modified: Thu, 24 Mar 2022 10:15:24 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166f5142bdfdc4a1d892bbe7321ef1bc565df72f8c76e89bccfb3317fe6ab95c`  
		Last Modified: Thu, 24 Mar 2022 10:15:31 GMT  
		Size: 40.5 MB (40481111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7d0b2cc84d36926c4bf673b382f6d794560e0517144c6a98118fcff50159e5`  
		Last Modified: Thu, 24 Mar 2022 10:15:24 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
