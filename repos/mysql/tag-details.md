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
$ docker pull mysql@sha256:f566819f2eee3a60cf5ea6c8b7d1bfc9de62e34268bf62dc34870c4fca8a85d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:358b0482ced8103a8691c781e1cb6cd6b5a0b463a6dc0924a7ef357513ecc7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137898383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdba757bc9336a536d6884ecfaef00d24c1da3becd41e094eb226076436f258c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:15:11 GMT
ADD file:3e0277519395faaec643f0d6752812c14478974d1a914a763327a3cf30bbd28c in / 
# Tue, 24 Oct 2023 16:15:11 GMT
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
	-	`sha256:11a38aebcb7ae84df8b4fdcc1c7540389829a1f599b7a9986df89df733b69cea`  
		Last Modified: Tue, 14 Nov 2023 18:22:00 GMT  
		Size: 50.5 MB (50499111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ab01309bd664e500e70dbc3a6cd5a671ef725cc650bacddc6e3e3e0177c2e4`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c91fabb88c28533b95e5cd10d9612dcb5e0f8cba5b907e81b089af7b9bdcb43`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 983.6 KB (983553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46e806ab5c4d1750a22e436dd6a0843c79c2695dcb0c5515940957c94375cf`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 4.6 MB (4582768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f5af1d166141a7b944cac8f99e95fa74763b4b73bec000d949df541c26b9ee`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aca7179a542fdc7b3ab8cfecbe6b1d3e44f0bcabee6cad568d1c2d91c9ecc7`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85023e6de3be9d69a9eaf1473a15f89ce1ee93d622fe4922356006f4af79d9ba`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 25.5 MB (25526786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5934a87cbb3c1ca8617e6afb047b2f949631501df3b8cb129ebc370ff21dc0`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878502d3f701b4bc6d4a849b58572de800ddb974f9b1f7c4c2e9e708e272caf`  
		Last Modified: Tue, 14 Nov 2023 19:26:21 GMT  
		Size: 56.3 MB (56296062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4756467c684a5489662a946c2274be869f7c863eff60a74a320a48ce786ab7ae`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9043dd2677465a371dbe7baa21aed779113f00e232f54cdd8d79e0ee5fb9d7`  
		Last Modified: Tue, 14 Nov 2023 19:26:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5` - unknown; unknown

```console
$ docker pull mysql@sha256:c092eba3670b63959de4d8094b03631a0cd53c05df4885dc411df0952acea459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7f220fbd29051e5f5bab6b85659d9fab302e5f6994b7c36021ad000b988c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88c985dac4c30a6a3ade1edb495df0a1f088e8965205cf5414b8fe7452826cb8`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bdf23f574c4dda1e207d57beefa48dfea197a6bf17c750cde4a813a84583a`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:f566819f2eee3a60cf5ea6c8b7d1bfc9de62e34268bf62dc34870c4fca8a85d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:358b0482ced8103a8691c781e1cb6cd6b5a0b463a6dc0924a7ef357513ecc7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137898383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdba757bc9336a536d6884ecfaef00d24c1da3becd41e094eb226076436f258c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:15:11 GMT
ADD file:3e0277519395faaec643f0d6752812c14478974d1a914a763327a3cf30bbd28c in / 
# Tue, 24 Oct 2023 16:15:11 GMT
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
	-	`sha256:11a38aebcb7ae84df8b4fdcc1c7540389829a1f599b7a9986df89df733b69cea`  
		Last Modified: Tue, 14 Nov 2023 18:22:00 GMT  
		Size: 50.5 MB (50499111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ab01309bd664e500e70dbc3a6cd5a671ef725cc650bacddc6e3e3e0177c2e4`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c91fabb88c28533b95e5cd10d9612dcb5e0f8cba5b907e81b089af7b9bdcb43`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 983.6 KB (983553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46e806ab5c4d1750a22e436dd6a0843c79c2695dcb0c5515940957c94375cf`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 4.6 MB (4582768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f5af1d166141a7b944cac8f99e95fa74763b4b73bec000d949df541c26b9ee`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aca7179a542fdc7b3ab8cfecbe6b1d3e44f0bcabee6cad568d1c2d91c9ecc7`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85023e6de3be9d69a9eaf1473a15f89ce1ee93d622fe4922356006f4af79d9ba`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 25.5 MB (25526786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5934a87cbb3c1ca8617e6afb047b2f949631501df3b8cb129ebc370ff21dc0`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878502d3f701b4bc6d4a849b58572de800ddb974f9b1f7c4c2e9e708e272caf`  
		Last Modified: Tue, 14 Nov 2023 19:26:21 GMT  
		Size: 56.3 MB (56296062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4756467c684a5489662a946c2274be869f7c863eff60a74a320a48ce786ab7ae`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9043dd2677465a371dbe7baa21aed779113f00e232f54cdd8d79e0ee5fb9d7`  
		Last Modified: Tue, 14 Nov 2023 19:26:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c092eba3670b63959de4d8094b03631a0cd53c05df4885dc411df0952acea459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7f220fbd29051e5f5bab6b85659d9fab302e5f6994b7c36021ad000b988c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88c985dac4c30a6a3ade1edb495df0a1f088e8965205cf5414b8fe7452826cb8`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bdf23f574c4dda1e207d57beefa48dfea197a6bf17c750cde4a813a84583a`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7`

```console
$ docker pull mysql@sha256:f566819f2eee3a60cf5ea6c8b7d1bfc9de62e34268bf62dc34870c4fca8a85d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:358b0482ced8103a8691c781e1cb6cd6b5a0b463a6dc0924a7ef357513ecc7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137898383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdba757bc9336a536d6884ecfaef00d24c1da3becd41e094eb226076436f258c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:15:11 GMT
ADD file:3e0277519395faaec643f0d6752812c14478974d1a914a763327a3cf30bbd28c in / 
# Tue, 24 Oct 2023 16:15:11 GMT
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
	-	`sha256:11a38aebcb7ae84df8b4fdcc1c7540389829a1f599b7a9986df89df733b69cea`  
		Last Modified: Tue, 14 Nov 2023 18:22:00 GMT  
		Size: 50.5 MB (50499111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ab01309bd664e500e70dbc3a6cd5a671ef725cc650bacddc6e3e3e0177c2e4`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c91fabb88c28533b95e5cd10d9612dcb5e0f8cba5b907e81b089af7b9bdcb43`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 983.6 KB (983553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46e806ab5c4d1750a22e436dd6a0843c79c2695dcb0c5515940957c94375cf`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 4.6 MB (4582768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f5af1d166141a7b944cac8f99e95fa74763b4b73bec000d949df541c26b9ee`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aca7179a542fdc7b3ab8cfecbe6b1d3e44f0bcabee6cad568d1c2d91c9ecc7`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85023e6de3be9d69a9eaf1473a15f89ce1ee93d622fe4922356006f4af79d9ba`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 25.5 MB (25526786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5934a87cbb3c1ca8617e6afb047b2f949631501df3b8cb129ebc370ff21dc0`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878502d3f701b4bc6d4a849b58572de800ddb974f9b1f7c4c2e9e708e272caf`  
		Last Modified: Tue, 14 Nov 2023 19:26:21 GMT  
		Size: 56.3 MB (56296062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4756467c684a5489662a946c2274be869f7c863eff60a74a320a48ce786ab7ae`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9043dd2677465a371dbe7baa21aed779113f00e232f54cdd8d79e0ee5fb9d7`  
		Last Modified: Tue, 14 Nov 2023 19:26:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7` - unknown; unknown

```console
$ docker pull mysql@sha256:c092eba3670b63959de4d8094b03631a0cd53c05df4885dc411df0952acea459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7f220fbd29051e5f5bab6b85659d9fab302e5f6994b7c36021ad000b988c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88c985dac4c30a6a3ade1edb495df0a1f088e8965205cf5414b8fe7452826cb8`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bdf23f574c4dda1e207d57beefa48dfea197a6bf17c750cde4a813a84583a`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:f566819f2eee3a60cf5ea6c8b7d1bfc9de62e34268bf62dc34870c4fca8a85d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:358b0482ced8103a8691c781e1cb6cd6b5a0b463a6dc0924a7ef357513ecc7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137898383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdba757bc9336a536d6884ecfaef00d24c1da3becd41e094eb226076436f258c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:15:11 GMT
ADD file:3e0277519395faaec643f0d6752812c14478974d1a914a763327a3cf30bbd28c in / 
# Tue, 24 Oct 2023 16:15:11 GMT
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
	-	`sha256:11a38aebcb7ae84df8b4fdcc1c7540389829a1f599b7a9986df89df733b69cea`  
		Last Modified: Tue, 14 Nov 2023 18:22:00 GMT  
		Size: 50.5 MB (50499111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ab01309bd664e500e70dbc3a6cd5a671ef725cc650bacddc6e3e3e0177c2e4`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c91fabb88c28533b95e5cd10d9612dcb5e0f8cba5b907e81b089af7b9bdcb43`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 983.6 KB (983553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46e806ab5c4d1750a22e436dd6a0843c79c2695dcb0c5515940957c94375cf`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 4.6 MB (4582768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f5af1d166141a7b944cac8f99e95fa74763b4b73bec000d949df541c26b9ee`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aca7179a542fdc7b3ab8cfecbe6b1d3e44f0bcabee6cad568d1c2d91c9ecc7`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85023e6de3be9d69a9eaf1473a15f89ce1ee93d622fe4922356006f4af79d9ba`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 25.5 MB (25526786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5934a87cbb3c1ca8617e6afb047b2f949631501df3b8cb129ebc370ff21dc0`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878502d3f701b4bc6d4a849b58572de800ddb974f9b1f7c4c2e9e708e272caf`  
		Last Modified: Tue, 14 Nov 2023 19:26:21 GMT  
		Size: 56.3 MB (56296062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4756467c684a5489662a946c2274be869f7c863eff60a74a320a48ce786ab7ae`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9043dd2677465a371dbe7baa21aed779113f00e232f54cdd8d79e0ee5fb9d7`  
		Last Modified: Tue, 14 Nov 2023 19:26:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c092eba3670b63959de4d8094b03631a0cd53c05df4885dc411df0952acea459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7f220fbd29051e5f5bab6b85659d9fab302e5f6994b7c36021ad000b988c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88c985dac4c30a6a3ade1edb495df0a1f088e8965205cf5414b8fe7452826cb8`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bdf23f574c4dda1e207d57beefa48dfea197a6bf17c750cde4a813a84583a`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7.44`

```console
$ docker pull mysql@sha256:f566819f2eee3a60cf5ea6c8b7d1bfc9de62e34268bf62dc34870c4fca8a85d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7.44` - linux; amd64

```console
$ docker pull mysql@sha256:358b0482ced8103a8691c781e1cb6cd6b5a0b463a6dc0924a7ef357513ecc7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137898383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdba757bc9336a536d6884ecfaef00d24c1da3becd41e094eb226076436f258c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:15:11 GMT
ADD file:3e0277519395faaec643f0d6752812c14478974d1a914a763327a3cf30bbd28c in / 
# Tue, 24 Oct 2023 16:15:11 GMT
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
	-	`sha256:11a38aebcb7ae84df8b4fdcc1c7540389829a1f599b7a9986df89df733b69cea`  
		Last Modified: Tue, 14 Nov 2023 18:22:00 GMT  
		Size: 50.5 MB (50499111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ab01309bd664e500e70dbc3a6cd5a671ef725cc650bacddc6e3e3e0177c2e4`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c91fabb88c28533b95e5cd10d9612dcb5e0f8cba5b907e81b089af7b9bdcb43`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 983.6 KB (983553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46e806ab5c4d1750a22e436dd6a0843c79c2695dcb0c5515940957c94375cf`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 4.6 MB (4582768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f5af1d166141a7b944cac8f99e95fa74763b4b73bec000d949df541c26b9ee`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aca7179a542fdc7b3ab8cfecbe6b1d3e44f0bcabee6cad568d1c2d91c9ecc7`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85023e6de3be9d69a9eaf1473a15f89ce1ee93d622fe4922356006f4af79d9ba`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 25.5 MB (25526786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5934a87cbb3c1ca8617e6afb047b2f949631501df3b8cb129ebc370ff21dc0`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878502d3f701b4bc6d4a849b58572de800ddb974f9b1f7c4c2e9e708e272caf`  
		Last Modified: Tue, 14 Nov 2023 19:26:21 GMT  
		Size: 56.3 MB (56296062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4756467c684a5489662a946c2274be869f7c863eff60a74a320a48ce786ab7ae`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9043dd2677465a371dbe7baa21aed779113f00e232f54cdd8d79e0ee5fb9d7`  
		Last Modified: Tue, 14 Nov 2023 19:26:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7.44` - unknown; unknown

```console
$ docker pull mysql@sha256:c092eba3670b63959de4d8094b03631a0cd53c05df4885dc411df0952acea459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7f220fbd29051e5f5bab6b85659d9fab302e5f6994b7c36021ad000b988c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88c985dac4c30a6a3ade1edb495df0a1f088e8965205cf5414b8fe7452826cb8`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bdf23f574c4dda1e207d57beefa48dfea197a6bf17c750cde4a813a84583a`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7.44-oracle`

```console
$ docker pull mysql@sha256:f566819f2eee3a60cf5ea6c8b7d1bfc9de62e34268bf62dc34870c4fca8a85d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7.44-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:358b0482ced8103a8691c781e1cb6cd6b5a0b463a6dc0924a7ef357513ecc7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137898383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdba757bc9336a536d6884ecfaef00d24c1da3becd41e094eb226076436f258c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:15:11 GMT
ADD file:3e0277519395faaec643f0d6752812c14478974d1a914a763327a3cf30bbd28c in / 
# Tue, 24 Oct 2023 16:15:11 GMT
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
	-	`sha256:11a38aebcb7ae84df8b4fdcc1c7540389829a1f599b7a9986df89df733b69cea`  
		Last Modified: Tue, 14 Nov 2023 18:22:00 GMT  
		Size: 50.5 MB (50499111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ab01309bd664e500e70dbc3a6cd5a671ef725cc650bacddc6e3e3e0177c2e4`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c91fabb88c28533b95e5cd10d9612dcb5e0f8cba5b907e81b089af7b9bdcb43`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 983.6 KB (983553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46e806ab5c4d1750a22e436dd6a0843c79c2695dcb0c5515940957c94375cf`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 4.6 MB (4582768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f5af1d166141a7b944cac8f99e95fa74763b4b73bec000d949df541c26b9ee`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aca7179a542fdc7b3ab8cfecbe6b1d3e44f0bcabee6cad568d1c2d91c9ecc7`  
		Last Modified: Tue, 14 Nov 2023 19:26:18 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85023e6de3be9d69a9eaf1473a15f89ce1ee93d622fe4922356006f4af79d9ba`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 25.5 MB (25526786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5934a87cbb3c1ca8617e6afb047b2f949631501df3b8cb129ebc370ff21dc0`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878502d3f701b4bc6d4a849b58572de800ddb974f9b1f7c4c2e9e708e272caf`  
		Last Modified: Tue, 14 Nov 2023 19:26:21 GMT  
		Size: 56.3 MB (56296062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4756467c684a5489662a946c2274be869f7c863eff60a74a320a48ce786ab7ae`  
		Last Modified: Tue, 14 Nov 2023 19:26:19 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9043dd2677465a371dbe7baa21aed779113f00e232f54cdd8d79e0ee5fb9d7`  
		Last Modified: Tue, 14 Nov 2023 19:26:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c092eba3670b63959de4d8094b03631a0cd53c05df4885dc411df0952acea459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11547937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7f220fbd29051e5f5bab6b85659d9fab302e5f6994b7c36021ad000b988c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88c985dac4c30a6a3ade1edb495df0a1f088e8965205cf5414b8fe7452826cb8`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 11.5 MB (11511485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bdf23f574c4dda1e207d57beefa48dfea197a6bf17c750cde4a813a84583a`  
		Last Modified: Tue, 14 Nov 2023 19:26:17 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:40ab5148cf849eb9858040893a28d1dc1ef3fe0d13637c75fd263aed316614c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:a125abed3c1ece64aecf9688de25d3bae28a59cbe1fec52a1753f2a644fe3d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173758517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfac2ea6de190debeebcdf5946416d5c89895cffacb2bc4a1b3aea3ac18d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10307f5b5d6b80f2009b2968b54c73a53ce87aab8cf2cc75590f2c1401703eb9`  
		Last Modified: Wed, 06 Dec 2023 20:13:44 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa16cc40bab771c815f19f467b96113f14cf2316effbbd27489eb1e1f09ee2`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 982.8 KB (982807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5d160ea917e3ee16f99c56e8b2677c0b64533c5d3bcbb6863936b58436a264`  
		Last Modified: Wed, 06 Dec 2023 20:13:46 GMT  
		Size: 4.6 MB (4606840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fd99b1e69e155441ef84cf0ea85ff4cca8d58b05bc30897ec493094a581e14`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bebc3df0e2f79e2bf238fc8f3ccb11e8df932d396fd79e8cd2fd3afde9ac56b`  
		Last Modified: Wed, 06 Dec 2023 20:13:46 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8068fd681d68e5bb90e0f749cb0c3a74d79842c591cffdaf8afaaa807bf5e415`  
		Last Modified: Wed, 06 Dec 2023 20:13:49 GMT  
		Size: 58.5 MB (58514559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be724b42e1184b308679dcc82719fc6431410686bef1a7516dccae61a231b8`  
		Last Modified: Wed, 06 Dec 2023 20:13:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5476ce09045ccd815a2c329e3a5c60e714bcf6cbde212884d8a8068a3e0f529`  
		Last Modified: Wed, 06 Dec 2023 20:13:49 GMT  
		Size: 58.3 MB (58324696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7710edad2dbb6ca9d24ae16fdaed3406b17147147b8820cad9789dc08fec4`  
		Last Modified: Wed, 06 Dec 2023 20:13:47 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d628f25d4da7e7d0fecf80ef62b866ec18a8081b27c7c773ab705d9add740`  
		Last Modified: Wed, 06 Dec 2023 20:13:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:12c1e3229b2967dd180bd9e7d11c3f3af8c286f58b2563c4fed23dcf4f5f29b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f31d44124c836254f983a686750c7c643df75ea7d25dbcd8720244bed14903`

```dockerfile
```

-	Layers:
	-	`sha256:c829714d3ea447198b24b44f142a57ee60082088462437a670bc56b43a4c3a70`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 11.6 MB (11567360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77452b61a4f7728c2969a4c33572be524de73d4d65a850aed7ffc01d8b35a94c`  
		Last Modified: Wed, 06 Dec 2023 20:13:44 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f65b6f36aa681795298dbfc608f9b3b9893a85684f72cfd3f605ab4653403612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4974f91543c250c9d327287af62f5e4fe0801a8f8da89384ed0c6bc352e6b5e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed6e3f1776718eb68b00279f695bd66e98f2cca29227c638981fec4e2fd9cb`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aca5ebfaba67d01add373a7ea687ae1ab06a013ddfe762e5fa2fac66c648f2`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 57.6 MB (57573639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deaa7499105a91874ae795f79c6471a7b16f4da822ac04b770b2bebdd33b9a5`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfee2607bfc89806f905f4478c15b70e606b2be0578e85b8a7c57c0957d48092`  
		Last Modified: Wed, 06 Dec 2023 21:17:32 GMT  
		Size: 64.6 MB (64575456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac8111285e24b9455ce1e3f9e0db890c26f7e8c94480cd125ce3cd735e1d20`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633671d9b4d85d88cf6f87585a78796e33242ff9265fa14f3f71eaff3f3d36c`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:1c8f6d0adcaba5d3b1c7130a80260dd0ea9c5d457f8a53ef0e09ec01e4b0ce5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401a8ad864b24e17b8f0932eae64f2df3eb96ccabe1d362ad2e20f696e98f0a2`

```dockerfile
```

-	Layers:
	-	`sha256:b2a0885e5dc92d43d666406a4efd8ffba1157dc7f88361e5f47e2a8aa7182c69`  
		Last Modified: Wed, 06 Dec 2023 21:17:30 GMT  
		Size: 11.6 MB (11565936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4c3ef20ddb6e4e8f82134bff5243142092f3aa455dd89b6bdcd9b57ae015a3`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 34.0 KB (34034 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:b8468d29f56498197888c573b7fa976cba3419233d4c9e405bc4d5c11a6b41c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:fd8f47c32de2993a704627bffca9b64495c156ec6e85e0af4074cf908830a794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179121251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd3c2ee4c5ac7dd9004ae4912168d0b784c8e2d556eff5cf170dffac130a64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c04f50b14afc01d8263ce8d758081291c712b4130ed529c2e63af81c4add5ee`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb2b8bfab5d7ed341674cda53b09d69981231d9a24de0fc0ebdb770bab6d5a9`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 4.2 MB (4207478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06848c6e0c8410b16c688adbaf5dd5c550fa43afd08a2d22ee8778d7139255c6`  
		Last Modified: Tue, 21 Nov 2023 06:17:17 GMT  
		Size: 1.5 MB (1472433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98691176bf0fcac8516c24d392c6e2754e47799f921436c013801c3c9e7f03c`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a46cc0d0031ef20735d56061d06520ee2a75a06b9a64dc3256cf0d2ae6ed27d`  
		Last Modified: Tue, 21 Nov 2023 06:17:17 GMT  
		Size: 12.5 MB (12454719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b33a1d9de8b3d8448468e72edca9de0b6fda512e6730b915fd08f036c7e9f3`  
		Last Modified: Tue, 21 Nov 2023 06:17:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e8fe85abdf72e4f7f3a9185e37dcd21c5f60f2787aede5173b02e8a98e98ab`  
		Last Modified: Tue, 21 Nov 2023 06:17:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad0e42be1e0fae889fd014114a6246c66b91794b9c4592b8910573c95a57a36`  
		Last Modified: Tue, 21 Nov 2023 06:17:19 GMT  
		Size: 129.6 MB (129557949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f991fc99fab2c3dbae168fd46d67f25524eb55eeda4f496ac331444c152e57c`  
		Last Modified: Tue, 21 Nov 2023 06:17:18 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f16fe0cadddb711042a68e3e9b2d7e92fc929f931b509a695f824b03a06ef98`  
		Last Modified: Tue, 21 Nov 2023 06:17:18 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbe64f95283b26e42d67d918a265a7eb110b1fd9e0a4d92d3f22aaec7aca330`  
		Last Modified: Tue, 21 Nov 2023 06:17:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:e134f07f183d462484aa85a786988fc043d50c24597f7fb8879ffc864d8ae282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486f6b96b26386c24400ad7f9a489ddb5aef50c482d43b79d0db765b1677ae06`

```dockerfile
```

-	Layers:
	-	`sha256:ce3f53752dccb622c781f0272b3becc6ad73017c219544f45981461dd388b97e`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 3.6 MB (3552338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ccb195ddc60b2195d012022d223558e8feb8c6e1faf82d39c67a892d9df4f33`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 33.3 KB (33289 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:40ab5148cf849eb9858040893a28d1dc1ef3fe0d13637c75fd263aed316614c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a125abed3c1ece64aecf9688de25d3bae28a59cbe1fec52a1753f2a644fe3d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173758517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfac2ea6de190debeebcdf5946416d5c89895cffacb2bc4a1b3aea3ac18d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10307f5b5d6b80f2009b2968b54c73a53ce87aab8cf2cc75590f2c1401703eb9`  
		Last Modified: Wed, 06 Dec 2023 20:13:44 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa16cc40bab771c815f19f467b96113f14cf2316effbbd27489eb1e1f09ee2`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 982.8 KB (982807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5d160ea917e3ee16f99c56e8b2677c0b64533c5d3bcbb6863936b58436a264`  
		Last Modified: Wed, 06 Dec 2023 20:13:46 GMT  
		Size: 4.6 MB (4606840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fd99b1e69e155441ef84cf0ea85ff4cca8d58b05bc30897ec493094a581e14`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bebc3df0e2f79e2bf238fc8f3ccb11e8df932d396fd79e8cd2fd3afde9ac56b`  
		Last Modified: Wed, 06 Dec 2023 20:13:46 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8068fd681d68e5bb90e0f749cb0c3a74d79842c591cffdaf8afaaa807bf5e415`  
		Last Modified: Wed, 06 Dec 2023 20:13:49 GMT  
		Size: 58.5 MB (58514559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be724b42e1184b308679dcc82719fc6431410686bef1a7516dccae61a231b8`  
		Last Modified: Wed, 06 Dec 2023 20:13:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5476ce09045ccd815a2c329e3a5c60e714bcf6cbde212884d8a8068a3e0f529`  
		Last Modified: Wed, 06 Dec 2023 20:13:49 GMT  
		Size: 58.3 MB (58324696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7710edad2dbb6ca9d24ae16fdaed3406b17147147b8820cad9789dc08fec4`  
		Last Modified: Wed, 06 Dec 2023 20:13:47 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d628f25d4da7e7d0fecf80ef62b866ec18a8081b27c7c773ab705d9add740`  
		Last Modified: Wed, 06 Dec 2023 20:13:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:12c1e3229b2967dd180bd9e7d11c3f3af8c286f58b2563c4fed23dcf4f5f29b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f31d44124c836254f983a686750c7c643df75ea7d25dbcd8720244bed14903`

```dockerfile
```

-	Layers:
	-	`sha256:c829714d3ea447198b24b44f142a57ee60082088462437a670bc56b43a4c3a70`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 11.6 MB (11567360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77452b61a4f7728c2969a4c33572be524de73d4d65a850aed7ffc01d8b35a94c`  
		Last Modified: Wed, 06 Dec 2023 20:13:44 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f65b6f36aa681795298dbfc608f9b3b9893a85684f72cfd3f605ab4653403612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4974f91543c250c9d327287af62f5e4fe0801a8f8da89384ed0c6bc352e6b5e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed6e3f1776718eb68b00279f695bd66e98f2cca29227c638981fec4e2fd9cb`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aca5ebfaba67d01add373a7ea687ae1ab06a013ddfe762e5fa2fac66c648f2`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 57.6 MB (57573639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deaa7499105a91874ae795f79c6471a7b16f4da822ac04b770b2bebdd33b9a5`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfee2607bfc89806f905f4478c15b70e606b2be0578e85b8a7c57c0957d48092`  
		Last Modified: Wed, 06 Dec 2023 21:17:32 GMT  
		Size: 64.6 MB (64575456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac8111285e24b9455ce1e3f9e0db890c26f7e8c94480cd125ce3cd735e1d20`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633671d9b4d85d88cf6f87585a78796e33242ff9265fa14f3f71eaff3f3d36c`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1c8f6d0adcaba5d3b1c7130a80260dd0ea9c5d457f8a53ef0e09ec01e4b0ce5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401a8ad864b24e17b8f0932eae64f2df3eb96ccabe1d362ad2e20f696e98f0a2`

```dockerfile
```

-	Layers:
	-	`sha256:b2a0885e5dc92d43d666406a4efd8ffba1157dc7f88361e5f47e2a8aa7182c69`  
		Last Modified: Wed, 06 Dec 2023 21:17:30 GMT  
		Size: 11.6 MB (11565936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4c3ef20ddb6e4e8f82134bff5243142092f3aa455dd89b6bdcd9b57ae015a3`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 34.0 KB (34034 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35`

```console
$ docker pull mysql@sha256:40ab5148cf849eb9858040893a28d1dc1ef3fe0d13637c75fd263aed316614c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35` - linux; amd64

```console
$ docker pull mysql@sha256:a125abed3c1ece64aecf9688de25d3bae28a59cbe1fec52a1753f2a644fe3d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173758517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfac2ea6de190debeebcdf5946416d5c89895cffacb2bc4a1b3aea3ac18d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10307f5b5d6b80f2009b2968b54c73a53ce87aab8cf2cc75590f2c1401703eb9`  
		Last Modified: Wed, 06 Dec 2023 20:13:44 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa16cc40bab771c815f19f467b96113f14cf2316effbbd27489eb1e1f09ee2`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 982.8 KB (982807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5d160ea917e3ee16f99c56e8b2677c0b64533c5d3bcbb6863936b58436a264`  
		Last Modified: Wed, 06 Dec 2023 20:13:46 GMT  
		Size: 4.6 MB (4606840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fd99b1e69e155441ef84cf0ea85ff4cca8d58b05bc30897ec493094a581e14`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bebc3df0e2f79e2bf238fc8f3ccb11e8df932d396fd79e8cd2fd3afde9ac56b`  
		Last Modified: Wed, 06 Dec 2023 20:13:46 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8068fd681d68e5bb90e0f749cb0c3a74d79842c591cffdaf8afaaa807bf5e415`  
		Last Modified: Wed, 06 Dec 2023 20:13:49 GMT  
		Size: 58.5 MB (58514559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be724b42e1184b308679dcc82719fc6431410686bef1a7516dccae61a231b8`  
		Last Modified: Wed, 06 Dec 2023 20:13:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5476ce09045ccd815a2c329e3a5c60e714bcf6cbde212884d8a8068a3e0f529`  
		Last Modified: Wed, 06 Dec 2023 20:13:49 GMT  
		Size: 58.3 MB (58324696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7710edad2dbb6ca9d24ae16fdaed3406b17147147b8820cad9789dc08fec4`  
		Last Modified: Wed, 06 Dec 2023 20:13:47 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d628f25d4da7e7d0fecf80ef62b866ec18a8081b27c7c773ab705d9add740`  
		Last Modified: Wed, 06 Dec 2023 20:13:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35` - unknown; unknown

```console
$ docker pull mysql@sha256:12c1e3229b2967dd180bd9e7d11c3f3af8c286f58b2563c4fed23dcf4f5f29b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f31d44124c836254f983a686750c7c643df75ea7d25dbcd8720244bed14903`

```dockerfile
```

-	Layers:
	-	`sha256:c829714d3ea447198b24b44f142a57ee60082088462437a670bc56b43a4c3a70`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 11.6 MB (11567360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77452b61a4f7728c2969a4c33572be524de73d4d65a850aed7ffc01d8b35a94c`  
		Last Modified: Wed, 06 Dec 2023 20:13:44 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f65b6f36aa681795298dbfc608f9b3b9893a85684f72cfd3f605ab4653403612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4974f91543c250c9d327287af62f5e4fe0801a8f8da89384ed0c6bc352e6b5e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed6e3f1776718eb68b00279f695bd66e98f2cca29227c638981fec4e2fd9cb`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aca5ebfaba67d01add373a7ea687ae1ab06a013ddfe762e5fa2fac66c648f2`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 57.6 MB (57573639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deaa7499105a91874ae795f79c6471a7b16f4da822ac04b770b2bebdd33b9a5`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfee2607bfc89806f905f4478c15b70e606b2be0578e85b8a7c57c0957d48092`  
		Last Modified: Wed, 06 Dec 2023 21:17:32 GMT  
		Size: 64.6 MB (64575456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac8111285e24b9455ce1e3f9e0db890c26f7e8c94480cd125ce3cd735e1d20`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633671d9b4d85d88cf6f87585a78796e33242ff9265fa14f3f71eaff3f3d36c`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35` - unknown; unknown

```console
$ docker pull mysql@sha256:1c8f6d0adcaba5d3b1c7130a80260dd0ea9c5d457f8a53ef0e09ec01e4b0ce5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401a8ad864b24e17b8f0932eae64f2df3eb96ccabe1d362ad2e20f696e98f0a2`

```dockerfile
```

-	Layers:
	-	`sha256:b2a0885e5dc92d43d666406a4efd8ffba1157dc7f88361e5f47e2a8aa7182c69`  
		Last Modified: Wed, 06 Dec 2023 21:17:30 GMT  
		Size: 11.6 MB (11565936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4c3ef20ddb6e4e8f82134bff5243142092f3aa455dd89b6bdcd9b57ae015a3`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 34.0 KB (34034 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-debian`

```console
$ docker pull mysql@sha256:b8468d29f56498197888c573b7fa976cba3419233d4c9e405bc4d5c11a6b41c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.35-debian` - linux; amd64

```console
$ docker pull mysql@sha256:fd8f47c32de2993a704627bffca9b64495c156ec6e85e0af4074cf908830a794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179121251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd3c2ee4c5ac7dd9004ae4912168d0b784c8e2d556eff5cf170dffac130a64d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c04f50b14afc01d8263ce8d758081291c712b4130ed529c2e63af81c4add5ee`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb2b8bfab5d7ed341674cda53b09d69981231d9a24de0fc0ebdb770bab6d5a9`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 4.2 MB (4207478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06848c6e0c8410b16c688adbaf5dd5c550fa43afd08a2d22ee8778d7139255c6`  
		Last Modified: Tue, 21 Nov 2023 06:17:17 GMT  
		Size: 1.5 MB (1472433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98691176bf0fcac8516c24d392c6e2754e47799f921436c013801c3c9e7f03c`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a46cc0d0031ef20735d56061d06520ee2a75a06b9a64dc3256cf0d2ae6ed27d`  
		Last Modified: Tue, 21 Nov 2023 06:17:17 GMT  
		Size: 12.5 MB (12454719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b33a1d9de8b3d8448468e72edca9de0b6fda512e6730b915fd08f036c7e9f3`  
		Last Modified: Tue, 21 Nov 2023 06:17:17 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e8fe85abdf72e4f7f3a9185e37dcd21c5f60f2787aede5173b02e8a98e98ab`  
		Last Modified: Tue, 21 Nov 2023 06:17:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad0e42be1e0fae889fd014114a6246c66b91794b9c4592b8910573c95a57a36`  
		Last Modified: Tue, 21 Nov 2023 06:17:19 GMT  
		Size: 129.6 MB (129557949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f991fc99fab2c3dbae168fd46d67f25524eb55eeda4f496ac331444c152e57c`  
		Last Modified: Tue, 21 Nov 2023 06:17:18 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f16fe0cadddb711042a68e3e9b2d7e92fc929f931b509a695f824b03a06ef98`  
		Last Modified: Tue, 21 Nov 2023 06:17:18 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbe64f95283b26e42d67d918a265a7eb110b1fd9e0a4d92d3f22aaec7aca330`  
		Last Modified: Tue, 21 Nov 2023 06:17:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:e134f07f183d462484aa85a786988fc043d50c24597f7fb8879ffc864d8ae282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486f6b96b26386c24400ad7f9a489ddb5aef50c482d43b79d0db765b1677ae06`

```dockerfile
```

-	Layers:
	-	`sha256:ce3f53752dccb622c781f0272b3becc6ad73017c219544f45981461dd388b97e`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 3.6 MB (3552338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ccb195ddc60b2195d012022d223558e8feb8c6e1faf82d39c67a892d9df4f33`  
		Last Modified: Tue, 21 Nov 2023 06:17:16 GMT  
		Size: 33.3 KB (33289 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-oracle`

```console
$ docker pull mysql@sha256:40ab5148cf849eb9858040893a28d1dc1ef3fe0d13637c75fd263aed316614c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a125abed3c1ece64aecf9688de25d3bae28a59cbe1fec52a1753f2a644fe3d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173758517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfac2ea6de190debeebcdf5946416d5c89895cffacb2bc4a1b3aea3ac18d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10307f5b5d6b80f2009b2968b54c73a53ce87aab8cf2cc75590f2c1401703eb9`  
		Last Modified: Wed, 06 Dec 2023 20:13:44 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa16cc40bab771c815f19f467b96113f14cf2316effbbd27489eb1e1f09ee2`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 982.8 KB (982807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5d160ea917e3ee16f99c56e8b2677c0b64533c5d3bcbb6863936b58436a264`  
		Last Modified: Wed, 06 Dec 2023 20:13:46 GMT  
		Size: 4.6 MB (4606840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fd99b1e69e155441ef84cf0ea85ff4cca8d58b05bc30897ec493094a581e14`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bebc3df0e2f79e2bf238fc8f3ccb11e8df932d396fd79e8cd2fd3afde9ac56b`  
		Last Modified: Wed, 06 Dec 2023 20:13:46 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8068fd681d68e5bb90e0f749cb0c3a74d79842c591cffdaf8afaaa807bf5e415`  
		Last Modified: Wed, 06 Dec 2023 20:13:49 GMT  
		Size: 58.5 MB (58514559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be724b42e1184b308679dcc82719fc6431410686bef1a7516dccae61a231b8`  
		Last Modified: Wed, 06 Dec 2023 20:13:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5476ce09045ccd815a2c329e3a5c60e714bcf6cbde212884d8a8068a3e0f529`  
		Last Modified: Wed, 06 Dec 2023 20:13:49 GMT  
		Size: 58.3 MB (58324696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7710edad2dbb6ca9d24ae16fdaed3406b17147147b8820cad9789dc08fec4`  
		Last Modified: Wed, 06 Dec 2023 20:13:47 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d628f25d4da7e7d0fecf80ef62b866ec18a8081b27c7c773ab705d9add740`  
		Last Modified: Wed, 06 Dec 2023 20:13:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:12c1e3229b2967dd180bd9e7d11c3f3af8c286f58b2563c4fed23dcf4f5f29b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f31d44124c836254f983a686750c7c643df75ea7d25dbcd8720244bed14903`

```dockerfile
```

-	Layers:
	-	`sha256:c829714d3ea447198b24b44f142a57ee60082088462437a670bc56b43a4c3a70`  
		Last Modified: Wed, 06 Dec 2023 20:13:45 GMT  
		Size: 11.6 MB (11567360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77452b61a4f7728c2969a4c33572be524de73d4d65a850aed7ffc01d8b35a94c`  
		Last Modified: Wed, 06 Dec 2023 20:13:44 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f65b6f36aa681795298dbfc608f9b3b9893a85684f72cfd3f605ab4653403612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4974f91543c250c9d327287af62f5e4fe0801a8f8da89384ed0c6bc352e6b5e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:18:19 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:18:19 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed6e3f1776718eb68b00279f695bd66e98f2cca29227c638981fec4e2fd9cb`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aca5ebfaba67d01add373a7ea687ae1ab06a013ddfe762e5fa2fac66c648f2`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 57.6 MB (57573639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deaa7499105a91874ae795f79c6471a7b16f4da822ac04b770b2bebdd33b9a5`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfee2607bfc89806f905f4478c15b70e606b2be0578e85b8a7c57c0957d48092`  
		Last Modified: Wed, 06 Dec 2023 21:17:32 GMT  
		Size: 64.6 MB (64575456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac8111285e24b9455ce1e3f9e0db890c26f7e8c94480cd125ce3cd735e1d20`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633671d9b4d85d88cf6f87585a78796e33242ff9265fa14f3f71eaff3f3d36c`  
		Last Modified: Wed, 06 Dec 2023 21:17:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1c8f6d0adcaba5d3b1c7130a80260dd0ea9c5d457f8a53ef0e09ec01e4b0ce5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401a8ad864b24e17b8f0932eae64f2df3eb96ccabe1d362ad2e20f696e98f0a2`

```dockerfile
```

-	Layers:
	-	`sha256:b2a0885e5dc92d43d666406a4efd8ffba1157dc7f88361e5f47e2a8aa7182c69`  
		Last Modified: Wed, 06 Dec 2023 21:17:30 GMT  
		Size: 11.6 MB (11565936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4c3ef20ddb6e4e8f82134bff5243142092f3aa455dd89b6bdcd9b57ae015a3`  
		Last Modified: Wed, 06 Dec 2023 21:17:29 GMT  
		Size: 34.0 KB (34034 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2-oracle`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0-oracle`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:6057dec95d87a0d7880d9cfc9b3d9292f9c11473a5104b906402a2b73396e377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:757ecdb9565a3a0d98a764484c0157df4b255a1ec2303a29177aac15749a61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177827340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdab215ab77d3c9f93d4a1afa4b77850bc1b1ed1372ffe31b96ad9cd78a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041cd0148ecebb2cde9ecefaf4d6a51d42158c6f9b2557ebc90c3ec7e99435e`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9fbf7aa29d89d2d9810e7620be8d02df888a1493c55df86bd56e9d4ab967d`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 982.8 KB (982808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc1efc1f1fa5752c818cee58c15991e640f8c30aa51c6b626e53e450877297`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d25a6611c2e88e645f765990dc520500b451bceee20a9db68f55fc358ba6c1`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846de7fe479fa0b557f248fc31698bfb7e5690b0edcb6d100625c22a6e4eaa7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf13e3256e8f3d879093b92bcad87822c157e16661a0c7e46082f1b35ac6ea9`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 62.6 MB (62585253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ed684a4fa569efc85222bf6128950f89ed18bd3fa90441bd1355608a0f22`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bfd3acf105c0d174e8362d77a63194a825c6b867ed126d50d5961fe4096f3b`  
		Last Modified: Wed, 06 Dec 2023 20:15:57 GMT  
		Size: 58.3 MB (58322922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68afdb04ae0c4232096342e684bf7ca2e3125c0e39c5b143459b16e142cba3`  
		Last Modified: Wed, 06 Dec 2023 20:15:56 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7b007b849c8fa06bc77baa3851260c53d576eb7177d0a14ea09986106f2a8b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bf635e48d035ad1bd9e90ef85a9041d0cc151da3e7540e4de93733f5885ae`

```dockerfile
```

-	Layers:
	-	`sha256:4b43ac920f8d73b767738036286920c7a1a6e83051b52b13e46cab8aef2da6b7`  
		Last Modified: Wed, 06 Dec 2023 20:15:55 GMT  
		Size: 11.6 MB (11569857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25183afaa3c91cdfb7be3414d8d446a697f9620eeb767681768c02f180ef2049`  
		Last Modified: Wed, 06 Dec 2023 20:15:54 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:be521da8b7992f6c950f103f55c2b47a52eafac90729e782e92f5ce09736f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c61872d4987a19e0bc9028731b0e94954ffe9c7fafb49f3b41784615da9cd2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 24 Oct 2023 16:24:49 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Tue, 24 Oct 2023 16:24:49 GMT
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
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fa257184cbabb42ef3365b6e8a2f50fcc7fe28f49c6511783bd3d41277974`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f07c7bd808cf5db2d75a352fad9abe82fb6d47d1655d49ef47d4cc54d042`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 913.0 KB (912966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ad857d8cbb18a682a7ae9423b36f9ef89fbff9698f9cc25b0caf383146cc`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 4.3 MB (4300793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0aaa5cd9dd34b61d7e07d65a142ce83f19215ebd708a3d575f7e2ae1eb4c18`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f7a2c7ba00e1068901233b73719b7398a620ea3bb8417f6db1eebd742d178`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8e8957267fbe1e15c429f3270e5e51fdc7caad1a88f3a05b2166824b46a2e`  
		Last Modified: Wed, 06 Dec 2023 21:15:38 GMT  
		Size: 61.6 MB (61602942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79963848dcea34c8d7405835b4b6402e7692f2a9a69b20fbbd0d5ec7b897ed`  
		Last Modified: Wed, 06 Dec 2023 21:15:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4e430daf10249def03bcaad227f98fd2cdacbb12b824e0d181d139727509b`  
		Last Modified: Wed, 06 Dec 2023 21:15:39 GMT  
		Size: 64.6 MB (64573976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630e7dc32ebed22dd97a36f884301172b2a14928a3736ab73463d56bf7fd46b7`  
		Last Modified: Wed, 06 Dec 2023 21:15:37 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:97e9b6520d32d1a595a98e7d5db2968fe5d2ff9aed3820a021d483174bebe306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa989ffdba0d9c81002b75059bb5d3e3128bfaf88e05135bdeeb9302007242a`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca88b5707c0acb96644f01e35a5b7f6beee76f341a8edee75efc10fa2df6f3`  
		Last Modified: Wed, 06 Dec 2023 21:15:35 GMT  
		Size: 11.6 MB (11568445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37bd988db8fef2d2f2a5df2d02fcc07c4c711c4fa679003f7295ef17bb193f`  
		Last Modified: Wed, 06 Dec 2023 21:15:34 GMT  
		Size: 33.6 KB (33601 bytes)  
		MIME: application/vnd.in-toto+json
