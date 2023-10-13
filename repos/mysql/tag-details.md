<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.43`](#mysql5743)
-	[`mysql:5.7.43-oracle`](#mysql5743-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.34`](#mysql8034)
-	[`mysql:8.0.34-debian`](#mysql8034-debian)
-	[`mysql:8.0.34-oracle`](#mysql8034-oracle)
-	[`mysql:8.1`](#mysql81)
-	[`mysql:8.1-oracle`](#mysql81-oracle)
-	[`mysql:8.1.0`](#mysql810)
-	[`mysql:8.1.0-oracle`](#mysql810-oracle)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:4f9bfb0f7dd97739ceedb546b381534bb11e9b4abf013d6ad9ae6473fed66099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:188121394576d05aedb5daf229403bf58d4ee16e04e81828e4d43b72bd227bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170176061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b85be0b10d389e268b35d4c04075b95c295dd24d595e8c5261e43ab94c47de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:54 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:54 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4eda42c982f018b636fece13fbfe13b3c485002a9e5b1b4742d4a9b2472344`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 870.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6d882cf587c90f71772f078245206204ef6e06995073356c7a2e00d328d14c`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 983.5 KB (983548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c804e92b324adecac8c3c0829f89949711442b1895d71c858360a18bfdd1043`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 4.6 MB (4581890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54ada0c48d0dec4f65e2e53d9924fca6888029f800b994c4ad5629e5503172`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8fb20ac8df2f75e04b1bb786677b8ed82131aa33d652f176b708e0e05a350`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b1bc545491ca4135d1327d5d78299951efe05b6306e683d5d85f5d367ac3`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 25.5 MB (25533109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c3423057b75bfcdb2dcc8930c701bbcbebbe183f13ebd17316eee7657fa69f`  
		Last Modified: Thu, 12 Oct 2023 22:46:50 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122b2c7b16c0784f4f6edf05f89df6cd3864f50838f30ba1c58a7c1e00515cd1`  
		Last Modified: Thu, 12 Oct 2023 22:46:56 GMT  
		Size: 88.6 MB (88570755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30e03d70e3e18516a20a38b5f5160974f52706f98e372c560a51d22479788f`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c43898e898ff024290d810c763e672209840a60f00ecd50cf138b16756c88d`  
		Last Modified: Thu, 12 Oct 2023 22:46:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5` - unknown; unknown

```console
$ docker pull mysql@sha256:f6d617308dde54c4515d27dc7f6c3190da1a767bf4203eb03d6f0491cc6a0909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14459686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102079ba75bd947c0eff2ef29718862d2a85b66bae829bc1cb0435887adb1f9`

```dockerfile
```

-	Layers:
	-	`sha256:0f321d3ef98514552b6fb61836bf1e7c253e5c213a5b39c963115490a11509ef`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 14.4 MB (14423234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e53b4ee50168adfbdb6db4e785a17926a698ce8595d58be1fce6cac977106b`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:4f9bfb0f7dd97739ceedb546b381534bb11e9b4abf013d6ad9ae6473fed66099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:188121394576d05aedb5daf229403bf58d4ee16e04e81828e4d43b72bd227bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170176061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b85be0b10d389e268b35d4c04075b95c295dd24d595e8c5261e43ab94c47de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:54 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:54 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4eda42c982f018b636fece13fbfe13b3c485002a9e5b1b4742d4a9b2472344`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 870.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6d882cf587c90f71772f078245206204ef6e06995073356c7a2e00d328d14c`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 983.5 KB (983548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c804e92b324adecac8c3c0829f89949711442b1895d71c858360a18bfdd1043`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 4.6 MB (4581890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54ada0c48d0dec4f65e2e53d9924fca6888029f800b994c4ad5629e5503172`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8fb20ac8df2f75e04b1bb786677b8ed82131aa33d652f176b708e0e05a350`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b1bc545491ca4135d1327d5d78299951efe05b6306e683d5d85f5d367ac3`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 25.5 MB (25533109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c3423057b75bfcdb2dcc8930c701bbcbebbe183f13ebd17316eee7657fa69f`  
		Last Modified: Thu, 12 Oct 2023 22:46:50 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122b2c7b16c0784f4f6edf05f89df6cd3864f50838f30ba1c58a7c1e00515cd1`  
		Last Modified: Thu, 12 Oct 2023 22:46:56 GMT  
		Size: 88.6 MB (88570755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30e03d70e3e18516a20a38b5f5160974f52706f98e372c560a51d22479788f`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c43898e898ff024290d810c763e672209840a60f00ecd50cf138b16756c88d`  
		Last Modified: Thu, 12 Oct 2023 22:46:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6d617308dde54c4515d27dc7f6c3190da1a767bf4203eb03d6f0491cc6a0909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14459686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102079ba75bd947c0eff2ef29718862d2a85b66bae829bc1cb0435887adb1f9`

```dockerfile
```

-	Layers:
	-	`sha256:0f321d3ef98514552b6fb61836bf1e7c253e5c213a5b39c963115490a11509ef`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 14.4 MB (14423234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e53b4ee50168adfbdb6db4e785a17926a698ce8595d58be1fce6cac977106b`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7`

```console
$ docker pull mysql@sha256:4f9bfb0f7dd97739ceedb546b381534bb11e9b4abf013d6ad9ae6473fed66099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:188121394576d05aedb5daf229403bf58d4ee16e04e81828e4d43b72bd227bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170176061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b85be0b10d389e268b35d4c04075b95c295dd24d595e8c5261e43ab94c47de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:54 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:54 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4eda42c982f018b636fece13fbfe13b3c485002a9e5b1b4742d4a9b2472344`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 870.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6d882cf587c90f71772f078245206204ef6e06995073356c7a2e00d328d14c`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 983.5 KB (983548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c804e92b324adecac8c3c0829f89949711442b1895d71c858360a18bfdd1043`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 4.6 MB (4581890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54ada0c48d0dec4f65e2e53d9924fca6888029f800b994c4ad5629e5503172`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8fb20ac8df2f75e04b1bb786677b8ed82131aa33d652f176b708e0e05a350`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b1bc545491ca4135d1327d5d78299951efe05b6306e683d5d85f5d367ac3`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 25.5 MB (25533109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c3423057b75bfcdb2dcc8930c701bbcbebbe183f13ebd17316eee7657fa69f`  
		Last Modified: Thu, 12 Oct 2023 22:46:50 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122b2c7b16c0784f4f6edf05f89df6cd3864f50838f30ba1c58a7c1e00515cd1`  
		Last Modified: Thu, 12 Oct 2023 22:46:56 GMT  
		Size: 88.6 MB (88570755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30e03d70e3e18516a20a38b5f5160974f52706f98e372c560a51d22479788f`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c43898e898ff024290d810c763e672209840a60f00ecd50cf138b16756c88d`  
		Last Modified: Thu, 12 Oct 2023 22:46:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7` - unknown; unknown

```console
$ docker pull mysql@sha256:f6d617308dde54c4515d27dc7f6c3190da1a767bf4203eb03d6f0491cc6a0909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14459686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102079ba75bd947c0eff2ef29718862d2a85b66bae829bc1cb0435887adb1f9`

```dockerfile
```

-	Layers:
	-	`sha256:0f321d3ef98514552b6fb61836bf1e7c253e5c213a5b39c963115490a11509ef`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 14.4 MB (14423234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e53b4ee50168adfbdb6db4e785a17926a698ce8595d58be1fce6cac977106b`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:4f9bfb0f7dd97739ceedb546b381534bb11e9b4abf013d6ad9ae6473fed66099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:188121394576d05aedb5daf229403bf58d4ee16e04e81828e4d43b72bd227bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170176061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b85be0b10d389e268b35d4c04075b95c295dd24d595e8c5261e43ab94c47de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:54 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:54 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4eda42c982f018b636fece13fbfe13b3c485002a9e5b1b4742d4a9b2472344`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 870.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6d882cf587c90f71772f078245206204ef6e06995073356c7a2e00d328d14c`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 983.5 KB (983548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c804e92b324adecac8c3c0829f89949711442b1895d71c858360a18bfdd1043`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 4.6 MB (4581890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54ada0c48d0dec4f65e2e53d9924fca6888029f800b994c4ad5629e5503172`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8fb20ac8df2f75e04b1bb786677b8ed82131aa33d652f176b708e0e05a350`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b1bc545491ca4135d1327d5d78299951efe05b6306e683d5d85f5d367ac3`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 25.5 MB (25533109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c3423057b75bfcdb2dcc8930c701bbcbebbe183f13ebd17316eee7657fa69f`  
		Last Modified: Thu, 12 Oct 2023 22:46:50 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122b2c7b16c0784f4f6edf05f89df6cd3864f50838f30ba1c58a7c1e00515cd1`  
		Last Modified: Thu, 12 Oct 2023 22:46:56 GMT  
		Size: 88.6 MB (88570755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30e03d70e3e18516a20a38b5f5160974f52706f98e372c560a51d22479788f`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c43898e898ff024290d810c763e672209840a60f00ecd50cf138b16756c88d`  
		Last Modified: Thu, 12 Oct 2023 22:46:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6d617308dde54c4515d27dc7f6c3190da1a767bf4203eb03d6f0491cc6a0909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14459686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102079ba75bd947c0eff2ef29718862d2a85b66bae829bc1cb0435887adb1f9`

```dockerfile
```

-	Layers:
	-	`sha256:0f321d3ef98514552b6fb61836bf1e7c253e5c213a5b39c963115490a11509ef`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 14.4 MB (14423234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e53b4ee50168adfbdb6db4e785a17926a698ce8595d58be1fce6cac977106b`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7.43`

```console
$ docker pull mysql@sha256:4f9bfb0f7dd97739ceedb546b381534bb11e9b4abf013d6ad9ae6473fed66099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7.43` - linux; amd64

```console
$ docker pull mysql@sha256:188121394576d05aedb5daf229403bf58d4ee16e04e81828e4d43b72bd227bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170176061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b85be0b10d389e268b35d4c04075b95c295dd24d595e8c5261e43ab94c47de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:54 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:54 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4eda42c982f018b636fece13fbfe13b3c485002a9e5b1b4742d4a9b2472344`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 870.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6d882cf587c90f71772f078245206204ef6e06995073356c7a2e00d328d14c`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 983.5 KB (983548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c804e92b324adecac8c3c0829f89949711442b1895d71c858360a18bfdd1043`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 4.6 MB (4581890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54ada0c48d0dec4f65e2e53d9924fca6888029f800b994c4ad5629e5503172`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8fb20ac8df2f75e04b1bb786677b8ed82131aa33d652f176b708e0e05a350`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b1bc545491ca4135d1327d5d78299951efe05b6306e683d5d85f5d367ac3`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 25.5 MB (25533109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c3423057b75bfcdb2dcc8930c701bbcbebbe183f13ebd17316eee7657fa69f`  
		Last Modified: Thu, 12 Oct 2023 22:46:50 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122b2c7b16c0784f4f6edf05f89df6cd3864f50838f30ba1c58a7c1e00515cd1`  
		Last Modified: Thu, 12 Oct 2023 22:46:56 GMT  
		Size: 88.6 MB (88570755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30e03d70e3e18516a20a38b5f5160974f52706f98e372c560a51d22479788f`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c43898e898ff024290d810c763e672209840a60f00ecd50cf138b16756c88d`  
		Last Modified: Thu, 12 Oct 2023 22:46:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7.43` - unknown; unknown

```console
$ docker pull mysql@sha256:f6d617308dde54c4515d27dc7f6c3190da1a767bf4203eb03d6f0491cc6a0909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14459686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102079ba75bd947c0eff2ef29718862d2a85b66bae829bc1cb0435887adb1f9`

```dockerfile
```

-	Layers:
	-	`sha256:0f321d3ef98514552b6fb61836bf1e7c253e5c213a5b39c963115490a11509ef`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 14.4 MB (14423234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e53b4ee50168adfbdb6db4e785a17926a698ce8595d58be1fce6cac977106b`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:5.7.43-oracle`

```console
$ docker pull mysql@sha256:4f9bfb0f7dd97739ceedb546b381534bb11e9b4abf013d6ad9ae6473fed66099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:5.7.43-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:188121394576d05aedb5daf229403bf58d4ee16e04e81828e4d43b72bd227bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170176061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b85be0b10d389e268b35d4c04075b95c295dd24d595e8c5261e43ab94c47de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:54 GMT
ADD file:2726e2d5d9aaf4024ea489d9049884aa06c0c95d6111037ba29987ba029ddc44 in / 
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 27 Jul 2023 22:18:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Jul 2023 22:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:54 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9ad776bc39341b015fa96ec38b0ef30213514fedd245d657d3188d81b46d367c`  
		Last Modified: Thu, 12 Oct 2023 21:30:53 GMT  
		Size: 50.5 MB (50496653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4eda42c982f018b636fece13fbfe13b3c485002a9e5b1b4742d4a9b2472344`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 870.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6d882cf587c90f71772f078245206204ef6e06995073356c7a2e00d328d14c`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 983.5 KB (983548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c804e92b324adecac8c3c0829f89949711442b1895d71c858360a18bfdd1043`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 4.6 MB (4581890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54ada0c48d0dec4f65e2e53d9924fca6888029f800b994c4ad5629e5503172`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 3.1 KB (3077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8fb20ac8df2f75e04b1bb786677b8ed82131aa33d652f176b708e0e05a350`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b1bc545491ca4135d1327d5d78299951efe05b6306e683d5d85f5d367ac3`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 25.5 MB (25533109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c3423057b75bfcdb2dcc8930c701bbcbebbe183f13ebd17316eee7657fa69f`  
		Last Modified: Thu, 12 Oct 2023 22:46:50 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122b2c7b16c0784f4f6edf05f89df6cd3864f50838f30ba1c58a7c1e00515cd1`  
		Last Modified: Thu, 12 Oct 2023 22:46:56 GMT  
		Size: 88.6 MB (88570755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30e03d70e3e18516a20a38b5f5160974f52706f98e372c560a51d22479788f`  
		Last Modified: Thu, 12 Oct 2023 22:46:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c43898e898ff024290d810c763e672209840a60f00ecd50cf138b16756c88d`  
		Last Modified: Thu, 12 Oct 2023 22:46:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:5.7.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f6d617308dde54c4515d27dc7f6c3190da1a767bf4203eb03d6f0491cc6a0909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14459686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102079ba75bd947c0eff2ef29718862d2a85b66bae829bc1cb0435887adb1f9`

```dockerfile
```

-	Layers:
	-	`sha256:0f321d3ef98514552b6fb61836bf1e7c253e5c213a5b39c963115490a11509ef`  
		Last Modified: Thu, 12 Oct 2023 22:46:49 GMT  
		Size: 14.4 MB (14423234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e53b4ee50168adfbdb6db4e785a17926a698ce8595d58be1fce6cac977106b`  
		Last Modified: Thu, 12 Oct 2023 22:46:48 GMT  
		Size: 36.5 KB (36452 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:0ecb879cac92720d2800651c062eff258bde65072ff202e85915e1680030d8d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:af31a35b4de73a35bb764a4ed0e08f9c5c8c5159359f247162ee5b5138a77036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165886094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d38554e569caa399097757542f266c34ab2713cfcfe640d32d31a9213637d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db815db7655c8466ec50b5ddf092ddeffb6bfc9e742acacc56cbee4faafa8d4`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28bf3be614c52f9ea4aad5c5a145d573e5402443949165c861ace804c28e041`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0bce98d2423e0a9382dce198e21d3830b568e9bfdac22605cdc0e33cc7d4b3`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 4.6 MB (4613109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa28f8c9e4a0b1b3c7c68bb4c3cdb992074e7d7384535ec9ccdf17fda01fa40`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae93ee014f6766fb64e501b815c0270bbaaab10ae58a849938d8d1ba91947ca0`  
		Last Modified: Thu, 12 Oct 2023 22:47:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52f6ff520763a65fb3385d8800bb4f81dbedb07f6018c4c1d6216a6484a3d66`  
		Last Modified: Thu, 12 Oct 2023 22:47:58 GMT  
		Size: 58.5 MB (58482092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0395c647e3cd72e5248e5e4a8b6b85fac92439f9b448ff827b7c20089828138d`  
		Last Modified: Thu, 12 Oct 2023 22:47:55 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62096e97f2c522845f62b133dce62e16693b11dcf1bff34c9ef1a4e681fa0e4b`  
		Last Modified: Thu, 12 Oct 2023 22:47:59 GMT  
		Size: 57.5 MB (57519324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49723393f420522b6160272a3499e4f312ad3942f58825b7f30edc4ed6023a5`  
		Last Modified: Thu, 12 Oct 2023 22:47:56 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc49fc928f33645c6a887c77ee49d428fde01b9a01f1d9e8bddeb85e4a45dc`  
		Last Modified: Thu, 12 Oct 2023 22:47:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2e9380fd730acfdcf016c38c80ed086bd3cf24b7e5cd65d11183006ad5972ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4db265f38beb3c68a4def0cae55f97cab2f4156b26470881de56c619597dda`

```dockerfile
```

-	Layers:
	-	`sha256:63abe1f026ec435c825bc099c47cd0861f5d5a965d9082fffee2027e92f06858`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 13.1 MB (13106199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7add113b7b118cf45d3f4c3c4a54f6c75cd158703f5b21d1bae1be978789d9c1`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cea62ed306c9e2a96a3d8672381cdff326fd90123d284ef4852153c0a877835b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170129736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c3aea4e3deeec5a6139350e9c1bc1f108fbfdbeb136054e77ef4669e4ae1f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf89d2c4916c1368bf3a4c6fb20a4441ec8cd4a3d57bdb015e9277b17286a03`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79120d0882796ce1ccdabc2e93d363faa3227c0773f4dccdad561aab2814f783`  
		Last Modified: Thu, 12 Oct 2023 20:59:41 GMT  
		Size: 57.5 MB (57461596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d0fac447c9eae2f0323e6dedbe3131b2f651c46d5c52ee869f8d2e028a6c0e`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6095297ac0a99514ffaa4f43e03709f12a64bce3301266c6324beabac8608835`  
		Last Modified: Thu, 12 Oct 2023 20:59:42 GMT  
		Size: 63.8 MB (63772242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e274f5c921d7f5b78607112364fe96697bb43f6d9af8e38152c9d06b8cb0c9c9`  
		Last Modified: Thu, 12 Oct 2023 20:59:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969873ad404751d35993621a462d3350aeb15f63238fc5930bd78d177d52db66`  
		Last Modified: Thu, 12 Oct 2023 20:59:39 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3bc988bea23d6f5fd6693b7be9a8da8ace0346c8150ebe4bb0ea4e75cea797cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13138887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857f42418489e182abc8b171c9c5048be74e446e9448248ec9e30443bdfb6aa9`

```dockerfile
```

-	Layers:
	-	`sha256:243dd07e28b64dcf4c34487ff9d905b095c9774305c321224a45370ccdeea70b`  
		Last Modified: Thu, 12 Oct 2023 20:59:39 GMT  
		Size: 13.1 MB (13104850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36467b2da21cc688d8b4728c2e497669d084b9212de6b061103a4c13b82a64d5`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:2a31847951cdf92d6901ef58b4c5a9fbe75b47823d9ade1f7a4652ede7a88e2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e10fb73841ef30dcdb02e0759035f7730e5303cdc455268de219407d3fb4b846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179083456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc21a4e132a7e63c4a4eca71b3e75fbc7e965aef2b157a60a9c322e41e592795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1debian11
# Thu, 20 Jul 2023 22:15:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf330228e741604571f4caab61f2cc172717b89147d1238d45d057fb46edb697`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafbe13d22f4d4ef6ed406ac05b335dc1371424f95a2beafc66051e6cb3974bf`  
		Last Modified: Wed, 11 Oct 2023 20:03:40 GMT  
		Size: 4.2 MB (4207542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dcfd9f33b298cff0fc2ee7fd95dbd76a738414a4269d51121ef718fbcbf87b`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 1.5 MB (1472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae14d9c3e441351e1ec5b465e6bf617e393bc4a0ad072589600a2b8ae73b37`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1086d8d2521ba8f681003c1bb0594f31379d599a291c6646085f007fe8f395a1`  
		Last Modified: Wed, 11 Oct 2023 20:03:41 GMT  
		Size: 12.5 MB (12455173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afe97457504eb7005a224c7c679006bb937483986e5365633519004752f789`  
		Last Modified: Wed, 11 Oct 2023 20:03:40 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8169ee2bdb0a81c638c5dfb7aeef3c7c5b17755771f95a889cfe4c29b26e4966`  
		Last Modified: Wed, 11 Oct 2023 20:03:41 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc0f64b1cbafeb07f2c175c0486123720ed151cdd007b251816564e4381d23`  
		Last Modified: Wed, 11 Oct 2023 20:03:47 GMT  
		Size: 129.5 MB (129519547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3994da0db6238691c6a2208c2da4b3dafb961db6ca184feedab3435104154f4d`  
		Last Modified: Wed, 11 Oct 2023 20:03:41 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae385311e5ed3100ff6111e185211d9a5749c784bd675d0ba713898acb9dafd8`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 5.4 KB (5383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ceafee559334b9217ef6cde4d657abe3fb79466a7ef1b5e6f911d185b689f6`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:2831145c9d8abb4571f51bd89b331516c37b2b0421ec56d2647082e631ce3d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95857c88929774216f8e99858617023ea09d821927280ca85a5fbfdc8a6a609a`

```dockerfile
```

-	Layers:
	-	`sha256:d6cded17556303c4d1affc0cc57b7ae8b5fdce8a01462b0b5bf4608e0e7a413d`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 3.5 MB (3450737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29553eed5402c121dca04ea081b05fbfc44820c10ddb43cc09308bc0051fd6c1`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 33.3 KB (33289 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:0ecb879cac92720d2800651c062eff258bde65072ff202e85915e1680030d8d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:af31a35b4de73a35bb764a4ed0e08f9c5c8c5159359f247162ee5b5138a77036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165886094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d38554e569caa399097757542f266c34ab2713cfcfe640d32d31a9213637d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db815db7655c8466ec50b5ddf092ddeffb6bfc9e742acacc56cbee4faafa8d4`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28bf3be614c52f9ea4aad5c5a145d573e5402443949165c861ace804c28e041`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0bce98d2423e0a9382dce198e21d3830b568e9bfdac22605cdc0e33cc7d4b3`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 4.6 MB (4613109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa28f8c9e4a0b1b3c7c68bb4c3cdb992074e7d7384535ec9ccdf17fda01fa40`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae93ee014f6766fb64e501b815c0270bbaaab10ae58a849938d8d1ba91947ca0`  
		Last Modified: Thu, 12 Oct 2023 22:47:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52f6ff520763a65fb3385d8800bb4f81dbedb07f6018c4c1d6216a6484a3d66`  
		Last Modified: Thu, 12 Oct 2023 22:47:58 GMT  
		Size: 58.5 MB (58482092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0395c647e3cd72e5248e5e4a8b6b85fac92439f9b448ff827b7c20089828138d`  
		Last Modified: Thu, 12 Oct 2023 22:47:55 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62096e97f2c522845f62b133dce62e16693b11dcf1bff34c9ef1a4e681fa0e4b`  
		Last Modified: Thu, 12 Oct 2023 22:47:59 GMT  
		Size: 57.5 MB (57519324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49723393f420522b6160272a3499e4f312ad3942f58825b7f30edc4ed6023a5`  
		Last Modified: Thu, 12 Oct 2023 22:47:56 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc49fc928f33645c6a887c77ee49d428fde01b9a01f1d9e8bddeb85e4a45dc`  
		Last Modified: Thu, 12 Oct 2023 22:47:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2e9380fd730acfdcf016c38c80ed086bd3cf24b7e5cd65d11183006ad5972ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4db265f38beb3c68a4def0cae55f97cab2f4156b26470881de56c619597dda`

```dockerfile
```

-	Layers:
	-	`sha256:63abe1f026ec435c825bc099c47cd0861f5d5a965d9082fffee2027e92f06858`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 13.1 MB (13106199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7add113b7b118cf45d3f4c3c4a54f6c75cd158703f5b21d1bae1be978789d9c1`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cea62ed306c9e2a96a3d8672381cdff326fd90123d284ef4852153c0a877835b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170129736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c3aea4e3deeec5a6139350e9c1bc1f108fbfdbeb136054e77ef4669e4ae1f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf89d2c4916c1368bf3a4c6fb20a4441ec8cd4a3d57bdb015e9277b17286a03`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79120d0882796ce1ccdabc2e93d363faa3227c0773f4dccdad561aab2814f783`  
		Last Modified: Thu, 12 Oct 2023 20:59:41 GMT  
		Size: 57.5 MB (57461596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d0fac447c9eae2f0323e6dedbe3131b2f651c46d5c52ee869f8d2e028a6c0e`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6095297ac0a99514ffaa4f43e03709f12a64bce3301266c6324beabac8608835`  
		Last Modified: Thu, 12 Oct 2023 20:59:42 GMT  
		Size: 63.8 MB (63772242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e274f5c921d7f5b78607112364fe96697bb43f6d9af8e38152c9d06b8cb0c9c9`  
		Last Modified: Thu, 12 Oct 2023 20:59:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969873ad404751d35993621a462d3350aeb15f63238fc5930bd78d177d52db66`  
		Last Modified: Thu, 12 Oct 2023 20:59:39 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3bc988bea23d6f5fd6693b7be9a8da8ace0346c8150ebe4bb0ea4e75cea797cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13138887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857f42418489e182abc8b171c9c5048be74e446e9448248ec9e30443bdfb6aa9`

```dockerfile
```

-	Layers:
	-	`sha256:243dd07e28b64dcf4c34487ff9d905b095c9774305c321224a45370ccdeea70b`  
		Last Modified: Thu, 12 Oct 2023 20:59:39 GMT  
		Size: 13.1 MB (13104850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36467b2da21cc688d8b4728c2e497669d084b9212de6b061103a4c13b82a64d5`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.34`

```console
$ docker pull mysql@sha256:0ecb879cac92720d2800651c062eff258bde65072ff202e85915e1680030d8d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.34` - linux; amd64

```console
$ docker pull mysql@sha256:af31a35b4de73a35bb764a4ed0e08f9c5c8c5159359f247162ee5b5138a77036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165886094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d38554e569caa399097757542f266c34ab2713cfcfe640d32d31a9213637d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db815db7655c8466ec50b5ddf092ddeffb6bfc9e742acacc56cbee4faafa8d4`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28bf3be614c52f9ea4aad5c5a145d573e5402443949165c861ace804c28e041`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0bce98d2423e0a9382dce198e21d3830b568e9bfdac22605cdc0e33cc7d4b3`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 4.6 MB (4613109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa28f8c9e4a0b1b3c7c68bb4c3cdb992074e7d7384535ec9ccdf17fda01fa40`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae93ee014f6766fb64e501b815c0270bbaaab10ae58a849938d8d1ba91947ca0`  
		Last Modified: Thu, 12 Oct 2023 22:47:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52f6ff520763a65fb3385d8800bb4f81dbedb07f6018c4c1d6216a6484a3d66`  
		Last Modified: Thu, 12 Oct 2023 22:47:58 GMT  
		Size: 58.5 MB (58482092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0395c647e3cd72e5248e5e4a8b6b85fac92439f9b448ff827b7c20089828138d`  
		Last Modified: Thu, 12 Oct 2023 22:47:55 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62096e97f2c522845f62b133dce62e16693b11dcf1bff34c9ef1a4e681fa0e4b`  
		Last Modified: Thu, 12 Oct 2023 22:47:59 GMT  
		Size: 57.5 MB (57519324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49723393f420522b6160272a3499e4f312ad3942f58825b7f30edc4ed6023a5`  
		Last Modified: Thu, 12 Oct 2023 22:47:56 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc49fc928f33645c6a887c77ee49d428fde01b9a01f1d9e8bddeb85e4a45dc`  
		Last Modified: Thu, 12 Oct 2023 22:47:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.34` - unknown; unknown

```console
$ docker pull mysql@sha256:2e9380fd730acfdcf016c38c80ed086bd3cf24b7e5cd65d11183006ad5972ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4db265f38beb3c68a4def0cae55f97cab2f4156b26470881de56c619597dda`

```dockerfile
```

-	Layers:
	-	`sha256:63abe1f026ec435c825bc099c47cd0861f5d5a965d9082fffee2027e92f06858`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 13.1 MB (13106199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7add113b7b118cf45d3f4c3c4a54f6c75cd158703f5b21d1bae1be978789d9c1`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.34` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cea62ed306c9e2a96a3d8672381cdff326fd90123d284ef4852153c0a877835b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170129736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c3aea4e3deeec5a6139350e9c1bc1f108fbfdbeb136054e77ef4669e4ae1f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf89d2c4916c1368bf3a4c6fb20a4441ec8cd4a3d57bdb015e9277b17286a03`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79120d0882796ce1ccdabc2e93d363faa3227c0773f4dccdad561aab2814f783`  
		Last Modified: Thu, 12 Oct 2023 20:59:41 GMT  
		Size: 57.5 MB (57461596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d0fac447c9eae2f0323e6dedbe3131b2f651c46d5c52ee869f8d2e028a6c0e`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6095297ac0a99514ffaa4f43e03709f12a64bce3301266c6324beabac8608835`  
		Last Modified: Thu, 12 Oct 2023 20:59:42 GMT  
		Size: 63.8 MB (63772242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e274f5c921d7f5b78607112364fe96697bb43f6d9af8e38152c9d06b8cb0c9c9`  
		Last Modified: Thu, 12 Oct 2023 20:59:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969873ad404751d35993621a462d3350aeb15f63238fc5930bd78d177d52db66`  
		Last Modified: Thu, 12 Oct 2023 20:59:39 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.34` - unknown; unknown

```console
$ docker pull mysql@sha256:3bc988bea23d6f5fd6693b7be9a8da8ace0346c8150ebe4bb0ea4e75cea797cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13138887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857f42418489e182abc8b171c9c5048be74e446e9448248ec9e30443bdfb6aa9`

```dockerfile
```

-	Layers:
	-	`sha256:243dd07e28b64dcf4c34487ff9d905b095c9774305c321224a45370ccdeea70b`  
		Last Modified: Thu, 12 Oct 2023 20:59:39 GMT  
		Size: 13.1 MB (13104850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36467b2da21cc688d8b4728c2e497669d084b9212de6b061103a4c13b82a64d5`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.34-debian`

```console
$ docker pull mysql@sha256:2a31847951cdf92d6901ef58b4c5a9fbe75b47823d9ade1f7a4652ede7a88e2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.34-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e10fb73841ef30dcdb02e0759035f7730e5303cdc455268de219407d3fb4b846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179083456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc21a4e132a7e63c4a4eca71b3e75fbc7e965aef2b157a60a9c322e41e592795`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1debian11
# Thu, 20 Jul 2023 22:15:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf330228e741604571f4caab61f2cc172717b89147d1238d45d057fb46edb697`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafbe13d22f4d4ef6ed406ac05b335dc1371424f95a2beafc66051e6cb3974bf`  
		Last Modified: Wed, 11 Oct 2023 20:03:40 GMT  
		Size: 4.2 MB (4207542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dcfd9f33b298cff0fc2ee7fd95dbd76a738414a4269d51121ef718fbcbf87b`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 1.5 MB (1472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae14d9c3e441351e1ec5b465e6bf617e393bc4a0ad072589600a2b8ae73b37`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1086d8d2521ba8f681003c1bb0594f31379d599a291c6646085f007fe8f395a1`  
		Last Modified: Wed, 11 Oct 2023 20:03:41 GMT  
		Size: 12.5 MB (12455173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afe97457504eb7005a224c7c679006bb937483986e5365633519004752f789`  
		Last Modified: Wed, 11 Oct 2023 20:03:40 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8169ee2bdb0a81c638c5dfb7aeef3c7c5b17755771f95a889cfe4c29b26e4966`  
		Last Modified: Wed, 11 Oct 2023 20:03:41 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc0f64b1cbafeb07f2c175c0486123720ed151cdd007b251816564e4381d23`  
		Last Modified: Wed, 11 Oct 2023 20:03:47 GMT  
		Size: 129.5 MB (129519547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3994da0db6238691c6a2208c2da4b3dafb961db6ca184feedab3435104154f4d`  
		Last Modified: Wed, 11 Oct 2023 20:03:41 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae385311e5ed3100ff6111e185211d9a5749c784bd675d0ba713898acb9dafd8`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 5.4 KB (5383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ceafee559334b9217ef6cde4d657abe3fb79466a7ef1b5e6f911d185b689f6`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.34-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:2831145c9d8abb4571f51bd89b331516c37b2b0421ec56d2647082e631ce3d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95857c88929774216f8e99858617023ea09d821927280ca85a5fbfdc8a6a609a`

```dockerfile
```

-	Layers:
	-	`sha256:d6cded17556303c4d1affc0cc57b7ae8b5fdce8a01462b0b5bf4608e0e7a413d`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 3.5 MB (3450737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29553eed5402c121dca04ea081b05fbfc44820c10ddb43cc09308bc0051fd6c1`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 33.3 KB (33289 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.34-oracle`

```console
$ docker pull mysql@sha256:0ecb879cac92720d2800651c062eff258bde65072ff202e85915e1680030d8d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.34-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:af31a35b4de73a35bb764a4ed0e08f9c5c8c5159359f247162ee5b5138a77036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165886094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d38554e569caa399097757542f266c34ab2713cfcfe640d32d31a9213637d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db815db7655c8466ec50b5ddf092ddeffb6bfc9e742acacc56cbee4faafa8d4`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28bf3be614c52f9ea4aad5c5a145d573e5402443949165c861ace804c28e041`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0bce98d2423e0a9382dce198e21d3830b568e9bfdac22605cdc0e33cc7d4b3`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 4.6 MB (4613109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa28f8c9e4a0b1b3c7c68bb4c3cdb992074e7d7384535ec9ccdf17fda01fa40`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae93ee014f6766fb64e501b815c0270bbaaab10ae58a849938d8d1ba91947ca0`  
		Last Modified: Thu, 12 Oct 2023 22:47:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52f6ff520763a65fb3385d8800bb4f81dbedb07f6018c4c1d6216a6484a3d66`  
		Last Modified: Thu, 12 Oct 2023 22:47:58 GMT  
		Size: 58.5 MB (58482092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0395c647e3cd72e5248e5e4a8b6b85fac92439f9b448ff827b7c20089828138d`  
		Last Modified: Thu, 12 Oct 2023 22:47:55 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62096e97f2c522845f62b133dce62e16693b11dcf1bff34c9ef1a4e681fa0e4b`  
		Last Modified: Thu, 12 Oct 2023 22:47:59 GMT  
		Size: 57.5 MB (57519324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49723393f420522b6160272a3499e4f312ad3942f58825b7f30edc4ed6023a5`  
		Last Modified: Thu, 12 Oct 2023 22:47:56 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc49fc928f33645c6a887c77ee49d428fde01b9a01f1d9e8bddeb85e4a45dc`  
		Last Modified: Thu, 12 Oct 2023 22:47:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.34-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2e9380fd730acfdcf016c38c80ed086bd3cf24b7e5cd65d11183006ad5972ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4db265f38beb3c68a4def0cae55f97cab2f4156b26470881de56c619597dda`

```dockerfile
```

-	Layers:
	-	`sha256:63abe1f026ec435c825bc099c47cd0861f5d5a965d9082fffee2027e92f06858`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 13.1 MB (13106199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7add113b7b118cf45d3f4c3c4a54f6c75cd158703f5b21d1bae1be978789d9c1`  
		Last Modified: Thu, 12 Oct 2023 22:47:54 GMT  
		Size: 34.2 KB (34194 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.34-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cea62ed306c9e2a96a3d8672381cdff326fd90123d284ef4852153c0a877835b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170129736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c3aea4e3deeec5a6139350e9c1bc1f108fbfdbeb136054e77ef4669e4ae1f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 20 Jul 2023 22:15:44 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 20 Jul 2023 22:15:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 20 Jul 2023 22:15:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Jul 2023 22:15:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jul 2023 22:15:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 20 Jul 2023 22:15:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf89d2c4916c1368bf3a4c6fb20a4441ec8cd4a3d57bdb015e9277b17286a03`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79120d0882796ce1ccdabc2e93d363faa3227c0773f4dccdad561aab2814f783`  
		Last Modified: Thu, 12 Oct 2023 20:59:41 GMT  
		Size: 57.5 MB (57461596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d0fac447c9eae2f0323e6dedbe3131b2f651c46d5c52ee869f8d2e028a6c0e`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6095297ac0a99514ffaa4f43e03709f12a64bce3301266c6324beabac8608835`  
		Last Modified: Thu, 12 Oct 2023 20:59:42 GMT  
		Size: 63.8 MB (63772242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e274f5c921d7f5b78607112364fe96697bb43f6d9af8e38152c9d06b8cb0c9c9`  
		Last Modified: Thu, 12 Oct 2023 20:59:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969873ad404751d35993621a462d3350aeb15f63238fc5930bd78d177d52db66`  
		Last Modified: Thu, 12 Oct 2023 20:59:39 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.34-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3bc988bea23d6f5fd6693b7be9a8da8ace0346c8150ebe4bb0ea4e75cea797cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13138887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857f42418489e182abc8b171c9c5048be74e446e9448248ec9e30443bdfb6aa9`

```dockerfile
```

-	Layers:
	-	`sha256:243dd07e28b64dcf4c34487ff9d905b095c9774305c321224a45370ccdeea70b`  
		Last Modified: Thu, 12 Oct 2023 20:59:39 GMT  
		Size: 13.1 MB (13104850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36467b2da21cc688d8b4728c2e497669d084b9212de6b061103a4c13b82a64d5`  
		Last Modified: Thu, 12 Oct 2023 20:59:37 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.1`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.1` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.1` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.1` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.1-oracle`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.1.0`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.1.0` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.1.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.1.0-oracle`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.1.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.1.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:1ee299bf9eb8d2218fcb4fad666a090c92caef48ce524e6edce35f2e2d55170d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:067d20e7b9218d03c6a2ff7ee5dfa71d2e366b2adc6c4cb2f89dbc822bdedd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166125702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9aad1b5856bbb040d01e4acddaaad74b5fbd7f620dac33e4e58ecc5d0aa86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4c64fd6473f821c393644b8f402ef6456251a6350fd74773b2cbc9b956edb`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8397d67a0f45c6bc8854982af8a1ba0a70aa6ef58b2ee82aef940e37f540a0`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e9bc8aa4e96e875f612b394938110de56a7d4c3137af9ef60e21651d33bcd`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 4.6 MB (4613092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f52b272e7ff653088921a058e8a54459e1d140fdc18f084d9f15ac5e8d7111`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e8e437ee72ca9b72f031fc5015beed719cd173c743a03b0580bd66ca6bb8`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6151773824822e17d0f8ddb84b73a64546a55b58c3b59587109430c6ec523f9`  
		Last Modified: Thu, 12 Oct 2023 22:47:14 GMT  
		Size: 58.8 MB (58753526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2700e72524e088f5634e277c97646c0a9085c712ea087b90f638b8b165a2f`  
		Last Modified: Thu, 12 Oct 2023 22:47:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044404847ddeadf0364ee2dc15035714c260b351102744d36eed1594c247d62`  
		Last Modified: Thu, 12 Oct 2023 22:47:16 GMT  
		Size: 57.5 MB (57487626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142db3aeff8a7fca703978ecc71db947d286a968025cfb6322408b95ad66a22`  
		Last Modified: Thu, 12 Oct 2023 22:47:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a7798f8014a2f847a58adbd1159f3fba7a98848e90c1210fb9ebc7f3c08d0e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a6f96e38096b392c2630c624aed7cdfbfbceec24de77de441d5ada9b809520`

```dockerfile
```

-	Layers:
	-	`sha256:49c0486065be54cee6275bae91b78c01b002d2ea75e65cd6d40c28d74be98fb2`  
		Last Modified: Thu, 12 Oct 2023 22:47:11 GMT  
		Size: 13.1 MB (13107835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59409dbfd83f40a53e5ff9b7863e6183425238beaba44264e9508de308dbec63`  
		Last Modified: Thu, 12 Oct 2023 22:47:10 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8cacf9ef3db6f3e040c4ecde7f897706401d1f8330ca96862744e8b0d5781454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a00232fdc87bddbd635dad0486bf2278d705c76af20ec01f0814d0481064f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 22:18:51 GMT
ADD file:b51d9ae1b78eb07ac424bfa71c45180e09ea3a5ed18fbfbcf881fb540bf83e9a in / 
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV GOSU_VERSION=1.16
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 27 Jul 2023 22:18:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 27 Jul 2023 22:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Jul 2023 22:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jul 2023 22:18:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 27 Jul 2023 22:18:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:89ec84aa94fe6a62fb4e9f51aced09dea3cc4d7979c9f0ebd6b5bd4fd729e04e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 43.7 MB (43669807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047d0a85fcf9107bca7c22f98448ccf140ceed34e3b161beeb4904344032ab7`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981666a88bb712c4283e2a0a14f7ab9b27ff60bfc893fba647a0dbfaa93f6d0`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9dbd754432215cdd312410444c1c3859b4196dc771c13eba5a56682bef8dc`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 4.3 MB (4303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed90386e32a0124cf2dbca9de0ca31cd5f666b339a7e9a63dae44ed117e587`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b36981941b7e06e20d54a95dc6d483b22da2cb1e1fe68e9a77bcbcd2f55696c`  
		Last Modified: Thu, 12 Oct 2023 20:57:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca996c23fc53d3fd7658d98952a4d481ae66e74585e2b72c55f961bf54455736`  
		Last Modified: Thu, 12 Oct 2023 20:57:57 GMT  
		Size: 57.7 MB (57701851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15050e9043e65433ddefd92b793734e91755006d5f756c6a9259998e9ccf916a`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfc97ced27490a7dd8db645fba5623698b5a933cb2359aedacf99e2dd74d54`  
		Last Modified: Thu, 12 Oct 2023 20:57:58 GMT  
		Size: 63.8 MB (63773775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435e3bf4d77af270e3b5245b5aa6234fcd3bb791ed57db4641d7ef99b33bf18`  
		Last Modified: Thu, 12 Oct 2023 20:57:55 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:33f7834b9a596feb3b7660924e45d3886bc1908da500f449c853ace58e7ef70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31013d6e714b5c7d6108fc3965658f4e7d97b6c8aa096f02b8230c4e1ebf99ae`

```dockerfile
```

-	Layers:
	-	`sha256:564dbabf3309a798678bcee0a9ac7f451cacb91050175a2e98f9313a605ae7cd`  
		Last Modified: Thu, 12 Oct 2023 20:57:54 GMT  
		Size: 13.1 MB (13106498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18613fc7c61e609bc95ef7402649a9c574fb26d032c9df3aa4e7b3f9b86b70e4`  
		Last Modified: Thu, 12 Oct 2023 20:57:52 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json
