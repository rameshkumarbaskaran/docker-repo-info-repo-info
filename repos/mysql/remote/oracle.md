## `mysql:oracle`

```console
$ docker pull mysql@sha256:4377686768c90f2048b264d5a35b0e5946e04e7d6135ff9a6b0095ec09841c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9e1153be4b9c62a158d15b0e6f77799759bcd8a0766d3bb7038272fe21179370
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132915921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110c7218bb7188c986e7febc2f55d6a959818ac34d4d345a65aa7f98613a4d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:31:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:31:44 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:31:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:23:08 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:23:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:23:44 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:23:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:24:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:24:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:24:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:24:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:24:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:24:54 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:24:54 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:24:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5207ba089c5352dfd5cafa4419213f7e6c2dfb2a3d8301f9911ec66fc683c9`  
		Last Modified: Fri, 25 Feb 2022 03:36:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598adc979ae4bcf156eb841c681302fa8f44b58dea06ce95ccf11afb915fd3c2`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84657b0f541b69d0df5959c2a2bf58e9015de5f8e3aec3604f07692e18bea39a`  
		Last Modified: Tue, 08 Mar 2022 19:28:33 GMT  
		Size: 4.5 MB (4549263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b564ce0a68e22f654e153a1aba91e74956614f223ba2ccadb4250f1527c5e0d`  
		Last Modified: Tue, 08 Mar 2022 19:28:31 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5790554ab14a56904f0c6c10c45bb623c160349b3590540ac790c931eadaedf2`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c8157d30bc26ba6e81fa5e10143c100ed056a439a0836568678490d46d0a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 47.3 MB (47263779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390e812ba33fe1baf908f76e9ab2e26607cc5d7790893c4f7c20502ff9702a0`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c924b76189376a203d08a1c022f536033ef154ad1c29842d233347101a1b8fc`  
		Last Modified: Tue, 08 Mar 2022 19:28:37 GMT  
		Size: 38.3 MB (38283274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a3deabc6af673361daaf9cd0bde8f2da0054e0ee36cb3b0a2825d364c8df16`  
		Last Modified: Tue, 08 Mar 2022 19:28:29 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd32a12635aee6af9d552ec32dd353a8c5abe5726e931023a3b6c12b07eb55b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141154782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0356e0d737001e53d9109c189846ca8a8dcb6dfa5058522fac5ff0590757a7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:58:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 02:58:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 02:58:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:50:32 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 08 Mar 2022 19:51:15 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:51:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 08 Mar 2022 19:51:17 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:51:18 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:51:40 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:51:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:51:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Tue, 08 Mar 2022 19:52:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:52:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:52:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:52:13 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:52:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e43073605675017fa1d3f45abfea0fa0d6b3f0dcc26eb29a4920adc5d49b`  
		Last Modified: Fri, 25 Feb 2022 03:00:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811e76642f83f9e9101fd42b5f55528b93b5e1943f6d61006f71ee6291bcde0`  
		Last Modified: Fri, 25 Feb 2022 03:00:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a8bda1feeb7c2f1d3be071ebe0e2eb0fcd0ccd3ead359c52ec1aade8fb1c81`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 4.4 MB (4387324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2e1490447a6058e6894a33d6e3059a6a8e3f77d9b5015529ecf481747a6383`  
		Last Modified: Tue, 08 Mar 2022 19:52:37 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbcebabf3bd13e9e4e457f8f863a5e30541efd7edf9a7321acf231d69f52c24`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f336d193ba9eb36ca50acb329aad504ddc5fb057c38baa92cdadb136243d351a`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 53.4 MB (53435007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377fdaaf480b2bc83cc6dc95000b54c3ac4d858319775baf4bcba5a9c12002f`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77464d80dfef5c59883655a88a449266f939dc59c01727245d89ac8648290f34`  
		Last Modified: Tue, 08 Mar 2022 19:52:42 GMT  
		Size: 40.5 MB (40514019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01868f6e8e34bb8f26a9cc3da8ee584ab3e0a726936f325928a413a9f68853a6`  
		Last Modified: Tue, 08 Mar 2022 19:52:34 GMT  
		Size: 5.1 KB (5143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
