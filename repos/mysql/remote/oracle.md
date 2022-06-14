## `mysql:oracle`

```console
$ docker pull mysql@sha256:1a3b696ed3413f845968e5fd3d8636e5838ba6be7470aaf9bf7957ccfc17ec52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:940fdfa3dc408fb792a8cceb21cafda4b7cd56ce4fbc32833766bdd2a57d6a4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfb2bcbf716a71cdb2dd51277575869547854e0c57519c03cd5d5cec58a9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:26 GMT
ADD file:837f6c6e7e20067b92edb72e78a8399e6cbbd72dab23db7b5b5a301c58d2a0de in / 
# Tue, 14 Jun 2022 18:23:26 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:39:39 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 18:39:39 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 18:39:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 14 Jun 2022 18:40:04 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:40:05 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:40:06 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 14 Jun 2022 18:40:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 14 Jun 2022 18:40:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 14 Jun 2022 18:40:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:41:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 14 Jun 2022 18:41:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jun 2022 18:41:10 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 14 Jun 2022 18:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jun 2022 18:41:11 GMT
EXPOSE 3306 33060
# Tue, 14 Jun 2022 18:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5f160c0f6cac587a73883b48a8857f5cce0930112792cef25c62510e256e93dc`  
		Last Modified: Tue, 14 Jun 2022 18:24:18 GMT  
		Size: 39.2 MB (39219730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c3d841d1984f858257755bdf734554725af4f926f3b1d1b22f119cce8bda9`  
		Last Modified: Tue, 14 Jun 2022 18:41:49 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f026b3ec1ed102cfe531d812e2063669bad08ac3a0ac68a31e44083d9b9a5f5d`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80b2ddd662a38dbb423dbaa2be04afd41904253b436138b52f2a73aa46a5547`  
		Last Modified: Tue, 14 Jun 2022 18:41:48 GMT  
		Size: 4.5 MB (4535169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7724a6d28d1e789da86c89f0010caa7de0e4747dfcd360fa981a194850951f`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122570b85fec5c1d3bc0c08a48be2657da195b764c9a13b1a791a086c007368`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea018df6cdc3d2aa821feb43a3035926c0c296b3c363e64ab0fa95f144f2e7b`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 47.2 MB (47244178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8066c16abd2efdd49dd1fe3fab6fec9d250b699d9c0227f69c779c8da2c2acd6`  
		Last Modified: Tue, 14 Jun 2022 18:41:44 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd480e7da7ced7cfb1fb54d07fc5eb08057151be162150bd053f4eb89d9ba85f`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 39.7 MB (39698832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b680e02f092e5330cf0200abf3ba02bddc3d440d02ebb11ec6ed8bf2ba3155`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:afc6503454a50cb7c6e0f15679f78f28a69c64ef9c13ab250b03868327d22964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138552519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d55b4cff902af2f58c08c9cb28ec9ec7ea498734d9e2b29b8211cab1399a0e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:52:38 GMT
ADD file:263fe8ce0663428b324fa2909814084a77bf17118d772058d41546b804a4b968 in / 
# Tue, 17 May 2022 22:52:39 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:09:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 17 May 2022 23:09:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 17 May 2022 23:09:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 May 2022 23:09:26 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 17 May 2022 23:09:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 17 May 2022 23:09:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 May 2022 23:09:30 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:09:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 May 2022 23:09:56 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:10:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 May 2022 23:10:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 May 2022 00:06:13 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 24 May 2022 00:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 May 2022 00:06:14 GMT
EXPOSE 3306 33060
# Tue, 24 May 2022 00:06:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0dbddf5847a3e154a061766ddebe6a3cae471c97cabb3be2871f6d91f265d137`  
		Last Modified: Tue, 17 May 2022 22:53:43 GMT  
		Size: 38.0 MB (38012703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db29b0b5a771d422a5f85337ad705ae13b90861da7c4ae8a2d3020b42d0d4892`  
		Last Modified: Tue, 17 May 2022 23:10:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3855c850e40abd0de4601587237af854d07522e10e3bb9ee0e8c66b40ae49911`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a57b88152cf6fe699baa66b60fd8c2f07daef18b1931fae4dfc7c92d5d48ae5`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 4.3 MB (4342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac9375febdd7998b9cc129e95d554b5b9d024f9ecf3053d3e7156a31279923f`  
		Last Modified: Tue, 17 May 2022 23:10:55 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199a4e720f0e82bafd1852cdf3a57870a449bcb60c197daf349869c4d332bb3`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebac76248d98ab600a56814d6569f0e4f4799aceb8bc8d8999f1b88938873e6`  
		Last Modified: Tue, 17 May 2022 23:11:00 GMT  
		Size: 53.3 MB (53299522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6eb52402d98a9e93f419ca2bc248862a3b2b7e0c0fc6800cadd1622dc46e9`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef5d943dd79edceeeeb858d6e3e80aa85a14a1f402e70156d2fd61d6e5f60a4`  
		Last Modified: Tue, 17 May 2022 23:11:01 GMT  
		Size: 42.0 MB (42030739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd8fe16828e527c9aa77b2da2af6a7ac4b797b59113d833c84b4400434b2012`  
		Last Modified: Tue, 24 May 2022 00:06:32 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
