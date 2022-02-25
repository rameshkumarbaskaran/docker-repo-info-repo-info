## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:7bab537633b1955d01d10fcea459da545d1fb8bd5345ecb7934fa22cf59f8d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f82078cf4647dab1229b20ce5f0b877fc9d0ff1e004fe5ed381ac49111bd2e31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123652103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4d7f4f7f485571b1ee8ed8cc37368884da5e73b1db25b851ef12d4fdabc94e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:33:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:33:55 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:33:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 25 Feb 2022 03:34:10 GMT
RUN set -eux; 	yum install -y 		gzip 		xz 	; 	yum clean all
# Fri, 25 Feb 2022 03:34:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 03:34:47 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 25 Feb 2022 03:34:47 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Fri, 25 Feb 2022 03:34:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 03:35:07 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 03:35:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 03:35:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Fri, 25 Feb 2022 03:35:27 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:35:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:35:28 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:35:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:35:28 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:35:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4915557694f2e99ba4f3c31018dd343c5dd684cc17dfc82bc6907c0ad8b7c7be`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda14bdaa732132cfb0a98e28a5372b750b07f7c701dd3f23b27209d91359dd0`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 930.2 KB (930235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717da021737923f3dedb7a5d42e088a49fd88858199b4896c90e26a12b980725`  
		Last Modified: Fri, 25 Feb 2022 03:36:24 GMT  
		Size: 2.7 MB (2667688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c870db35ffe1eca150aea5d46e9d3c8c7351a8117b7f880e48cb3fd83f54b8c`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9e012335bb37e2d78a5b25ae542ed05eeecc9c7ee04784e0a2b82a09ef9e04`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dfabeb5ffffa978096a9dd68b54bbc1dc5117a5b6c11a0b9fc9f95b8802448`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 25.4 MB (25397512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fa53264d9d4fcd7ba835996d0246996ff398b8e06dbe6e44852828002684b4`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a237e3df161318234fdec2f8c2cdbfb6386cb86d7b9c565e3545532daefe6643`  
		Last Modified: Fri, 25 Feb 2022 03:36:29 GMT  
		Size: 46.3 MB (46316473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d643c0f9440b2ba54a6c4bfe5e5033aeaa2c68c1831c997c3fe937c37f4721d5`  
		Last Modified: Fri, 25 Feb 2022 03:36:21 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
