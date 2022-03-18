## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:189961fb494eb150e5b358ed23e9d526d75847abe0e84428cca0f7c629e6cd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7e0deebd9fdf8e46d830911a8c8975a00462147f7d923d7aa7773221eafe5534
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133155232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fb8170f15f6d079a63ed552de428861e093873629a97b5cde83ddf86af5d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:23:28 GMT
ADD file:09b0bc8af49fa3558fb3e8d50daa682180e194cb11ca332d03ca65059e615dfd in / 
# Fri, 18 Mar 2022 05:23:29 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 08:02:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:02:48 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:02:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:03:25 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 18 Mar 2022 08:04:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Mar 2022 08:04:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Mar 2022 08:04:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Mar 2022 08:04:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:57 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Mar 2022 08:04:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:04:58 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:04:58 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:04:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1824cb7e97fbcfc5c6ffea667f8e19cee765d015fef1b8ad70f96252d9713c95`  
		Last Modified: Fri, 18 Mar 2022 05:24:44 GMT  
		Size: 42.1 MB (42110196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5603b74046dbdf928d0641abd36690bf5ef09bec61a2131c3ec7eb4b4c6d8ba4`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c5d7fe8298ed20bcb5c7adbbe025eef7a9de9e5b1e3447936ed9d02b09b7f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc1f1a8427b3e502f4f25dd7acf037e2a2d35927b3201d2711442516c32591b`  
		Last Modified: Fri, 18 Mar 2022 08:07:32 GMT  
		Size: 4.6 MB (4552961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c348d46c25eeb80c794020883a39367c3db1dae41fc9a79aa6fda96d43a51d`  
		Last Modified: Fri, 18 Mar 2022 08:07:31 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2658193beeb76b4b398b4ee7ecc71ebfd580ecf8925d131c8e84598f7c3182`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3694176cd71ffaa30adad12882db7b497d0e83d860f4cbfbdf559213d1fcbb1b`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 47.3 MB (47269558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32d4e62ce97c09e1c91dcf712a5bec3c227e2edcbbc4947ffaf2a7f7acddfb4`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3b55b1e47e4fb94d7b16d8d2d6c298bf1b155b21feed7e8eb3b50060ce91fd`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 38.3 MB (38284179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b3ad406f04dc3a6b8a318c6bf53f8868d1b65941fd2aaf608d5e9a9f4dc33e`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

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
