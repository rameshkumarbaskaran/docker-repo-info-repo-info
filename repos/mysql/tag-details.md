<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.44`](#mysql5744)
-	[`mysql:5.7.44-oracle`](#mysql5744-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.35`](#mysql8035)
-	[`mysql:8.0.35-debian`](#mysql8035-debian)
-	[`mysql:8.0.35-oracle`](#mysql8035-oracle)
-	[`mysql:8.2`](#mysql82)
-	[`mysql:8.2-oracle`](#mysql82-oracle)
-	[`mysql:8.2.0`](#mysql820)
-	[`mysql:8.2.0-oracle`](#mysql820-oracle)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:880063e8acda81825f0b946eff47c45235840480da03e71a22113ebafe166a3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:444e015ba2ad9fc0884a82cef6c3b15f89db003aef11b55e4daca24f55538cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137893279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547b3c3c15a9698ee368530b251e6baa66807c64742355e6724ba59b4d3ec8a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 12 Oct 2023 21:29:07 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 12 Oct 2023 21:29:07 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_VERSION=5.7.44-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:15:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:15:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:15:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a280ac4a8665e7273bf6a25ab20eac0aca50dc4e7e4183ffb2055a545d827175`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4047a3b08336709b0266a333c3a886acaffaa4e3219665bf4d91f608368eafe7`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 983.5 KB (983550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435611dd49992fa2e5d724c98b5e37dc08f821a562a3788b788ef771237199f5`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 4.6 MB (4581821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f2572cb0bb86444ec19bda78b738291b540fc4e924271ad3c3c2e23d93bcf`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef893e58839b0210e7a98dab9ba89d600956ab1df1b4ec6f6fbe2f11e5a5bc3a`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42897f5317839984e5ca7d5b1caea1821057f228e8b82fd4e1e23f3f4a07f550`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 25.5 MB (25525680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8aad27e96b3493812be9a72f2bb9ee46424babb2472f5a9115ddb92c8d0da4`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2751f26202485d0d09fd56bc88226d8fb44c73b8269e086e3f82f2a4c5e9cb`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 56.3 MB (56295470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e9b86ed64c8df8320596d475d3bbc4927e1e8bdc9ea97473c7e38024ae9c82`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfef93045c96cfc909e0b6b4d373e5cb88f5a1c92c22754bf1a353220e24f02c`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5` - unknown; unknown

```console
$ docker pull mysql@sha256:d204f87012383a2ae95d838c5890d72d49a4a0ada20ca71eccfac15d62115ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc2a31436e149eabe8b413783a8702be0009e737b9cc969d0bea6c170f6e9b`

```dockerfile
```

-	Layers:
	-	`sha256:5c62b3dd50222a07b620ab6db4bfdf0fcbf0058222eb67b38357d9d6cc3b3532`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99295500a19ce47fa801a84949ba1fc3836ca4c110ad48602e949ddaae63dbfd`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:880063e8acda81825f0b946eff47c45235840480da03e71a22113ebafe166a3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:444e015ba2ad9fc0884a82cef6c3b15f89db003aef11b55e4daca24f55538cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137893279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547b3c3c15a9698ee368530b251e6baa66807c64742355e6724ba59b4d3ec8a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 12 Oct 2023 21:29:07 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 12 Oct 2023 21:29:07 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_VERSION=5.7.44-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:15:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:15:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:15:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a280ac4a8665e7273bf6a25ab20eac0aca50dc4e7e4183ffb2055a545d827175`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4047a3b08336709b0266a333c3a886acaffaa4e3219665bf4d91f608368eafe7`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 983.5 KB (983550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435611dd49992fa2e5d724c98b5e37dc08f821a562a3788b788ef771237199f5`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 4.6 MB (4581821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f2572cb0bb86444ec19bda78b738291b540fc4e924271ad3c3c2e23d93bcf`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef893e58839b0210e7a98dab9ba89d600956ab1df1b4ec6f6fbe2f11e5a5bc3a`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42897f5317839984e5ca7d5b1caea1821057f228e8b82fd4e1e23f3f4a07f550`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 25.5 MB (25525680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8aad27e96b3493812be9a72f2bb9ee46424babb2472f5a9115ddb92c8d0da4`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2751f26202485d0d09fd56bc88226d8fb44c73b8269e086e3f82f2a4c5e9cb`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 56.3 MB (56295470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e9b86ed64c8df8320596d475d3bbc4927e1e8bdc9ea97473c7e38024ae9c82`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfef93045c96cfc909e0b6b4d373e5cb88f5a1c92c22754bf1a353220e24f02c`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d204f87012383a2ae95d838c5890d72d49a4a0ada20ca71eccfac15d62115ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc2a31436e149eabe8b413783a8702be0009e737b9cc969d0bea6c170f6e9b`

```dockerfile
```

-	Layers:
	-	`sha256:5c62b3dd50222a07b620ab6db4bfdf0fcbf0058222eb67b38357d9d6cc3b3532`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99295500a19ce47fa801a84949ba1fc3836ca4c110ad48602e949ddaae63dbfd`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7`

```console
$ docker pull mysql@sha256:880063e8acda81825f0b946eff47c45235840480da03e71a22113ebafe166a3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:444e015ba2ad9fc0884a82cef6c3b15f89db003aef11b55e4daca24f55538cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137893279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547b3c3c15a9698ee368530b251e6baa66807c64742355e6724ba59b4d3ec8a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 12 Oct 2023 21:29:07 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 12 Oct 2023 21:29:07 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_VERSION=5.7.44-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:15:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:15:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:15:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a280ac4a8665e7273bf6a25ab20eac0aca50dc4e7e4183ffb2055a545d827175`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4047a3b08336709b0266a333c3a886acaffaa4e3219665bf4d91f608368eafe7`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 983.5 KB (983550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435611dd49992fa2e5d724c98b5e37dc08f821a562a3788b788ef771237199f5`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 4.6 MB (4581821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f2572cb0bb86444ec19bda78b738291b540fc4e924271ad3c3c2e23d93bcf`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef893e58839b0210e7a98dab9ba89d600956ab1df1b4ec6f6fbe2f11e5a5bc3a`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42897f5317839984e5ca7d5b1caea1821057f228e8b82fd4e1e23f3f4a07f550`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 25.5 MB (25525680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8aad27e96b3493812be9a72f2bb9ee46424babb2472f5a9115ddb92c8d0da4`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2751f26202485d0d09fd56bc88226d8fb44c73b8269e086e3f82f2a4c5e9cb`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 56.3 MB (56295470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e9b86ed64c8df8320596d475d3bbc4927e1e8bdc9ea97473c7e38024ae9c82`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfef93045c96cfc909e0b6b4d373e5cb88f5a1c92c22754bf1a353220e24f02c`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7` - unknown; unknown

```console
$ docker pull mysql@sha256:d204f87012383a2ae95d838c5890d72d49a4a0ada20ca71eccfac15d62115ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc2a31436e149eabe8b413783a8702be0009e737b9cc969d0bea6c170f6e9b`

```dockerfile
```

-	Layers:
	-	`sha256:5c62b3dd50222a07b620ab6db4bfdf0fcbf0058222eb67b38357d9d6cc3b3532`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99295500a19ce47fa801a84949ba1fc3836ca4c110ad48602e949ddaae63dbfd`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:880063e8acda81825f0b946eff47c45235840480da03e71a22113ebafe166a3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:444e015ba2ad9fc0884a82cef6c3b15f89db003aef11b55e4daca24f55538cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137893279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547b3c3c15a9698ee368530b251e6baa66807c64742355e6724ba59b4d3ec8a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 12 Oct 2023 21:29:07 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 12 Oct 2023 21:29:07 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_VERSION=5.7.44-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:15:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:15:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:15:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a280ac4a8665e7273bf6a25ab20eac0aca50dc4e7e4183ffb2055a545d827175`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4047a3b08336709b0266a333c3a886acaffaa4e3219665bf4d91f608368eafe7`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 983.5 KB (983550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435611dd49992fa2e5d724c98b5e37dc08f821a562a3788b788ef771237199f5`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 4.6 MB (4581821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f2572cb0bb86444ec19bda78b738291b540fc4e924271ad3c3c2e23d93bcf`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef893e58839b0210e7a98dab9ba89d600956ab1df1b4ec6f6fbe2f11e5a5bc3a`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42897f5317839984e5ca7d5b1caea1821057f228e8b82fd4e1e23f3f4a07f550`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 25.5 MB (25525680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8aad27e96b3493812be9a72f2bb9ee46424babb2472f5a9115ddb92c8d0da4`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2751f26202485d0d09fd56bc88226d8fb44c73b8269e086e3f82f2a4c5e9cb`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 56.3 MB (56295470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e9b86ed64c8df8320596d475d3bbc4927e1e8bdc9ea97473c7e38024ae9c82`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfef93045c96cfc909e0b6b4d373e5cb88f5a1c92c22754bf1a353220e24f02c`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d204f87012383a2ae95d838c5890d72d49a4a0ada20ca71eccfac15d62115ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc2a31436e149eabe8b413783a8702be0009e737b9cc969d0bea6c170f6e9b`

```dockerfile
```

-	Layers:
	-	`sha256:5c62b3dd50222a07b620ab6db4bfdf0fcbf0058222eb67b38357d9d6cc3b3532`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99295500a19ce47fa801a84949ba1fc3836ca4c110ad48602e949ddaae63dbfd`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7.44`

```console
$ docker pull mysql@sha256:880063e8acda81825f0b946eff47c45235840480da03e71a22113ebafe166a3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7.44` - linux; amd64

```console
$ docker pull mysql@sha256:444e015ba2ad9fc0884a82cef6c3b15f89db003aef11b55e4daca24f55538cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137893279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547b3c3c15a9698ee368530b251e6baa66807c64742355e6724ba59b4d3ec8a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 12 Oct 2023 21:29:07 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 12 Oct 2023 21:29:07 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_VERSION=5.7.44-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:15:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:15:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:15:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a280ac4a8665e7273bf6a25ab20eac0aca50dc4e7e4183ffb2055a545d827175`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4047a3b08336709b0266a333c3a886acaffaa4e3219665bf4d91f608368eafe7`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 983.5 KB (983550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435611dd49992fa2e5d724c98b5e37dc08f821a562a3788b788ef771237199f5`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 4.6 MB (4581821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f2572cb0bb86444ec19bda78b738291b540fc4e924271ad3c3c2e23d93bcf`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef893e58839b0210e7a98dab9ba89d600956ab1df1b4ec6f6fbe2f11e5a5bc3a`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42897f5317839984e5ca7d5b1caea1821057f228e8b82fd4e1e23f3f4a07f550`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 25.5 MB (25525680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8aad27e96b3493812be9a72f2bb9ee46424babb2472f5a9115ddb92c8d0da4`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2751f26202485d0d09fd56bc88226d8fb44c73b8269e086e3f82f2a4c5e9cb`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 56.3 MB (56295470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e9b86ed64c8df8320596d475d3bbc4927e1e8bdc9ea97473c7e38024ae9c82`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfef93045c96cfc909e0b6b4d373e5cb88f5a1c92c22754bf1a353220e24f02c`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7.44` - unknown; unknown

```console
$ docker pull mysql@sha256:d204f87012383a2ae95d838c5890d72d49a4a0ada20ca71eccfac15d62115ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc2a31436e149eabe8b413783a8702be0009e737b9cc969d0bea6c170f6e9b`

```dockerfile
```

-	Layers:
	-	`sha256:5c62b3dd50222a07b620ab6db4bfdf0fcbf0058222eb67b38357d9d6cc3b3532`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99295500a19ce47fa801a84949ba1fc3836ca4c110ad48602e949ddaae63dbfd`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7.44-oracle`

```console
$ docker pull mysql@sha256:880063e8acda81825f0b946eff47c45235840480da03e71a22113ebafe166a3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7.44-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:444e015ba2ad9fc0884a82cef6c3b15f89db003aef11b55e4daca24f55538cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137893279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547b3c3c15a9698ee368530b251e6baa66807c64742355e6724ba59b4d3ec8a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 12 Oct 2023 21:29:07 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 12 Oct 2023 21:29:07 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_VERSION=5.7.44-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el7
# Tue, 24 Oct 2023 16:15:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:15:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:15:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:15:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:15:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a280ac4a8665e7273bf6a25ab20eac0aca50dc4e7e4183ffb2055a545d827175`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4047a3b08336709b0266a333c3a886acaffaa4e3219665bf4d91f608368eafe7`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 983.5 KB (983550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435611dd49992fa2e5d724c98b5e37dc08f821a562a3788b788ef771237199f5`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 4.6 MB (4581821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f2572cb0bb86444ec19bda78b738291b540fc4e924271ad3c3c2e23d93bcf`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef893e58839b0210e7a98dab9ba89d600956ab1df1b4ec6f6fbe2f11e5a5bc3a`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42897f5317839984e5ca7d5b1caea1821057f228e8b82fd4e1e23f3f4a07f550`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 25.5 MB (25525680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8aad27e96b3493812be9a72f2bb9ee46424babb2472f5a9115ddb92c8d0da4`  
		Last Modified: Fri, 27 Oct 2023 16:52:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2751f26202485d0d09fd56bc88226d8fb44c73b8269e086e3f82f2a4c5e9cb`  
		Last Modified: Fri, 27 Oct 2023 16:52:17 GMT  
		Size: 56.3 MB (56295470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e9b86ed64c8df8320596d475d3bbc4927e1e8bdc9ea97473c7e38024ae9c82`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfef93045c96cfc909e0b6b4d373e5cb88f5a1c92c22754bf1a353220e24f02c`  
		Last Modified: Fri, 27 Oct 2023 16:52:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d204f87012383a2ae95d838c5890d72d49a4a0ada20ca71eccfac15d62115ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc2a31436e149eabe8b413783a8702be0009e737b9cc969d0bea6c170f6e9b`

```dockerfile
```

-	Layers:
	-	`sha256:5c62b3dd50222a07b620ab6db4bfdf0fcbf0058222eb67b38357d9d6cc3b3532`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99295500a19ce47fa801a84949ba1fc3836ca4c110ad48602e949ddaae63dbfd`  
		Last Modified: Fri, 27 Oct 2023 16:52:14 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:974cac08fff819ea2dfeb83fed4d2eb5100bb79603aff6148bdc53d8be4895f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:fb3bd1a95fb7031940038d16b178be03c92f26e186bbeb69943b8a852746d392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166783886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bc8cf3633b279f56f393b3571f9c37f0a396285f40219a346c25ef407bb1db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6bf6e5d0f797f0dbde0ed09ebf2fd39c612b1a7345af4ed0b0efd6d0a97c6`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b83f8620f94c7b15448608b5ca82b804681e39d4e1eccdf3dddcbb53c28c1`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e259cd9b6cbe4bb0e1e250f29133131d12f7f98520a8b152502bf107b2de41`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 4.6 MB (4613942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366131ab00d155ed24098b5da1719901f2a1200a53541653104aa8ee5b20f7ab`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99ba83a3cb97ee64f4c873f0740c3e35eeaf088bbb4768787a382da039b95e`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c88955f01f18423e680ca4210745b75119aef91cc7f39f5136c90e9f22213d`  
		Last Modified: Fri, 27 Oct 2023 16:52:36 GMT  
		Size: 58.5 MB (58512865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577fb415d7f8d85525c41132971e40fd7b193d94c8a6ce72a2645434a22f911e`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29160ed46eb125ec317fe3140877887fc5fe46c1f1828beb5890e60361700570`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 58.4 MB (58385001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce9884ce5da8f3cb92f929eb488a7e4f67f9640196a4e18df0cc4ee8ea0b00`  
		Last Modified: Fri, 27 Oct 2023 16:52:33 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f0dceb14ce64e78616fdd2397a5e13361fc449b5dc542a1cb95404ff28179`  
		Last Modified: Fri, 27 Oct 2023 16:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:192ac1fe700f86b7db7147c740f05dc3970a10b9d55cee2c589c5e6410d0246d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c0f77bea9bf58b43eec0cdd8c674c0b7ec3b3de8922b79e3932468ad1d936a`

```dockerfile
```

-	Layers:
	-	`sha256:e522da18f974179cac95b261d4b597aac3378e03097d3cc7d049e08e19d7afe6`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 11.6 MB (11571249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a542b80af92e60a4df2008cc1ed93c6e7aed929581fc60ee4503f5f5b620280a`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:536dbedd801cb178559a7ba1636ff431a9308b296f4940d32802410639d1e799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171129249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77db3b0e88f00b6d34e4f5a3d0531aaa46edf57b0b9186ac2a394395787eb98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa7b76489a7fec7031401bb2b6029c270f41a77fa3a2be76dff839387ad8924`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ec9441db74d4410413cf0a5ed9d714a3733fa28379ceb7b3298b1a7b5f6eb7`  
		Last Modified: Fri, 27 Oct 2023 17:35:31 GMT  
		Size: 57.6 MB (57569300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762cfba29069980c8a6a63471767be52f7b398b124fa7538cc511caacc1534c3`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee3de57ddb2a23a5bde678f2c7d93026a97a1e819c6b3a6b98ae3ef9d3ff45e`  
		Last Modified: Fri, 27 Oct 2023 17:35:32 GMT  
		Size: 64.7 MB (64662393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977481c71c9bbb791068306e4d97d6ef27c4fefa0503b86321408a3938d63af1`  
		Last Modified: Fri, 27 Oct 2023 17:35:30 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777eb7fbf1d555215c2c89eb269c4a541db26bb9e7a10d8138118e5504240233`  
		Last Modified: Fri, 27 Oct 2023 17:35:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2909f8a487cc780f39e4a4c10dfd615053302a3c99643e450c776151c7f3284d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1125c446107ef60867c1987db7a7f2f9e20bf4a15a61f28141399df820fe0164`

```dockerfile
```

-	Layers:
	-	`sha256:a931a4b3072de1209acc4c0ca7e32f7a3322b65928f7cefbdcf287760bacc6cd`  
		Last Modified: Fri, 27 Oct 2023 17:35:29 GMT  
		Size: 11.6 MB (11569825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2939df9d11998be55cac802fd38133b1a97af0c408afe0483024bf8eeedf97d4`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:85f062e0d2b7e168d9de067961ed95a13c7df9a37ebde33c329d843f9dd8f9db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:da63be223d545b454b7c5b73d089878581092fd6911de7c9ca927ad5ff1734d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179123412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4696d3f37fae349df3a2e1f200333609d8d2c2de9b5da8ff1f189446137fce9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1debian11
# Tue, 24 Oct 2023 16:18:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81174744baa5836fd58e8b6d195fec5e3446b1123fb5b6d2ea8fd18c34b58635`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf9084d182c6777f2678b63ce7130d17473f4a2dc888df6bd01fae40820fead`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 4.2 MB (4207463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4121e535f9d557df9569dd9e33d2b4eba249c4ac7425e0bc0b75fd7f62e902cb`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 1.5 MB (1472458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6ac1683e69ff3c5f13579336e877e208b61ff62bef725eb146fa6f3b2d7499`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec803dff8a9708e3ca23a829daece394687b089cdd20c6572fef7dfb158cf9b7`  
		Last Modified: Fri, 27 Oct 2023 16:51:40 GMT  
		Size: 12.5 MB (12455064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ab247fb8f9ff1019aa5f59825f00bb75595d722635a24f8a168a1be3a4d750`  
		Last Modified: Fri, 27 Oct 2023 16:51:39 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4899e5e40ae8c4e616e94254af25fbdfb5daf76fc400c3b72c9d17dc59a20a`  
		Last Modified: Fri, 27 Oct 2023 16:51:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce40117f3c61d48df4e891580df1547719f19051bcd03095e3ad5ec0bfce339`  
		Last Modified: Fri, 27 Oct 2023 16:51:47 GMT  
		Size: 129.6 MB (129559712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177c7e0f59387fe1272411352b3543ccd466376d71703857f469609f4a3073a7`  
		Last Modified: Fri, 27 Oct 2023 16:51:41 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bd8c4f25a944a7152fe09e0e40eb95c8e48a2d754fccb197a36ebd717aabc`  
		Last Modified: Fri, 27 Oct 2023 16:51:41 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203273a5e095383700cf5cf6ae5a5bc51f0b0ddc057b69cd81f13384b2e8d209`  
		Last Modified: Fri, 27 Oct 2023 16:51:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:8c9dc9af8579af0bb9ab921dd4c4ec6fc0515d70ffbf0d1bb85729eda5878c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e5f1b9e054ba2884f447a09d4c79d009b65df5375b12238d50d76ed090c9d1`

```dockerfile
```

-	Layers:
	-	`sha256:eb3beae59fb045bae14a759b85c2d0797074202060db1542ff87a3351b74f463`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 3.6 MB (3551726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8772ef63d4c93adaeb669d1160b8fd12fbdd5d1ad642d0551a7628d8d399cd`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 33.3 KB (33289 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:974cac08fff819ea2dfeb83fed4d2eb5100bb79603aff6148bdc53d8be4895f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fb3bd1a95fb7031940038d16b178be03c92f26e186bbeb69943b8a852746d392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166783886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bc8cf3633b279f56f393b3571f9c37f0a396285f40219a346c25ef407bb1db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6bf6e5d0f797f0dbde0ed09ebf2fd39c612b1a7345af4ed0b0efd6d0a97c6`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b83f8620f94c7b15448608b5ca82b804681e39d4e1eccdf3dddcbb53c28c1`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e259cd9b6cbe4bb0e1e250f29133131d12f7f98520a8b152502bf107b2de41`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 4.6 MB (4613942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366131ab00d155ed24098b5da1719901f2a1200a53541653104aa8ee5b20f7ab`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99ba83a3cb97ee64f4c873f0740c3e35eeaf088bbb4768787a382da039b95e`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c88955f01f18423e680ca4210745b75119aef91cc7f39f5136c90e9f22213d`  
		Last Modified: Fri, 27 Oct 2023 16:52:36 GMT  
		Size: 58.5 MB (58512865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577fb415d7f8d85525c41132971e40fd7b193d94c8a6ce72a2645434a22f911e`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29160ed46eb125ec317fe3140877887fc5fe46c1f1828beb5890e60361700570`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 58.4 MB (58385001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce9884ce5da8f3cb92f929eb488a7e4f67f9640196a4e18df0cc4ee8ea0b00`  
		Last Modified: Fri, 27 Oct 2023 16:52:33 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f0dceb14ce64e78616fdd2397a5e13361fc449b5dc542a1cb95404ff28179`  
		Last Modified: Fri, 27 Oct 2023 16:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:192ac1fe700f86b7db7147c740f05dc3970a10b9d55cee2c589c5e6410d0246d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c0f77bea9bf58b43eec0cdd8c674c0b7ec3b3de8922b79e3932468ad1d936a`

```dockerfile
```

-	Layers:
	-	`sha256:e522da18f974179cac95b261d4b597aac3378e03097d3cc7d049e08e19d7afe6`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 11.6 MB (11571249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a542b80af92e60a4df2008cc1ed93c6e7aed929581fc60ee4503f5f5b620280a`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:536dbedd801cb178559a7ba1636ff431a9308b296f4940d32802410639d1e799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171129249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77db3b0e88f00b6d34e4f5a3d0531aaa46edf57b0b9186ac2a394395787eb98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa7b76489a7fec7031401bb2b6029c270f41a77fa3a2be76dff839387ad8924`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ec9441db74d4410413cf0a5ed9d714a3733fa28379ceb7b3298b1a7b5f6eb7`  
		Last Modified: Fri, 27 Oct 2023 17:35:31 GMT  
		Size: 57.6 MB (57569300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762cfba29069980c8a6a63471767be52f7b398b124fa7538cc511caacc1534c3`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee3de57ddb2a23a5bde678f2c7d93026a97a1e819c6b3a6b98ae3ef9d3ff45e`  
		Last Modified: Fri, 27 Oct 2023 17:35:32 GMT  
		Size: 64.7 MB (64662393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977481c71c9bbb791068306e4d97d6ef27c4fefa0503b86321408a3938d63af1`  
		Last Modified: Fri, 27 Oct 2023 17:35:30 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777eb7fbf1d555215c2c89eb269c4a541db26bb9e7a10d8138118e5504240233`  
		Last Modified: Fri, 27 Oct 2023 17:35:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2909f8a487cc780f39e4a4c10dfd615053302a3c99643e450c776151c7f3284d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1125c446107ef60867c1987db7a7f2f9e20bf4a15a61f28141399df820fe0164`

```dockerfile
```

-	Layers:
	-	`sha256:a931a4b3072de1209acc4c0ca7e32f7a3322b65928f7cefbdcf287760bacc6cd`  
		Last Modified: Fri, 27 Oct 2023 17:35:29 GMT  
		Size: 11.6 MB (11569825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2939df9d11998be55cac802fd38133b1a97af0c408afe0483024bf8eeedf97d4`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35`

```console
$ docker pull mysql@sha256:974cac08fff819ea2dfeb83fed4d2eb5100bb79603aff6148bdc53d8be4895f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35` - linux; amd64

```console
$ docker pull mysql@sha256:fb3bd1a95fb7031940038d16b178be03c92f26e186bbeb69943b8a852746d392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166783886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bc8cf3633b279f56f393b3571f9c37f0a396285f40219a346c25ef407bb1db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6bf6e5d0f797f0dbde0ed09ebf2fd39c612b1a7345af4ed0b0efd6d0a97c6`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b83f8620f94c7b15448608b5ca82b804681e39d4e1eccdf3dddcbb53c28c1`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e259cd9b6cbe4bb0e1e250f29133131d12f7f98520a8b152502bf107b2de41`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 4.6 MB (4613942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366131ab00d155ed24098b5da1719901f2a1200a53541653104aa8ee5b20f7ab`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99ba83a3cb97ee64f4c873f0740c3e35eeaf088bbb4768787a382da039b95e`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c88955f01f18423e680ca4210745b75119aef91cc7f39f5136c90e9f22213d`  
		Last Modified: Fri, 27 Oct 2023 16:52:36 GMT  
		Size: 58.5 MB (58512865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577fb415d7f8d85525c41132971e40fd7b193d94c8a6ce72a2645434a22f911e`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29160ed46eb125ec317fe3140877887fc5fe46c1f1828beb5890e60361700570`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 58.4 MB (58385001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce9884ce5da8f3cb92f929eb488a7e4f67f9640196a4e18df0cc4ee8ea0b00`  
		Last Modified: Fri, 27 Oct 2023 16:52:33 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f0dceb14ce64e78616fdd2397a5e13361fc449b5dc542a1cb95404ff28179`  
		Last Modified: Fri, 27 Oct 2023 16:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35` - unknown; unknown

```console
$ docker pull mysql@sha256:192ac1fe700f86b7db7147c740f05dc3970a10b9d55cee2c589c5e6410d0246d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c0f77bea9bf58b43eec0cdd8c674c0b7ec3b3de8922b79e3932468ad1d936a`

```dockerfile
```

-	Layers:
	-	`sha256:e522da18f974179cac95b261d4b597aac3378e03097d3cc7d049e08e19d7afe6`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 11.6 MB (11571249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a542b80af92e60a4df2008cc1ed93c6e7aed929581fc60ee4503f5f5b620280a`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:536dbedd801cb178559a7ba1636ff431a9308b296f4940d32802410639d1e799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171129249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77db3b0e88f00b6d34e4f5a3d0531aaa46edf57b0b9186ac2a394395787eb98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa7b76489a7fec7031401bb2b6029c270f41a77fa3a2be76dff839387ad8924`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ec9441db74d4410413cf0a5ed9d714a3733fa28379ceb7b3298b1a7b5f6eb7`  
		Last Modified: Fri, 27 Oct 2023 17:35:31 GMT  
		Size: 57.6 MB (57569300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762cfba29069980c8a6a63471767be52f7b398b124fa7538cc511caacc1534c3`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee3de57ddb2a23a5bde678f2c7d93026a97a1e819c6b3a6b98ae3ef9d3ff45e`  
		Last Modified: Fri, 27 Oct 2023 17:35:32 GMT  
		Size: 64.7 MB (64662393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977481c71c9bbb791068306e4d97d6ef27c4fefa0503b86321408a3938d63af1`  
		Last Modified: Fri, 27 Oct 2023 17:35:30 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777eb7fbf1d555215c2c89eb269c4a541db26bb9e7a10d8138118e5504240233`  
		Last Modified: Fri, 27 Oct 2023 17:35:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35` - unknown; unknown

```console
$ docker pull mysql@sha256:2909f8a487cc780f39e4a4c10dfd615053302a3c99643e450c776151c7f3284d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1125c446107ef60867c1987db7a7f2f9e20bf4a15a61f28141399df820fe0164`

```dockerfile
```

-	Layers:
	-	`sha256:a931a4b3072de1209acc4c0ca7e32f7a3322b65928f7cefbdcf287760bacc6cd`  
		Last Modified: Fri, 27 Oct 2023 17:35:29 GMT  
		Size: 11.6 MB (11569825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2939df9d11998be55cac802fd38133b1a97af0c408afe0483024bf8eeedf97d4`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-debian`

```console
$ docker pull mysql@sha256:85f062e0d2b7e168d9de067961ed95a13c7df9a37ebde33c329d843f9dd8f9db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.35-debian` - linux; amd64

```console
$ docker pull mysql@sha256:da63be223d545b454b7c5b73d089878581092fd6911de7c9ca927ad5ff1734d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179123412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4696d3f37fae349df3a2e1f200333609d8d2c2de9b5da8ff1f189446137fce9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1debian11
# Tue, 24 Oct 2023 16:18:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81174744baa5836fd58e8b6d195fec5e3446b1123fb5b6d2ea8fd18c34b58635`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf9084d182c6777f2678b63ce7130d17473f4a2dc888df6bd01fae40820fead`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 4.2 MB (4207463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4121e535f9d557df9569dd9e33d2b4eba249c4ac7425e0bc0b75fd7f62e902cb`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 1.5 MB (1472458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6ac1683e69ff3c5f13579336e877e208b61ff62bef725eb146fa6f3b2d7499`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec803dff8a9708e3ca23a829daece394687b089cdd20c6572fef7dfb158cf9b7`  
		Last Modified: Fri, 27 Oct 2023 16:51:40 GMT  
		Size: 12.5 MB (12455064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ab247fb8f9ff1019aa5f59825f00bb75595d722635a24f8a168a1be3a4d750`  
		Last Modified: Fri, 27 Oct 2023 16:51:39 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4899e5e40ae8c4e616e94254af25fbdfb5daf76fc400c3b72c9d17dc59a20a`  
		Last Modified: Fri, 27 Oct 2023 16:51:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce40117f3c61d48df4e891580df1547719f19051bcd03095e3ad5ec0bfce339`  
		Last Modified: Fri, 27 Oct 2023 16:51:47 GMT  
		Size: 129.6 MB (129559712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177c7e0f59387fe1272411352b3543ccd466376d71703857f469609f4a3073a7`  
		Last Modified: Fri, 27 Oct 2023 16:51:41 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bd8c4f25a944a7152fe09e0e40eb95c8e48a2d754fccb197a36ebd717aabc`  
		Last Modified: Fri, 27 Oct 2023 16:51:41 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203273a5e095383700cf5cf6ae5a5bc51f0b0ddc057b69cd81f13384b2e8d209`  
		Last Modified: Fri, 27 Oct 2023 16:51:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:8c9dc9af8579af0bb9ab921dd4c4ec6fc0515d70ffbf0d1bb85729eda5878c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e5f1b9e054ba2884f447a09d4c79d009b65df5375b12238d50d76ed090c9d1`

```dockerfile
```

-	Layers:
	-	`sha256:eb3beae59fb045bae14a759b85c2d0797074202060db1542ff87a3351b74f463`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 3.6 MB (3551726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8772ef63d4c93adaeb669d1160b8fd12fbdd5d1ad642d0551a7628d8d399cd`  
		Last Modified: Fri, 27 Oct 2023 16:51:38 GMT  
		Size: 33.3 KB (33289 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-oracle`

```console
$ docker pull mysql@sha256:974cac08fff819ea2dfeb83fed4d2eb5100bb79603aff6148bdc53d8be4895f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fb3bd1a95fb7031940038d16b178be03c92f26e186bbeb69943b8a852746d392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166783886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bc8cf3633b279f56f393b3571f9c37f0a396285f40219a346c25ef407bb1db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6bf6e5d0f797f0dbde0ed09ebf2fd39c612b1a7345af4ed0b0efd6d0a97c6`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b83f8620f94c7b15448608b5ca82b804681e39d4e1eccdf3dddcbb53c28c1`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e259cd9b6cbe4bb0e1e250f29133131d12f7f98520a8b152502bf107b2de41`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 4.6 MB (4613942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366131ab00d155ed24098b5da1719901f2a1200a53541653104aa8ee5b20f7ab`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99ba83a3cb97ee64f4c873f0740c3e35eeaf088bbb4768787a382da039b95e`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c88955f01f18423e680ca4210745b75119aef91cc7f39f5136c90e9f22213d`  
		Last Modified: Fri, 27 Oct 2023 16:52:36 GMT  
		Size: 58.5 MB (58512865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577fb415d7f8d85525c41132971e40fd7b193d94c8a6ce72a2645434a22f911e`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29160ed46eb125ec317fe3140877887fc5fe46c1f1828beb5890e60361700570`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 58.4 MB (58385001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce9884ce5da8f3cb92f929eb488a7e4f67f9640196a4e18df0cc4ee8ea0b00`  
		Last Modified: Fri, 27 Oct 2023 16:52:33 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f0dceb14ce64e78616fdd2397a5e13361fc449b5dc542a1cb95404ff28179`  
		Last Modified: Fri, 27 Oct 2023 16:52:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:192ac1fe700f86b7db7147c740f05dc3970a10b9d55cee2c589c5e6410d0246d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c0f77bea9bf58b43eec0cdd8c674c0b7ec3b3de8922b79e3932468ad1d936a`

```dockerfile
```

-	Layers:
	-	`sha256:e522da18f974179cac95b261d4b597aac3378e03097d3cc7d049e08e19d7afe6`  
		Last Modified: Fri, 27 Oct 2023 16:52:32 GMT  
		Size: 11.6 MB (11571249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a542b80af92e60a4df2008cc1ed93c6e7aed929581fc60ee4503f5f5b620280a`  
		Last Modified: Fri, 27 Oct 2023 16:52:31 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:536dbedd801cb178559a7ba1636ff431a9308b296f4940d32802410639d1e799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171129249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77db3b0e88f00b6d34e4f5a3d0531aaa46edf57b0b9186ac2a394395787eb98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:18:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:18:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Oct 2023 16:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:18:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:18:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa7b76489a7fec7031401bb2b6029c270f41a77fa3a2be76dff839387ad8924`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ec9441db74d4410413cf0a5ed9d714a3733fa28379ceb7b3298b1a7b5f6eb7`  
		Last Modified: Fri, 27 Oct 2023 17:35:31 GMT  
		Size: 57.6 MB (57569300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762cfba29069980c8a6a63471767be52f7b398b124fa7538cc511caacc1534c3`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee3de57ddb2a23a5bde678f2c7d93026a97a1e819c6b3a6b98ae3ef9d3ff45e`  
		Last Modified: Fri, 27 Oct 2023 17:35:32 GMT  
		Size: 64.7 MB (64662393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977481c71c9bbb791068306e4d97d6ef27c4fefa0503b86321408a3938d63af1`  
		Last Modified: Fri, 27 Oct 2023 17:35:30 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777eb7fbf1d555215c2c89eb269c4a541db26bb9e7a10d8138118e5504240233`  
		Last Modified: Fri, 27 Oct 2023 17:35:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2909f8a487cc780f39e4a4c10dfd615053302a3c99643e450c776151c7f3284d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1125c446107ef60867c1987db7a7f2f9e20bf4a15a61f28141399df820fe0164`

```dockerfile
```

-	Layers:
	-	`sha256:a931a4b3072de1209acc4c0ca7e32f7a3322b65928f7cefbdcf287760bacc6cd`  
		Last Modified: Fri, 27 Oct 2023 17:35:29 GMT  
		Size: 11.6 MB (11569825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2939df9d11998be55cac802fd38133b1a97af0c408afe0483024bf8eeedf97d4`  
		Last Modified: Fri, 27 Oct 2023 17:35:28 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2-oracle`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0-oracle`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:1773f3c7aa9522f0014d0ad2bbdaf597ea3b1643c64c8ccc2123c64afd8b82b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d43bab9d9bd18d3770f6156bdb7c5364cac797c6a906e67cf548b0a439ff1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b6608898d600759effd58768b7213bb44a6d58ab3a53495dd88e6b2042a8a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c52718f659575d985c333e7c7dba235ad525ee2247943aa8309e72adbf415`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d03ce139bba7985059e737fc0d92676d8de0b28dd29373cd73d51df5eb917`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 982.8 KB (982803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d7f11aa1ef914682fba80d61f12d92d33bcb330317c786159f87f2abe4457`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 4.6 MB (4613883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5949193e4c0a12884d6f5c8d1450655c294b7aa9953dba87f7827f584db3cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f024dfb3292ef1d74bddd001b32d497d0888cc631dc672d98cbbe05b722de4`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3c840facc99e1799423dcf8717c8135d4f85802a696e00603eaaf54555579`  
		Last Modified: Fri, 27 Oct 2023 16:52:44 GMT  
		Size: 62.6 MB (62585271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509068e4948821c9dee6cb69b3fdcc49b1700436cccce576a8db12e41821e40c`  
		Last Modified: Fri, 27 Oct 2023 16:52:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc847bab598e716df16e74538d8a7aa37c1d113414910946773f7052b5665cc`  
		Last Modified: Fri, 27 Oct 2023 16:52:43 GMT  
		Size: 58.4 MB (58389738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942bef62a146fe789efc9a325490033fe7c31e992f41674ef2dc5ba2dd16bb03`  
		Last Modified: Fri, 27 Oct 2023 16:52:40 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:049ee0faaab71a2ca3be523a8e5ec6049ce787fa753348094f6f10cf6e038cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11607325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a46233654b93da551fcb523f9b6fdbf711cac62dfc7abbc964b2856d811fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:cd34638f853651f4bbebe72893a2e064e623046f694a7f6bcbc4e185bcaecfa1`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 11.6 MB (11573746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0f27881910d49668ff79f1b17cdcb05030ee8e04bb66f9e9800c86a54e421`  
		Last Modified: Fri, 27 Oct 2023 16:52:38 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c1a182859289910f68f928bec0a2728238a7c4303421b663fe4bcbdf3b26e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175175472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fb452c483ffe15d4ec362a904fd285ab1f4dedd98b0a38060c87f1d98f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 24 Oct 2023 16:24:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Oct 2023 16:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 16:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 16:24:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Oct 2023 16:24:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7fadc33ecff9fcb4c6067c675ad7d14bb8b71f383f243e558ae552cf8da05`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d193449aafd2e76aefe49f553ee2d007ed850656e18916b74c5d28057e6cfb7`  
		Last Modified: Fri, 20 Oct 2023 20:38:15 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea497c74b15661c8dcda90c65a4d6878277fb00ba8ce6c4b71bab676b372c34`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 4.3 MB (4302158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778acbf55f327acde293ae0092a016ebf0324943d47aa131140a802397301d2`  
		Last Modified: Fri, 20 Oct 2023 20:38:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a633e58f96699b9353a7f8c519f9d539ddf019bf45b7cece8d069489ccd81ec3`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3047f9b4b2396b11f161cba3aa6cea21ffa0e785445a9dac59a1255f59858`  
		Last Modified: Fri, 27 Oct 2023 17:33:02 GMT  
		Size: 61.6 MB (61599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae0c334fe165d6e3360cdad3092278ae584ecac51145e7e35914b49af9fc62`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139fc79e81c59fd5f78bec666717625e67ef9fb035f32633d4d63d80faf34d2`  
		Last Modified: Fri, 27 Oct 2023 17:33:01 GMT  
		Size: 64.7 MB (64678146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956b492354cca5bff67029469043e2dbc692fb2fea70be223ac81319677cfa6`  
		Last Modified: Fri, 27 Oct 2023 17:32:59 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fcfd64c148b8d8710b49d9c262d7592c5eefedd5739f0b7e0db4de7c7c6ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11605768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ac1138f124abd5764cbc6f38f4c6407f6eadb4816f561c4d8d44b6ae8f4eb`

```dockerfile
```

-	Layers:
	-	`sha256:728052679d05a5b4011ca1034115db7db10de5c4bfca08997d6ecc0f244ed86f`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 11.6 MB (11572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1912d978be5f77a319be5da24760e346fb4b27b7c27f4a6ec0d123bbb664ab`  
		Last Modified: Fri, 27 Oct 2023 17:32:58 GMT  
		Size: 33.4 KB (33434 bytes)  
		MIME: application/vnd.in-toto+json
