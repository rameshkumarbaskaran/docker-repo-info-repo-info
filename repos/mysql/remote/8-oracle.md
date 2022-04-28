## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:a9f1a19f7b38fa1528e25a83f18881bd6e2b7eed54396f39ebd9bad4e5aabf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e2e3ac9e2e250f5a732aa19e7abbecaddd8b6ca0062219639b63d712cc896101
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134826957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb7e0211b3307d63627318adc7ded02adf2f286fcd01a9a9eb29d497dff9325`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 27 Apr 2022 20:33:04 GMT
ADD file:9893213a9ea238f53ac68d87a3cf2f05d86763688392e5ddb6a2c9b60d3550a6 in / 
# Wed, 27 Apr 2022 20:33:05 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 22:18:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 27 Apr 2022 22:18:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 27 Apr 2022 22:18:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 27 Apr 2022 22:18:28 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 27 Apr 2022 22:18:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 27 Apr 2022 22:18:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 27 Apr 2022 22:18:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:19:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 27 Apr 2022 22:19:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:24 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:24 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:38a980f2cc8accf69c23deae6743d42a87eb34a54f02396f3fcfd7c2d06e2c5b`  
		Last Modified: Wed, 27 Apr 2022 20:33:57 GMT  
		Size: 42.1 MB (42114164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfb98692c91e41758cca49b67e9d047a2b0b9330b7b72fbff20a4c50865e5b5`  
		Last Modified: Wed, 27 Apr 2022 22:21:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12707a593559027a9ae6ecf82c947caf83dea80b0bb7dd42c59fd1b95f8701d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e11d97b12251011247579c13626ff8dfb07b0e6dd8eb90e7abc3553bedc04d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 4.6 MB (4558301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9923677ea4133dd45c8ca78f72f6f375732f0dd79e314ad3b1f0cc120d59010`  
		Last Modified: Wed, 27 Apr 2022 22:21:15 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ea275311cdcc42db37cacafb4c63481f6341e971dc3a8b6bef67cca06a82d`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b618919e74db0e4a09bddba62fdc562d4955d20b32bc23c4414416b64f92dc61`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 47.3 MB (47267824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7481ce0984d0580224176c0926e2797d941accba91da8b98b343294be1ad66ec`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d98e5de332ce6dd030a782b4f0945f0b6b19b02b04f9a5aca1799524549cc85`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 39.9 MB (39948341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798d9de77592cc395f2d2034b096fc1cdeb02ebc88dcbfd336b3c1ed30bfcc66`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8048d192687a4c073980e0b7937c936f1abdba81c9aa5cb57c471aaa45df29bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142800591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183e8d92445a13e873ad70f076ae26f1bd274782aa9516ce5a097b33df1bede6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 27 Apr 2022 22:55:53 GMT
ADD file:6fef7a4ab2de57c438dad76949e7eb87cfb1ea6f45b0f2423f71188efdaa0d8e in / 
# Wed, 27 Apr 2022 22:55:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 23:54:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 27 Apr 2022 23:54:34 GMT
ENV GOSU_VERSION=1.14
# Wed, 27 Apr 2022 23:54:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 27 Apr 2022 23:55:11 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 27 Apr 2022 23:55:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 27 Apr 2022 23:55:14 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 23:55:15 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 23:55:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 27 Apr 2022 23:55:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 27 Apr 2022 23:55:52 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 27 Apr 2022 23:55:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 23:56:25 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 27 Apr 2022 23:56:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 23:56:28 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 23:56:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 23:56:29 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 23:56:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:416105dc84fc8cf66df5d2c9f81570a2cc36a6cae58aedd4d58792f041f7a2f5`  
		Last Modified: Wed, 27 Apr 2022 22:56:57 GMT  
		Size: 42.0 MB (42018977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6894aebbb30b27680e78853b2d191b2b12448f8ef1e18aaddb60d63145fec32`  
		Last Modified: Wed, 27 Apr 2022 23:57:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552a264c301149b708c960de561d2ca60b943b1e7df73a3014c167af15c92ca1`  
		Last Modified: Wed, 27 Apr 2022 23:56:59 GMT  
		Size: 857.1 KB (857150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95db80d1282c166ea52579f1c1a5c467c3195b80898aa81d1e806ad18c4a5`  
		Last Modified: Wed, 27 Apr 2022 23:56:59 GMT  
		Size: 4.4 MB (4362174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826e5a82cd06b8cb8be57cec1870596edc933bd07e12e5ed0769b52651c6bf1c`  
		Last Modified: Wed, 27 Apr 2022 23:56:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f17650b58990a80a10cb6453dd26998bcbd2331820496489507d8fea1c65185`  
		Last Modified: Wed, 27 Apr 2022 23:56:56 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b055e0a6767051016c6b21f2d75bef706677e4cdbe373bda1a1a90875c94ebc5`  
		Last Modified: Wed, 27 Apr 2022 23:57:04 GMT  
		Size: 53.3 MB (53312707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a1c5bb850a1433e133ff4ad2f03aba0760bcaec777b89f966277fcc1d5e853`  
		Last Modified: Wed, 27 Apr 2022 23:56:56 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d95cfc30862e4a18f2816e950616909e7bf68418225712824bdc082de20feaf`  
		Last Modified: Wed, 27 Apr 2022 23:57:04 GMT  
		Size: 42.2 MB (42240171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbbeea923ab3e76c4bde4b1193e85df4ba6b2d26811eb1e04001e8691b23fc1`  
		Last Modified: Wed, 27 Apr 2022 23:56:56 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
