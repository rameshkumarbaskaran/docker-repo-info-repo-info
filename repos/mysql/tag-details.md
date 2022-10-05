<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.39`](#mysql5739)
-	[`mysql:5.7.39-debian`](#mysql5739-debian)
-	[`mysql:5.7.39-oracle`](#mysql5739-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.30`](#mysql8030)
-	[`mysql:8.0.30-debian`](#mysql8030-debian)
-	[`mysql:8.0.30-oracle`](#mysql8030-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:94fe67a04001e9841f68f114c8e9b5231c1d012e6b00d3b8ade42c0c5e239a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:a0a2c8b6beabcbe472a38806d5727416ef1135099b19936a755c61826f57d2ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129375677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa803eda0f25baa8886e951f76473a28bec9938508849bc70a0ef340c0077956`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Sep 2022 18:21:00 GMT
ADD file:bc2c7ba728e9e4bfc9aa5e6072db4cbab3cadbd76aff485b6afd233dcdfbdb1e in / 
# Thu, 22 Sep 2022 18:21:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 18:44:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 22 Sep 2022 18:44:16 GMT
ENV GOSU_VERSION=1.14
# Thu, 22 Sep 2022 18:44:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Sep 2022 18:44:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 22 Sep 2022 18:44:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 22 Sep 2022 18:45:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 22 Sep 2022 18:45:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Thu, 22 Sep 2022 18:45:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 22 Sep 2022 18:45:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Sep 2022 18:45:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Thu, 22 Sep 2022 18:45:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Sep 2022 18:45:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 18:45:25 GMT
EXPOSE 3306 33060
# Thu, 22 Sep 2022 18:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2a00260331c858dbb0d8dae185769162dbb3e7cb3342d52798d837e7a156c45`  
		Last Modified: Thu, 22 Sep 2022 18:21:50 GMT  
		Size: 49.8 MB (49796793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8167f2fcbe07badb74ea8da139081ca2f01a12334d28152b4719e79c187c2b`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32454e9854ca917e071559d6827e5974ad1780ae6860a9defd58ead4f7ade100`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 930.2 KB (930217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473e2917b0d5ebef2e46b395bb9e099d71855d49be3d7027154173fd600ef8bf`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 4.5 MB (4538328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173f8104ec8168935afa8185ed6fc18e2ff300bdc68997146fcd9082506cd87`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e218351f9ae95fd888e7c503ba27fec3a3beda4ae178ba3d9a4849acdb6f88`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9e1a82359ae7532637d28d4f7665ca5675e3d48320a58681553570fabb385c`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 25.5 MB (25504750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602a3ea2ce74ed5feb8d1780da2760597305b5671d5106741152c21f779bec7`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ea9927039c38bcb87da982abbad5c24e3de05f3128d09b95156b6e285d326`  
		Last Modified: Thu, 22 Sep 2022 18:46:18 GMT  
		Size: 48.6 MB (48595906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb1b236c7fce4f6da7150bc2320d1031c0d07c508139a0b18c792d60076984f`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad62bd72a757206fb91b920c05205375dad064c33dc55f0fd30827df92e4ec`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:f1c5bbefe1aaff6c816fb7193391668521cd0eb3587560fd15faeb9b226b77a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e60db24aaf5c748b3e5f3320c843282e6ebd87039faa188e4bf986dd574e54d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162534124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abe8c2c2f9465506e659685eb6012bed544ebb0a3ce91b9bd1c6c8ee63e2d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:22:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 05 Oct 2022 04:22:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:42 GMT
ENV GOSU_VERSION=1.14
# Wed, 05 Oct 2022 04:22:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 04:22:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 04:22:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 05 Oct 2022 04:22:59 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 05 Oct 2022 04:22:59 GMT
ENV MYSQL_VERSION=5.7.39-1debian10
# Wed, 05 Oct 2022 04:23:00 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 05 Oct 2022 04:23:20 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 05 Oct 2022 04:23:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Oct 2022 04:23:21 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:23:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 04:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 04:23:21 GMT
EXPOSE 3306 33060
# Wed, 05 Oct 2022 04:23:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a11d1b00d26182c3e9edb027d075aab8c6529517f09b58b9474b42e96b7282`  
		Last Modified: Wed, 05 Oct 2022 04:24:27 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65869aed91d26fee82355255ac43a74ad1b1efab8c4f9733cb985f5a65a215bc`  
		Last Modified: Wed, 05 Oct 2022 04:24:25 GMT  
		Size: 4.2 MB (4179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b594fff16bcffe32ae29c2e6ef1d64e50b63c956002ed96f4aeb670ae2c9d15`  
		Last Modified: Wed, 05 Oct 2022 04:24:25 GMT  
		Size: 1.4 MB (1386660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e1e42bcc85e082d51a8bdfde663ae17168e85c0773a7f9d7ffbacfc03abd4`  
		Last Modified: Wed, 05 Oct 2022 04:24:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ecc9da4c857053937cf0e8c8f6b93d1e20a238dc8986301597f014a58607ef`  
		Last Modified: Wed, 05 Oct 2022 04:24:28 GMT  
		Size: 14.1 MB (14086928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed6254a5eabd760fd83f3fe87470ef4c5d74e38809164e20d82ccea7403ad82`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0225260858f5bec45902e81dc388af9707d656b2ac6d16a89c0195636bbd76c`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5200d9e491caac48656cd7f43bfb68ddeb2a210567b8ef6f7c4399df3b3332`  
		Last Modified: Wed, 05 Oct 2022 04:24:38 GMT  
		Size: 115.7 MB (115733089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d6ad7fb947346c41003be489f740c140d6deb361bcba625733a8971f79fe2a`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013f5c86a18f9fa9483bb890aa37484141e557cab4c119fff68c34da2e22e5d8`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:94fe67a04001e9841f68f114c8e9b5231c1d012e6b00d3b8ade42c0c5e239a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0a2c8b6beabcbe472a38806d5727416ef1135099b19936a755c61826f57d2ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129375677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa803eda0f25baa8886e951f76473a28bec9938508849bc70a0ef340c0077956`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Sep 2022 18:21:00 GMT
ADD file:bc2c7ba728e9e4bfc9aa5e6072db4cbab3cadbd76aff485b6afd233dcdfbdb1e in / 
# Thu, 22 Sep 2022 18:21:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 18:44:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 22 Sep 2022 18:44:16 GMT
ENV GOSU_VERSION=1.14
# Thu, 22 Sep 2022 18:44:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Sep 2022 18:44:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 22 Sep 2022 18:44:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 22 Sep 2022 18:45:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 22 Sep 2022 18:45:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Thu, 22 Sep 2022 18:45:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 22 Sep 2022 18:45:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Sep 2022 18:45:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Thu, 22 Sep 2022 18:45:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Sep 2022 18:45:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 18:45:25 GMT
EXPOSE 3306 33060
# Thu, 22 Sep 2022 18:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2a00260331c858dbb0d8dae185769162dbb3e7cb3342d52798d837e7a156c45`  
		Last Modified: Thu, 22 Sep 2022 18:21:50 GMT  
		Size: 49.8 MB (49796793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8167f2fcbe07badb74ea8da139081ca2f01a12334d28152b4719e79c187c2b`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32454e9854ca917e071559d6827e5974ad1780ae6860a9defd58ead4f7ade100`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 930.2 KB (930217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473e2917b0d5ebef2e46b395bb9e099d71855d49be3d7027154173fd600ef8bf`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 4.5 MB (4538328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173f8104ec8168935afa8185ed6fc18e2ff300bdc68997146fcd9082506cd87`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e218351f9ae95fd888e7c503ba27fec3a3beda4ae178ba3d9a4849acdb6f88`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9e1a82359ae7532637d28d4f7665ca5675e3d48320a58681553570fabb385c`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 25.5 MB (25504750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602a3ea2ce74ed5feb8d1780da2760597305b5671d5106741152c21f779bec7`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ea9927039c38bcb87da982abbad5c24e3de05f3128d09b95156b6e285d326`  
		Last Modified: Thu, 22 Sep 2022 18:46:18 GMT  
		Size: 48.6 MB (48595906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb1b236c7fce4f6da7150bc2320d1031c0d07c508139a0b18c792d60076984f`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad62bd72a757206fb91b920c05205375dad064c33dc55f0fd30827df92e4ec`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:94fe67a04001e9841f68f114c8e9b5231c1d012e6b00d3b8ade42c0c5e239a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:a0a2c8b6beabcbe472a38806d5727416ef1135099b19936a755c61826f57d2ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129375677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa803eda0f25baa8886e951f76473a28bec9938508849bc70a0ef340c0077956`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Sep 2022 18:21:00 GMT
ADD file:bc2c7ba728e9e4bfc9aa5e6072db4cbab3cadbd76aff485b6afd233dcdfbdb1e in / 
# Thu, 22 Sep 2022 18:21:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 18:44:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 22 Sep 2022 18:44:16 GMT
ENV GOSU_VERSION=1.14
# Thu, 22 Sep 2022 18:44:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Sep 2022 18:44:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 22 Sep 2022 18:44:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 22 Sep 2022 18:45:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 22 Sep 2022 18:45:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Thu, 22 Sep 2022 18:45:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 22 Sep 2022 18:45:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Sep 2022 18:45:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Thu, 22 Sep 2022 18:45:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Sep 2022 18:45:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 18:45:25 GMT
EXPOSE 3306 33060
# Thu, 22 Sep 2022 18:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2a00260331c858dbb0d8dae185769162dbb3e7cb3342d52798d837e7a156c45`  
		Last Modified: Thu, 22 Sep 2022 18:21:50 GMT  
		Size: 49.8 MB (49796793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8167f2fcbe07badb74ea8da139081ca2f01a12334d28152b4719e79c187c2b`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32454e9854ca917e071559d6827e5974ad1780ae6860a9defd58ead4f7ade100`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 930.2 KB (930217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473e2917b0d5ebef2e46b395bb9e099d71855d49be3d7027154173fd600ef8bf`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 4.5 MB (4538328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173f8104ec8168935afa8185ed6fc18e2ff300bdc68997146fcd9082506cd87`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e218351f9ae95fd888e7c503ba27fec3a3beda4ae178ba3d9a4849acdb6f88`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9e1a82359ae7532637d28d4f7665ca5675e3d48320a58681553570fabb385c`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 25.5 MB (25504750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602a3ea2ce74ed5feb8d1780da2760597305b5671d5106741152c21f779bec7`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ea9927039c38bcb87da982abbad5c24e3de05f3128d09b95156b6e285d326`  
		Last Modified: Thu, 22 Sep 2022 18:46:18 GMT  
		Size: 48.6 MB (48595906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb1b236c7fce4f6da7150bc2320d1031c0d07c508139a0b18c792d60076984f`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad62bd72a757206fb91b920c05205375dad064c33dc55f0fd30827df92e4ec`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:f1c5bbefe1aaff6c816fb7193391668521cd0eb3587560fd15faeb9b226b77a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e60db24aaf5c748b3e5f3320c843282e6ebd87039faa188e4bf986dd574e54d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162534124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abe8c2c2f9465506e659685eb6012bed544ebb0a3ce91b9bd1c6c8ee63e2d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:22:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 05 Oct 2022 04:22:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:42 GMT
ENV GOSU_VERSION=1.14
# Wed, 05 Oct 2022 04:22:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 04:22:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 04:22:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 05 Oct 2022 04:22:59 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 05 Oct 2022 04:22:59 GMT
ENV MYSQL_VERSION=5.7.39-1debian10
# Wed, 05 Oct 2022 04:23:00 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 05 Oct 2022 04:23:20 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 05 Oct 2022 04:23:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Oct 2022 04:23:21 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:23:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 04:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 04:23:21 GMT
EXPOSE 3306 33060
# Wed, 05 Oct 2022 04:23:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a11d1b00d26182c3e9edb027d075aab8c6529517f09b58b9474b42e96b7282`  
		Last Modified: Wed, 05 Oct 2022 04:24:27 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65869aed91d26fee82355255ac43a74ad1b1efab8c4f9733cb985f5a65a215bc`  
		Last Modified: Wed, 05 Oct 2022 04:24:25 GMT  
		Size: 4.2 MB (4179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b594fff16bcffe32ae29c2e6ef1d64e50b63c956002ed96f4aeb670ae2c9d15`  
		Last Modified: Wed, 05 Oct 2022 04:24:25 GMT  
		Size: 1.4 MB (1386660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e1e42bcc85e082d51a8bdfde663ae17168e85c0773a7f9d7ffbacfc03abd4`  
		Last Modified: Wed, 05 Oct 2022 04:24:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ecc9da4c857053937cf0e8c8f6b93d1e20a238dc8986301597f014a58607ef`  
		Last Modified: Wed, 05 Oct 2022 04:24:28 GMT  
		Size: 14.1 MB (14086928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed6254a5eabd760fd83f3fe87470ef4c5d74e38809164e20d82ccea7403ad82`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0225260858f5bec45902e81dc388af9707d656b2ac6d16a89c0195636bbd76c`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5200d9e491caac48656cd7f43bfb68ddeb2a210567b8ef6f7c4399df3b3332`  
		Last Modified: Wed, 05 Oct 2022 04:24:38 GMT  
		Size: 115.7 MB (115733089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d6ad7fb947346c41003be489f740c140d6deb361bcba625733a8971f79fe2a`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013f5c86a18f9fa9483bb890aa37484141e557cab4c119fff68c34da2e22e5d8`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:94fe67a04001e9841f68f114c8e9b5231c1d012e6b00d3b8ade42c0c5e239a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0a2c8b6beabcbe472a38806d5727416ef1135099b19936a755c61826f57d2ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129375677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa803eda0f25baa8886e951f76473a28bec9938508849bc70a0ef340c0077956`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Sep 2022 18:21:00 GMT
ADD file:bc2c7ba728e9e4bfc9aa5e6072db4cbab3cadbd76aff485b6afd233dcdfbdb1e in / 
# Thu, 22 Sep 2022 18:21:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 18:44:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 22 Sep 2022 18:44:16 GMT
ENV GOSU_VERSION=1.14
# Thu, 22 Sep 2022 18:44:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Sep 2022 18:44:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 22 Sep 2022 18:44:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 22 Sep 2022 18:45:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 22 Sep 2022 18:45:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Thu, 22 Sep 2022 18:45:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 22 Sep 2022 18:45:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Sep 2022 18:45:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Thu, 22 Sep 2022 18:45:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Sep 2022 18:45:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 18:45:25 GMT
EXPOSE 3306 33060
# Thu, 22 Sep 2022 18:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2a00260331c858dbb0d8dae185769162dbb3e7cb3342d52798d837e7a156c45`  
		Last Modified: Thu, 22 Sep 2022 18:21:50 GMT  
		Size: 49.8 MB (49796793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8167f2fcbe07badb74ea8da139081ca2f01a12334d28152b4719e79c187c2b`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32454e9854ca917e071559d6827e5974ad1780ae6860a9defd58ead4f7ade100`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 930.2 KB (930217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473e2917b0d5ebef2e46b395bb9e099d71855d49be3d7027154173fd600ef8bf`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 4.5 MB (4538328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173f8104ec8168935afa8185ed6fc18e2ff300bdc68997146fcd9082506cd87`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e218351f9ae95fd888e7c503ba27fec3a3beda4ae178ba3d9a4849acdb6f88`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9e1a82359ae7532637d28d4f7665ca5675e3d48320a58681553570fabb385c`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 25.5 MB (25504750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602a3ea2ce74ed5feb8d1780da2760597305b5671d5106741152c21f779bec7`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ea9927039c38bcb87da982abbad5c24e3de05f3128d09b95156b6e285d326`  
		Last Modified: Thu, 22 Sep 2022 18:46:18 GMT  
		Size: 48.6 MB (48595906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb1b236c7fce4f6da7150bc2320d1031c0d07c508139a0b18c792d60076984f`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad62bd72a757206fb91b920c05205375dad064c33dc55f0fd30827df92e4ec`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.39`

```console
$ docker pull mysql@sha256:94fe67a04001e9841f68f114c8e9b5231c1d012e6b00d3b8ade42c0c5e239a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.39` - linux; amd64

```console
$ docker pull mysql@sha256:a0a2c8b6beabcbe472a38806d5727416ef1135099b19936a755c61826f57d2ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129375677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa803eda0f25baa8886e951f76473a28bec9938508849bc70a0ef340c0077956`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Sep 2022 18:21:00 GMT
ADD file:bc2c7ba728e9e4bfc9aa5e6072db4cbab3cadbd76aff485b6afd233dcdfbdb1e in / 
# Thu, 22 Sep 2022 18:21:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 18:44:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 22 Sep 2022 18:44:16 GMT
ENV GOSU_VERSION=1.14
# Thu, 22 Sep 2022 18:44:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Sep 2022 18:44:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 22 Sep 2022 18:44:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 22 Sep 2022 18:45:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 22 Sep 2022 18:45:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Thu, 22 Sep 2022 18:45:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 22 Sep 2022 18:45:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Sep 2022 18:45:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Thu, 22 Sep 2022 18:45:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Sep 2022 18:45:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 18:45:25 GMT
EXPOSE 3306 33060
# Thu, 22 Sep 2022 18:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2a00260331c858dbb0d8dae185769162dbb3e7cb3342d52798d837e7a156c45`  
		Last Modified: Thu, 22 Sep 2022 18:21:50 GMT  
		Size: 49.8 MB (49796793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8167f2fcbe07badb74ea8da139081ca2f01a12334d28152b4719e79c187c2b`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32454e9854ca917e071559d6827e5974ad1780ae6860a9defd58ead4f7ade100`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 930.2 KB (930217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473e2917b0d5ebef2e46b395bb9e099d71855d49be3d7027154173fd600ef8bf`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 4.5 MB (4538328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173f8104ec8168935afa8185ed6fc18e2ff300bdc68997146fcd9082506cd87`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e218351f9ae95fd888e7c503ba27fec3a3beda4ae178ba3d9a4849acdb6f88`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9e1a82359ae7532637d28d4f7665ca5675e3d48320a58681553570fabb385c`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 25.5 MB (25504750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602a3ea2ce74ed5feb8d1780da2760597305b5671d5106741152c21f779bec7`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ea9927039c38bcb87da982abbad5c24e3de05f3128d09b95156b6e285d326`  
		Last Modified: Thu, 22 Sep 2022 18:46:18 GMT  
		Size: 48.6 MB (48595906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb1b236c7fce4f6da7150bc2320d1031c0d07c508139a0b18c792d60076984f`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad62bd72a757206fb91b920c05205375dad064c33dc55f0fd30827df92e4ec`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.39-debian`

```console
$ docker pull mysql@sha256:f1c5bbefe1aaff6c816fb7193391668521cd0eb3587560fd15faeb9b226b77a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.39-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e60db24aaf5c748b3e5f3320c843282e6ebd87039faa188e4bf986dd574e54d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162534124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abe8c2c2f9465506e659685eb6012bed544ebb0a3ce91b9bd1c6c8ee63e2d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:22:36 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 05 Oct 2022 04:22:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:42 GMT
ENV GOSU_VERSION=1.14
# Wed, 05 Oct 2022 04:22:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 04:22:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 04:22:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 05 Oct 2022 04:22:59 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 05 Oct 2022 04:22:59 GMT
ENV MYSQL_VERSION=5.7.39-1debian10
# Wed, 05 Oct 2022 04:23:00 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 05 Oct 2022 04:23:20 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 05 Oct 2022 04:23:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Oct 2022 04:23:21 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:23:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 04:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 04:23:21 GMT
EXPOSE 3306 33060
# Wed, 05 Oct 2022 04:23:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a11d1b00d26182c3e9edb027d075aab8c6529517f09b58b9474b42e96b7282`  
		Last Modified: Wed, 05 Oct 2022 04:24:27 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65869aed91d26fee82355255ac43a74ad1b1efab8c4f9733cb985f5a65a215bc`  
		Last Modified: Wed, 05 Oct 2022 04:24:25 GMT  
		Size: 4.2 MB (4179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b594fff16bcffe32ae29c2e6ef1d64e50b63c956002ed96f4aeb670ae2c9d15`  
		Last Modified: Wed, 05 Oct 2022 04:24:25 GMT  
		Size: 1.4 MB (1386660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e1e42bcc85e082d51a8bdfde663ae17168e85c0773a7f9d7ffbacfc03abd4`  
		Last Modified: Wed, 05 Oct 2022 04:24:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ecc9da4c857053937cf0e8c8f6b93d1e20a238dc8986301597f014a58607ef`  
		Last Modified: Wed, 05 Oct 2022 04:24:28 GMT  
		Size: 14.1 MB (14086928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed6254a5eabd760fd83f3fe87470ef4c5d74e38809164e20d82ccea7403ad82`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0225260858f5bec45902e81dc388af9707d656b2ac6d16a89c0195636bbd76c`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5200d9e491caac48656cd7f43bfb68ddeb2a210567b8ef6f7c4399df3b3332`  
		Last Modified: Wed, 05 Oct 2022 04:24:38 GMT  
		Size: 115.7 MB (115733089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d6ad7fb947346c41003be489f740c140d6deb361bcba625733a8971f79fe2a`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013f5c86a18f9fa9483bb890aa37484141e557cab4c119fff68c34da2e22e5d8`  
		Last Modified: Wed, 05 Oct 2022 04:24:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.39-oracle`

```console
$ docker pull mysql@sha256:94fe67a04001e9841f68f114c8e9b5231c1d012e6b00d3b8ade42c0c5e239a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.39-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0a2c8b6beabcbe472a38806d5727416ef1135099b19936a755c61826f57d2ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129375677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa803eda0f25baa8886e951f76473a28bec9938508849bc70a0ef340c0077956`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Sep 2022 18:21:00 GMT
ADD file:bc2c7ba728e9e4bfc9aa5e6072db4cbab3cadbd76aff485b6afd233dcdfbdb1e in / 
# Thu, 22 Sep 2022 18:21:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 18:44:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 22 Sep 2022 18:44:16 GMT
ENV GOSU_VERSION=1.14
# Thu, 22 Sep 2022 18:44:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Sep 2022 18:44:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 22 Sep 2022 18:44:41 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Thu, 22 Sep 2022 18:44:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 22 Sep 2022 18:44:59 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 22 Sep 2022 18:45:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 22 Sep 2022 18:45:00 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Thu, 22 Sep 2022 18:45:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 22 Sep 2022 18:45:24 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Sep 2022 18:45:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Thu, 22 Sep 2022 18:45:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Sep 2022 18:45:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 18:45:25 GMT
EXPOSE 3306 33060
# Thu, 22 Sep 2022 18:45:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2a00260331c858dbb0d8dae185769162dbb3e7cb3342d52798d837e7a156c45`  
		Last Modified: Thu, 22 Sep 2022 18:21:50 GMT  
		Size: 49.8 MB (49796793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8167f2fcbe07badb74ea8da139081ca2f01a12334d28152b4719e79c187c2b`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32454e9854ca917e071559d6827e5974ad1780ae6860a9defd58ead4f7ade100`  
		Last Modified: Thu, 22 Sep 2022 18:46:13 GMT  
		Size: 930.2 KB (930217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473e2917b0d5ebef2e46b395bb9e099d71855d49be3d7027154173fd600ef8bf`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 4.5 MB (4538328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173f8104ec8168935afa8185ed6fc18e2ff300bdc68997146fcd9082506cd87`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e218351f9ae95fd888e7c503ba27fec3a3beda4ae178ba3d9a4849acdb6f88`  
		Last Modified: Thu, 22 Sep 2022 18:46:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9e1a82359ae7532637d28d4f7665ca5675e3d48320a58681553570fabb385c`  
		Last Modified: Thu, 22 Sep 2022 18:46:12 GMT  
		Size: 25.5 MB (25504750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602a3ea2ce74ed5feb8d1780da2760597305b5671d5106741152c21f779bec7`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ea9927039c38bcb87da982abbad5c24e3de05f3128d09b95156b6e285d326`  
		Last Modified: Thu, 22 Sep 2022 18:46:18 GMT  
		Size: 48.6 MB (48595906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb1b236c7fce4f6da7150bc2320d1031c0d07c508139a0b18c792d60076984f`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad62bd72a757206fb91b920c05205375dad064c33dc55f0fd30827df92e4ec`  
		Last Modified: Thu, 22 Sep 2022 18:46:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:b9532b1edea72b6cee12d9f5a78547bd3812ea5db842566e17f8b33291ed2921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:8c43b0fffec41abcb01d825b8d1a3bf49f28cca94bb350943c1686c633345fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133891432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fcfca0776df8e192d1647da2866237fbd9f8e875fb496e4ca887369b2dd995`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:45:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:45:02 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:45:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:45:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:45:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:45:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:45:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:46:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:46:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:46:30 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:46:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:46:31 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7627573fa82aa6fa625675120ab2da659d056afc38872fba26aaa03bfcc97443`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b358d779638ca172a6cd9fac8926779ec83f0cc1ec5f5e598a842659b95be`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 928.8 KB (928830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753aff4b95947bb49e47f9adc6169f5b718b649b13e0aa8dd3f8aeb32d28e1`  
		Last Modified: Wed, 14 Sep 2022 21:47:11 GMT  
		Size: 4.6 MB (4606953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa3bee53f45d4b5f13b1680267324c732f70099f5aeb6e2cea0f23fd100657`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5227e0d612cc3cbdbadda9082d35821013b94be48915f0e225ec362338f3893`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4368b19837a5d3b7ae0549f97f90ef0cde786eac09c2082bdc9400645727a`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 47.7 MB (47733942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26212810c32af8d7ce6567aa5e4eff976d8c236df93ea2403207ba13790c191`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803d4215f950ffbe84f925527006ced4d892ad0bb98a5839f83b0ad1011cc3b`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 40.0 MB (40021785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5358a7f7d072df12dc5e2276f7cb10cb069c1f606b23308e2693ad3da9f0528`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435e8908cd690ccf82ed2d0567095013ef79686b3b650f59e699694a0735a311`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d8ceb97140e661a4ef94a1f8960442f009c70302f2212762b3f8c5ba697b6759
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142633685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e229524f286e653111cb9d028bf1ba4c3490742c8cd18c84af22538f0e68575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:57:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:57:47 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:57:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:58:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:58:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:58:20 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:58:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:58:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:58:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:58:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:58:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:59:25 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:59:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:59:28 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:59:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:59:30 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c023923f622f4a64d561898afe3142f49c5ed26cb2f27f22d6e8877ba87092`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af22db8f5e1863d738d7c6fbc4f3e66ce8192417c4c59ccc89660f88f75826f0`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 857.1 KB (857150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c3a923aa34c4af8180e555667ca6db39a920b02de2154c873486de062b6bd`  
		Last Modified: Wed, 14 Sep 2022 22:00:05 GMT  
		Size: 4.4 MB (4433575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830d9608cd584343e51f4b7e372689596389d335cf96fa70d4ef31a2cb3c8337`  
		Last Modified: Wed, 14 Sep 2022 22:00:03 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914654f8cd5683bc7bf3f7025aa7fd9b5fe827c2cf69f81d1ba90b930a25090`  
		Last Modified: Wed, 14 Sep 2022 22:00:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a35992845d8a14e6a802651fb7b44463b3e032e0662761af253d27a2c31054`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 53.8 MB (53817808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4540528c83e950b7d415eb645620fd2f038d5e74b6cec9af48f0c2d352223`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec168f6cfd418dda7322375cdd92a8218f3b7ea07bc7abe882ae7d9d960cf`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 44.1 MB (44105600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742f8a782c5d9f0a1ad0052513356440cad2abe1c334cfac66792f7fddd691a`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e5cc37f4b17fb6bbb5c7c41abeb9ca6f2967b2e0755d65f34d85918eb49963`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:c00749f00b317206048b8eaf304ded3941ecaf452b73a8e178b8ea2d1fc29342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:12477b35d174c1a410da24a05c4884693836e2a863521aa339a1298ce48b8369
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157889330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e66721c05dacebba2911adc611de5a71b95458b5a7208fb961aa3051b5eec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:21:45 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 05 Oct 2022 04:21:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:21:51 GMT
ENV GOSU_VERSION=1.14
# Wed, 05 Oct 2022 04:22:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 04:22:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 04:22:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:07 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 05 Oct 2022 04:22:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 05 Oct 2022 04:22:08 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Wed, 05 Oct 2022 04:22:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 05 Oct 2022 04:22:23 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 05 Oct 2022 04:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Oct 2022 04:22:24 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 05 Oct 2022 04:22:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 04:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 04:22:25 GMT
EXPOSE 3306 33060
# Wed, 05 Oct 2022 04:22:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498ba1a3ae2dfa82359e0fb959af536134a1360d33dfa87638e409b70b3fa3`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c224eff0af51a4254bf410ca8f6cab7044171639fc6e7b29cd55248bb609d02`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 4.4 MB (4414808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdd40c1260704addfdb3a21bf71ae5c14567100f98acd4d8dfec303294e1c5f`  
		Last Modified: Wed, 05 Oct 2022 04:23:50 GMT  
		Size: 1.4 MB (1418452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c3ece0305cbf295220adfdacf8c9e9fdf5de35ea07e505913ea4ee6e1f4f74`  
		Last Modified: Wed, 05 Oct 2022 04:23:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a10286651685e256e36f218063406728987d0f36c285adf41d41f8665661b74`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 12.7 MB (12661783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a34b42ee331888b70b38f6c96cacce54fe2bb4cf6e2ccefdd7add2144d5a3e`  
		Last Modified: Wed, 05 Oct 2022 04:23:49 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1363e6677cacb6f7960a756d9b4c0aa8d4c8ec02869cb4a6d9159faa60ecba4`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1110efce5dd0e631830f85c1a0c25efbba11b2e55314c04bb4fc0f97a30fdfc`  
		Last Modified: Wed, 05 Oct 2022 04:24:04 GMT  
		Size: 108.0 MB (107963159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fda2bd249a81a6cde8a8959a44831ac82aa8e5ecf3e1d508cf07ae87454330`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89080d4312c49459448781df923db9f843c0f978fc5100842de22d34ce9b142`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d74113edbbb66aa319322589f5e5f54f3ac373cc17fb9a2fdd5c3fe2f877345`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:b9532b1edea72b6cee12d9f5a78547bd3812ea5db842566e17f8b33291ed2921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8c43b0fffec41abcb01d825b8d1a3bf49f28cca94bb350943c1686c633345fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133891432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fcfca0776df8e192d1647da2866237fbd9f8e875fb496e4ca887369b2dd995`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:45:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:45:02 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:45:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:45:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:45:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:45:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:45:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:46:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:46:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:46:30 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:46:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:46:31 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7627573fa82aa6fa625675120ab2da659d056afc38872fba26aaa03bfcc97443`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b358d779638ca172a6cd9fac8926779ec83f0cc1ec5f5e598a842659b95be`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 928.8 KB (928830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753aff4b95947bb49e47f9adc6169f5b718b649b13e0aa8dd3f8aeb32d28e1`  
		Last Modified: Wed, 14 Sep 2022 21:47:11 GMT  
		Size: 4.6 MB (4606953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa3bee53f45d4b5f13b1680267324c732f70099f5aeb6e2cea0f23fd100657`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5227e0d612cc3cbdbadda9082d35821013b94be48915f0e225ec362338f3893`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4368b19837a5d3b7ae0549f97f90ef0cde786eac09c2082bdc9400645727a`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 47.7 MB (47733942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26212810c32af8d7ce6567aa5e4eff976d8c236df93ea2403207ba13790c191`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803d4215f950ffbe84f925527006ced4d892ad0bb98a5839f83b0ad1011cc3b`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 40.0 MB (40021785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5358a7f7d072df12dc5e2276f7cb10cb069c1f606b23308e2693ad3da9f0528`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435e8908cd690ccf82ed2d0567095013ef79686b3b650f59e699694a0735a311`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d8ceb97140e661a4ef94a1f8960442f009c70302f2212762b3f8c5ba697b6759
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142633685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e229524f286e653111cb9d028bf1ba4c3490742c8cd18c84af22538f0e68575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:57:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:57:47 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:57:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:58:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:58:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:58:20 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:58:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:58:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:58:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:58:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:58:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:59:25 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:59:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:59:28 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:59:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:59:30 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c023923f622f4a64d561898afe3142f49c5ed26cb2f27f22d6e8877ba87092`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af22db8f5e1863d738d7c6fbc4f3e66ce8192417c4c59ccc89660f88f75826f0`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 857.1 KB (857150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c3a923aa34c4af8180e555667ca6db39a920b02de2154c873486de062b6bd`  
		Last Modified: Wed, 14 Sep 2022 22:00:05 GMT  
		Size: 4.4 MB (4433575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830d9608cd584343e51f4b7e372689596389d335cf96fa70d4ef31a2cb3c8337`  
		Last Modified: Wed, 14 Sep 2022 22:00:03 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914654f8cd5683bc7bf3f7025aa7fd9b5fe827c2cf69f81d1ba90b930a25090`  
		Last Modified: Wed, 14 Sep 2022 22:00:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a35992845d8a14e6a802651fb7b44463b3e032e0662761af253d27a2c31054`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 53.8 MB (53817808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4540528c83e950b7d415eb645620fd2f038d5e74b6cec9af48f0c2d352223`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec168f6cfd418dda7322375cdd92a8218f3b7ea07bc7abe882ae7d9d960cf`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 44.1 MB (44105600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742f8a782c5d9f0a1ad0052513356440cad2abe1c334cfac66792f7fddd691a`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e5cc37f4b17fb6bbb5c7c41abeb9ca6f2967b2e0755d65f34d85918eb49963`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:b9532b1edea72b6cee12d9f5a78547bd3812ea5db842566e17f8b33291ed2921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:8c43b0fffec41abcb01d825b8d1a3bf49f28cca94bb350943c1686c633345fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133891432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fcfca0776df8e192d1647da2866237fbd9f8e875fb496e4ca887369b2dd995`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:45:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:45:02 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:45:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:45:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:45:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:45:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:45:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:46:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:46:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:46:30 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:46:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:46:31 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7627573fa82aa6fa625675120ab2da659d056afc38872fba26aaa03bfcc97443`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b358d779638ca172a6cd9fac8926779ec83f0cc1ec5f5e598a842659b95be`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 928.8 KB (928830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753aff4b95947bb49e47f9adc6169f5b718b649b13e0aa8dd3f8aeb32d28e1`  
		Last Modified: Wed, 14 Sep 2022 21:47:11 GMT  
		Size: 4.6 MB (4606953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa3bee53f45d4b5f13b1680267324c732f70099f5aeb6e2cea0f23fd100657`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5227e0d612cc3cbdbadda9082d35821013b94be48915f0e225ec362338f3893`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4368b19837a5d3b7ae0549f97f90ef0cde786eac09c2082bdc9400645727a`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 47.7 MB (47733942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26212810c32af8d7ce6567aa5e4eff976d8c236df93ea2403207ba13790c191`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803d4215f950ffbe84f925527006ced4d892ad0bb98a5839f83b0ad1011cc3b`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 40.0 MB (40021785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5358a7f7d072df12dc5e2276f7cb10cb069c1f606b23308e2693ad3da9f0528`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435e8908cd690ccf82ed2d0567095013ef79686b3b650f59e699694a0735a311`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d8ceb97140e661a4ef94a1f8960442f009c70302f2212762b3f8c5ba697b6759
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142633685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e229524f286e653111cb9d028bf1ba4c3490742c8cd18c84af22538f0e68575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:57:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:57:47 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:57:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:58:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:58:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:58:20 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:58:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:58:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:58:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:58:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:58:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:59:25 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:59:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:59:28 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:59:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:59:30 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c023923f622f4a64d561898afe3142f49c5ed26cb2f27f22d6e8877ba87092`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af22db8f5e1863d738d7c6fbc4f3e66ce8192417c4c59ccc89660f88f75826f0`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 857.1 KB (857150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c3a923aa34c4af8180e555667ca6db39a920b02de2154c873486de062b6bd`  
		Last Modified: Wed, 14 Sep 2022 22:00:05 GMT  
		Size: 4.4 MB (4433575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830d9608cd584343e51f4b7e372689596389d335cf96fa70d4ef31a2cb3c8337`  
		Last Modified: Wed, 14 Sep 2022 22:00:03 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914654f8cd5683bc7bf3f7025aa7fd9b5fe827c2cf69f81d1ba90b930a25090`  
		Last Modified: Wed, 14 Sep 2022 22:00:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a35992845d8a14e6a802651fb7b44463b3e032e0662761af253d27a2c31054`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 53.8 MB (53817808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4540528c83e950b7d415eb645620fd2f038d5e74b6cec9af48f0c2d352223`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec168f6cfd418dda7322375cdd92a8218f3b7ea07bc7abe882ae7d9d960cf`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 44.1 MB (44105600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742f8a782c5d9f0a1ad0052513356440cad2abe1c334cfac66792f7fddd691a`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e5cc37f4b17fb6bbb5c7c41abeb9ca6f2967b2e0755d65f34d85918eb49963`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:c00749f00b317206048b8eaf304ded3941ecaf452b73a8e178b8ea2d1fc29342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:12477b35d174c1a410da24a05c4884693836e2a863521aa339a1298ce48b8369
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157889330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e66721c05dacebba2911adc611de5a71b95458b5a7208fb961aa3051b5eec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:21:45 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 05 Oct 2022 04:21:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:21:51 GMT
ENV GOSU_VERSION=1.14
# Wed, 05 Oct 2022 04:22:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 04:22:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 04:22:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:07 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 05 Oct 2022 04:22:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 05 Oct 2022 04:22:08 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Wed, 05 Oct 2022 04:22:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 05 Oct 2022 04:22:23 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 05 Oct 2022 04:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Oct 2022 04:22:24 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 05 Oct 2022 04:22:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 04:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 04:22:25 GMT
EXPOSE 3306 33060
# Wed, 05 Oct 2022 04:22:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498ba1a3ae2dfa82359e0fb959af536134a1360d33dfa87638e409b70b3fa3`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c224eff0af51a4254bf410ca8f6cab7044171639fc6e7b29cd55248bb609d02`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 4.4 MB (4414808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdd40c1260704addfdb3a21bf71ae5c14567100f98acd4d8dfec303294e1c5f`  
		Last Modified: Wed, 05 Oct 2022 04:23:50 GMT  
		Size: 1.4 MB (1418452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c3ece0305cbf295220adfdacf8c9e9fdf5de35ea07e505913ea4ee6e1f4f74`  
		Last Modified: Wed, 05 Oct 2022 04:23:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a10286651685e256e36f218063406728987d0f36c285adf41d41f8665661b74`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 12.7 MB (12661783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a34b42ee331888b70b38f6c96cacce54fe2bb4cf6e2ccefdd7add2144d5a3e`  
		Last Modified: Wed, 05 Oct 2022 04:23:49 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1363e6677cacb6f7960a756d9b4c0aa8d4c8ec02869cb4a6d9159faa60ecba4`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1110efce5dd0e631830f85c1a0c25efbba11b2e55314c04bb4fc0f97a30fdfc`  
		Last Modified: Wed, 05 Oct 2022 04:24:04 GMT  
		Size: 108.0 MB (107963159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fda2bd249a81a6cde8a8959a44831ac82aa8e5ecf3e1d508cf07ae87454330`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89080d4312c49459448781df923db9f843c0f978fc5100842de22d34ce9b142`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d74113edbbb66aa319322589f5e5f54f3ac373cc17fb9a2fdd5c3fe2f877345`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:b9532b1edea72b6cee12d9f5a78547bd3812ea5db842566e17f8b33291ed2921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8c43b0fffec41abcb01d825b8d1a3bf49f28cca94bb350943c1686c633345fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133891432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fcfca0776df8e192d1647da2866237fbd9f8e875fb496e4ca887369b2dd995`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:45:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:45:02 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:45:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:45:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:45:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:45:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:45:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:46:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:46:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:46:30 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:46:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:46:31 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7627573fa82aa6fa625675120ab2da659d056afc38872fba26aaa03bfcc97443`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b358d779638ca172a6cd9fac8926779ec83f0cc1ec5f5e598a842659b95be`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 928.8 KB (928830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753aff4b95947bb49e47f9adc6169f5b718b649b13e0aa8dd3f8aeb32d28e1`  
		Last Modified: Wed, 14 Sep 2022 21:47:11 GMT  
		Size: 4.6 MB (4606953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa3bee53f45d4b5f13b1680267324c732f70099f5aeb6e2cea0f23fd100657`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5227e0d612cc3cbdbadda9082d35821013b94be48915f0e225ec362338f3893`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4368b19837a5d3b7ae0549f97f90ef0cde786eac09c2082bdc9400645727a`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 47.7 MB (47733942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26212810c32af8d7ce6567aa5e4eff976d8c236df93ea2403207ba13790c191`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803d4215f950ffbe84f925527006ced4d892ad0bb98a5839f83b0ad1011cc3b`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 40.0 MB (40021785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5358a7f7d072df12dc5e2276f7cb10cb069c1f606b23308e2693ad3da9f0528`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435e8908cd690ccf82ed2d0567095013ef79686b3b650f59e699694a0735a311`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d8ceb97140e661a4ef94a1f8960442f009c70302f2212762b3f8c5ba697b6759
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142633685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e229524f286e653111cb9d028bf1ba4c3490742c8cd18c84af22538f0e68575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:57:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:57:47 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:57:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:58:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:58:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:58:20 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:58:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:58:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:58:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:58:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:58:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:59:25 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:59:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:59:28 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:59:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:59:30 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c023923f622f4a64d561898afe3142f49c5ed26cb2f27f22d6e8877ba87092`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af22db8f5e1863d738d7c6fbc4f3e66ce8192417c4c59ccc89660f88f75826f0`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 857.1 KB (857150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c3a923aa34c4af8180e555667ca6db39a920b02de2154c873486de062b6bd`  
		Last Modified: Wed, 14 Sep 2022 22:00:05 GMT  
		Size: 4.4 MB (4433575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830d9608cd584343e51f4b7e372689596389d335cf96fa70d4ef31a2cb3c8337`  
		Last Modified: Wed, 14 Sep 2022 22:00:03 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914654f8cd5683bc7bf3f7025aa7fd9b5fe827c2cf69f81d1ba90b930a25090`  
		Last Modified: Wed, 14 Sep 2022 22:00:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a35992845d8a14e6a802651fb7b44463b3e032e0662761af253d27a2c31054`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 53.8 MB (53817808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4540528c83e950b7d415eb645620fd2f038d5e74b6cec9af48f0c2d352223`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec168f6cfd418dda7322375cdd92a8218f3b7ea07bc7abe882ae7d9d960cf`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 44.1 MB (44105600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742f8a782c5d9f0a1ad0052513356440cad2abe1c334cfac66792f7fddd691a`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e5cc37f4b17fb6bbb5c7c41abeb9ca6f2967b2e0755d65f34d85918eb49963`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.30`

```console
$ docker pull mysql@sha256:b9532b1edea72b6cee12d9f5a78547bd3812ea5db842566e17f8b33291ed2921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.30` - linux; amd64

```console
$ docker pull mysql@sha256:8c43b0fffec41abcb01d825b8d1a3bf49f28cca94bb350943c1686c633345fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133891432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fcfca0776df8e192d1647da2866237fbd9f8e875fb496e4ca887369b2dd995`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:45:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:45:02 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:45:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:45:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:45:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:45:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:45:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:46:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:46:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:46:30 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:46:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:46:31 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7627573fa82aa6fa625675120ab2da659d056afc38872fba26aaa03bfcc97443`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b358d779638ca172a6cd9fac8926779ec83f0cc1ec5f5e598a842659b95be`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 928.8 KB (928830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753aff4b95947bb49e47f9adc6169f5b718b649b13e0aa8dd3f8aeb32d28e1`  
		Last Modified: Wed, 14 Sep 2022 21:47:11 GMT  
		Size: 4.6 MB (4606953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa3bee53f45d4b5f13b1680267324c732f70099f5aeb6e2cea0f23fd100657`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5227e0d612cc3cbdbadda9082d35821013b94be48915f0e225ec362338f3893`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4368b19837a5d3b7ae0549f97f90ef0cde786eac09c2082bdc9400645727a`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 47.7 MB (47733942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26212810c32af8d7ce6567aa5e4eff976d8c236df93ea2403207ba13790c191`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803d4215f950ffbe84f925527006ced4d892ad0bb98a5839f83b0ad1011cc3b`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 40.0 MB (40021785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5358a7f7d072df12dc5e2276f7cb10cb069c1f606b23308e2693ad3da9f0528`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435e8908cd690ccf82ed2d0567095013ef79686b3b650f59e699694a0735a311`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.30` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d8ceb97140e661a4ef94a1f8960442f009c70302f2212762b3f8c5ba697b6759
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142633685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e229524f286e653111cb9d028bf1ba4c3490742c8cd18c84af22538f0e68575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:57:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:57:47 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:57:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:58:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:58:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:58:20 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:58:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:58:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:58:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:58:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:58:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:59:25 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:59:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:59:28 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:59:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:59:30 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c023923f622f4a64d561898afe3142f49c5ed26cb2f27f22d6e8877ba87092`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af22db8f5e1863d738d7c6fbc4f3e66ce8192417c4c59ccc89660f88f75826f0`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 857.1 KB (857150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c3a923aa34c4af8180e555667ca6db39a920b02de2154c873486de062b6bd`  
		Last Modified: Wed, 14 Sep 2022 22:00:05 GMT  
		Size: 4.4 MB (4433575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830d9608cd584343e51f4b7e372689596389d335cf96fa70d4ef31a2cb3c8337`  
		Last Modified: Wed, 14 Sep 2022 22:00:03 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914654f8cd5683bc7bf3f7025aa7fd9b5fe827c2cf69f81d1ba90b930a25090`  
		Last Modified: Wed, 14 Sep 2022 22:00:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a35992845d8a14e6a802651fb7b44463b3e032e0662761af253d27a2c31054`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 53.8 MB (53817808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4540528c83e950b7d415eb645620fd2f038d5e74b6cec9af48f0c2d352223`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec168f6cfd418dda7322375cdd92a8218f3b7ea07bc7abe882ae7d9d960cf`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 44.1 MB (44105600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742f8a782c5d9f0a1ad0052513356440cad2abe1c334cfac66792f7fddd691a`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e5cc37f4b17fb6bbb5c7c41abeb9ca6f2967b2e0755d65f34d85918eb49963`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.30-debian`

```console
$ docker pull mysql@sha256:c00749f00b317206048b8eaf304ded3941ecaf452b73a8e178b8ea2d1fc29342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.30-debian` - linux; amd64

```console
$ docker pull mysql@sha256:12477b35d174c1a410da24a05c4884693836e2a863521aa339a1298ce48b8369
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157889330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e66721c05dacebba2911adc611de5a71b95458b5a7208fb961aa3051b5eec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:21:45 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 05 Oct 2022 04:21:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:21:51 GMT
ENV GOSU_VERSION=1.14
# Wed, 05 Oct 2022 04:22:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 04:22:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 04:22:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:07 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 05 Oct 2022 04:22:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 05 Oct 2022 04:22:08 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Wed, 05 Oct 2022 04:22:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 05 Oct 2022 04:22:23 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 05 Oct 2022 04:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Oct 2022 04:22:24 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 05 Oct 2022 04:22:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 04:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 04:22:25 GMT
EXPOSE 3306 33060
# Wed, 05 Oct 2022 04:22:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498ba1a3ae2dfa82359e0fb959af536134a1360d33dfa87638e409b70b3fa3`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c224eff0af51a4254bf410ca8f6cab7044171639fc6e7b29cd55248bb609d02`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 4.4 MB (4414808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdd40c1260704addfdb3a21bf71ae5c14567100f98acd4d8dfec303294e1c5f`  
		Last Modified: Wed, 05 Oct 2022 04:23:50 GMT  
		Size: 1.4 MB (1418452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c3ece0305cbf295220adfdacf8c9e9fdf5de35ea07e505913ea4ee6e1f4f74`  
		Last Modified: Wed, 05 Oct 2022 04:23:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a10286651685e256e36f218063406728987d0f36c285adf41d41f8665661b74`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 12.7 MB (12661783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a34b42ee331888b70b38f6c96cacce54fe2bb4cf6e2ccefdd7add2144d5a3e`  
		Last Modified: Wed, 05 Oct 2022 04:23:49 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1363e6677cacb6f7960a756d9b4c0aa8d4c8ec02869cb4a6d9159faa60ecba4`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1110efce5dd0e631830f85c1a0c25efbba11b2e55314c04bb4fc0f97a30fdfc`  
		Last Modified: Wed, 05 Oct 2022 04:24:04 GMT  
		Size: 108.0 MB (107963159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fda2bd249a81a6cde8a8959a44831ac82aa8e5ecf3e1d508cf07ae87454330`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89080d4312c49459448781df923db9f843c0f978fc5100842de22d34ce9b142`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d74113edbbb66aa319322589f5e5f54f3ac373cc17fb9a2fdd5c3fe2f877345`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.30-oracle`

```console
$ docker pull mysql@sha256:b9532b1edea72b6cee12d9f5a78547bd3812ea5db842566e17f8b33291ed2921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.30-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8c43b0fffec41abcb01d825b8d1a3bf49f28cca94bb350943c1686c633345fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133891432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fcfca0776df8e192d1647da2866237fbd9f8e875fb496e4ca887369b2dd995`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:45:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:45:02 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:45:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:45:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:45:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:45:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:45:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:46:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:46:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:46:30 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:46:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:46:31 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7627573fa82aa6fa625675120ab2da659d056afc38872fba26aaa03bfcc97443`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b358d779638ca172a6cd9fac8926779ec83f0cc1ec5f5e598a842659b95be`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 928.8 KB (928830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753aff4b95947bb49e47f9adc6169f5b718b649b13e0aa8dd3f8aeb32d28e1`  
		Last Modified: Wed, 14 Sep 2022 21:47:11 GMT  
		Size: 4.6 MB (4606953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa3bee53f45d4b5f13b1680267324c732f70099f5aeb6e2cea0f23fd100657`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5227e0d612cc3cbdbadda9082d35821013b94be48915f0e225ec362338f3893`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4368b19837a5d3b7ae0549f97f90ef0cde786eac09c2082bdc9400645727a`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 47.7 MB (47733942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26212810c32af8d7ce6567aa5e4eff976d8c236df93ea2403207ba13790c191`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803d4215f950ffbe84f925527006ced4d892ad0bb98a5839f83b0ad1011cc3b`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 40.0 MB (40021785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5358a7f7d072df12dc5e2276f7cb10cb069c1f606b23308e2693ad3da9f0528`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435e8908cd690ccf82ed2d0567095013ef79686b3b650f59e699694a0735a311`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.30-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d8ceb97140e661a4ef94a1f8960442f009c70302f2212762b3f8c5ba697b6759
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142633685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e229524f286e653111cb9d028bf1ba4c3490742c8cd18c84af22538f0e68575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:57:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:57:47 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:57:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:58:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:58:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:58:20 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:58:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:58:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:58:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:58:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:58:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:59:25 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:59:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:59:28 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:59:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:59:30 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c023923f622f4a64d561898afe3142f49c5ed26cb2f27f22d6e8877ba87092`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af22db8f5e1863d738d7c6fbc4f3e66ce8192417c4c59ccc89660f88f75826f0`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 857.1 KB (857150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c3a923aa34c4af8180e555667ca6db39a920b02de2154c873486de062b6bd`  
		Last Modified: Wed, 14 Sep 2022 22:00:05 GMT  
		Size: 4.4 MB (4433575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830d9608cd584343e51f4b7e372689596389d335cf96fa70d4ef31a2cb3c8337`  
		Last Modified: Wed, 14 Sep 2022 22:00:03 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914654f8cd5683bc7bf3f7025aa7fd9b5fe827c2cf69f81d1ba90b930a25090`  
		Last Modified: Wed, 14 Sep 2022 22:00:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a35992845d8a14e6a802651fb7b44463b3e032e0662761af253d27a2c31054`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 53.8 MB (53817808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4540528c83e950b7d415eb645620fd2f038d5e74b6cec9af48f0c2d352223`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec168f6cfd418dda7322375cdd92a8218f3b7ea07bc7abe882ae7d9d960cf`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 44.1 MB (44105600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742f8a782c5d9f0a1ad0052513356440cad2abe1c334cfac66792f7fddd691a`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e5cc37f4b17fb6bbb5c7c41abeb9ca6f2967b2e0755d65f34d85918eb49963`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:c00749f00b317206048b8eaf304ded3941ecaf452b73a8e178b8ea2d1fc29342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:12477b35d174c1a410da24a05c4884693836e2a863521aa339a1298ce48b8369
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157889330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e66721c05dacebba2911adc611de5a71b95458b5a7208fb961aa3051b5eec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:21:45 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 05 Oct 2022 04:21:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:21:51 GMT
ENV GOSU_VERSION=1.14
# Wed, 05 Oct 2022 04:22:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 04:22:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 04:22:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:22:07 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 05 Oct 2022 04:22:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 05 Oct 2022 04:22:08 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Wed, 05 Oct 2022 04:22:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 05 Oct 2022 04:22:23 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 05 Oct 2022 04:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Oct 2022 04:22:24 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 05 Oct 2022 04:22:24 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 05 Oct 2022 04:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 04:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 04:22:25 GMT
EXPOSE 3306 33060
# Wed, 05 Oct 2022 04:22:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498ba1a3ae2dfa82359e0fb959af536134a1360d33dfa87638e409b70b3fa3`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c224eff0af51a4254bf410ca8f6cab7044171639fc6e7b29cd55248bb609d02`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 4.4 MB (4414808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdd40c1260704addfdb3a21bf71ae5c14567100f98acd4d8dfec303294e1c5f`  
		Last Modified: Wed, 05 Oct 2022 04:23:50 GMT  
		Size: 1.4 MB (1418452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c3ece0305cbf295220adfdacf8c9e9fdf5de35ea07e505913ea4ee6e1f4f74`  
		Last Modified: Wed, 05 Oct 2022 04:23:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a10286651685e256e36f218063406728987d0f36c285adf41d41f8665661b74`  
		Last Modified: Wed, 05 Oct 2022 04:23:52 GMT  
		Size: 12.7 MB (12661783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a34b42ee331888b70b38f6c96cacce54fe2bb4cf6e2ccefdd7add2144d5a3e`  
		Last Modified: Wed, 05 Oct 2022 04:23:49 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1363e6677cacb6f7960a756d9b4c0aa8d4c8ec02869cb4a6d9159faa60ecba4`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1110efce5dd0e631830f85c1a0c25efbba11b2e55314c04bb4fc0f97a30fdfc`  
		Last Modified: Wed, 05 Oct 2022 04:24:04 GMT  
		Size: 108.0 MB (107963159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fda2bd249a81a6cde8a8959a44831ac82aa8e5ecf3e1d508cf07ae87454330`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89080d4312c49459448781df923db9f843c0f978fc5100842de22d34ce9b142`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d74113edbbb66aa319322589f5e5f54f3ac373cc17fb9a2fdd5c3fe2f877345`  
		Last Modified: Wed, 05 Oct 2022 04:23:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:b9532b1edea72b6cee12d9f5a78547bd3812ea5db842566e17f8b33291ed2921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:8c43b0fffec41abcb01d825b8d1a3bf49f28cca94bb350943c1686c633345fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133891432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fcfca0776df8e192d1647da2866237fbd9f8e875fb496e4ca887369b2dd995`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:45:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:45:02 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:45:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:45:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:45:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:45:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:45:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:46:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:46:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:46:30 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:46:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:46:31 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7627573fa82aa6fa625675120ab2da659d056afc38872fba26aaa03bfcc97443`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b358d779638ca172a6cd9fac8926779ec83f0cc1ec5f5e598a842659b95be`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 928.8 KB (928830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753aff4b95947bb49e47f9adc6169f5b718b649b13e0aa8dd3f8aeb32d28e1`  
		Last Modified: Wed, 14 Sep 2022 21:47:11 GMT  
		Size: 4.6 MB (4606953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa3bee53f45d4b5f13b1680267324c732f70099f5aeb6e2cea0f23fd100657`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5227e0d612cc3cbdbadda9082d35821013b94be48915f0e225ec362338f3893`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4368b19837a5d3b7ae0549f97f90ef0cde786eac09c2082bdc9400645727a`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 47.7 MB (47733942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26212810c32af8d7ce6567aa5e4eff976d8c236df93ea2403207ba13790c191`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803d4215f950ffbe84f925527006ced4d892ad0bb98a5839f83b0ad1011cc3b`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 40.0 MB (40021785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5358a7f7d072df12dc5e2276f7cb10cb069c1f606b23308e2693ad3da9f0528`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435e8908cd690ccf82ed2d0567095013ef79686b3b650f59e699694a0735a311`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d8ceb97140e661a4ef94a1f8960442f009c70302f2212762b3f8c5ba697b6759
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142633685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e229524f286e653111cb9d028bf1ba4c3490742c8cd18c84af22538f0e68575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:57:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:57:47 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:57:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:58:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:58:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:58:20 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:58:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:58:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:58:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:58:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:58:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:59:25 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:59:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:59:28 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:59:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:59:30 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c023923f622f4a64d561898afe3142f49c5ed26cb2f27f22d6e8877ba87092`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af22db8f5e1863d738d7c6fbc4f3e66ce8192417c4c59ccc89660f88f75826f0`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 857.1 KB (857150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c3a923aa34c4af8180e555667ca6db39a920b02de2154c873486de062b6bd`  
		Last Modified: Wed, 14 Sep 2022 22:00:05 GMT  
		Size: 4.4 MB (4433575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830d9608cd584343e51f4b7e372689596389d335cf96fa70d4ef31a2cb3c8337`  
		Last Modified: Wed, 14 Sep 2022 22:00:03 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914654f8cd5683bc7bf3f7025aa7fd9b5fe827c2cf69f81d1ba90b930a25090`  
		Last Modified: Wed, 14 Sep 2022 22:00:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a35992845d8a14e6a802651fb7b44463b3e032e0662761af253d27a2c31054`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 53.8 MB (53817808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4540528c83e950b7d415eb645620fd2f038d5e74b6cec9af48f0c2d352223`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec168f6cfd418dda7322375cdd92a8218f3b7ea07bc7abe882ae7d9d960cf`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 44.1 MB (44105600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742f8a782c5d9f0a1ad0052513356440cad2abe1c334cfac66792f7fddd691a`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e5cc37f4b17fb6bbb5c7c41abeb9ca6f2967b2e0755d65f34d85918eb49963`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:b9532b1edea72b6cee12d9f5a78547bd3812ea5db842566e17f8b33291ed2921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8c43b0fffec41abcb01d825b8d1a3bf49f28cca94bb350943c1686c633345fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133891432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fcfca0776df8e192d1647da2866237fbd9f8e875fb496e4ca887369b2dd995`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:45:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:45:02 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:45:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:45:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:45:29 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:45:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:45:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:45:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:45:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:46:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:46:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:46:30 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:46:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:46:31 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7627573fa82aa6fa625675120ab2da659d056afc38872fba26aaa03bfcc97443`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b358d779638ca172a6cd9fac8926779ec83f0cc1ec5f5e598a842659b95be`  
		Last Modified: Wed, 14 Sep 2022 21:47:12 GMT  
		Size: 928.8 KB (928830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753aff4b95947bb49e47f9adc6169f5b718b649b13e0aa8dd3f8aeb32d28e1`  
		Last Modified: Wed, 14 Sep 2022 21:47:11 GMT  
		Size: 4.6 MB (4606953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa3bee53f45d4b5f13b1680267324c732f70099f5aeb6e2cea0f23fd100657`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5227e0d612cc3cbdbadda9082d35821013b94be48915f0e225ec362338f3893`  
		Last Modified: Wed, 14 Sep 2022 21:47:10 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4368b19837a5d3b7ae0549f97f90ef0cde786eac09c2082bdc9400645727a`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 47.7 MB (47733942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26212810c32af8d7ce6567aa5e4eff976d8c236df93ea2403207ba13790c191`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803d4215f950ffbe84f925527006ced4d892ad0bb98a5839f83b0ad1011cc3b`  
		Last Modified: Wed, 14 Sep 2022 21:47:15 GMT  
		Size: 40.0 MB (40021785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5358a7f7d072df12dc5e2276f7cb10cb069c1f606b23308e2693ad3da9f0528`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435e8908cd690ccf82ed2d0567095013ef79686b3b650f59e699694a0735a311`  
		Last Modified: Wed, 14 Sep 2022 21:47:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d8ceb97140e661a4ef94a1f8960442f009c70302f2212762b3f8c5ba697b6759
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142633685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e229524f286e653111cb9d028bf1ba4c3490742c8cd18c84af22538f0e68575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:57:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Sep 2022 21:57:47 GMT
ENV GOSU_VERSION=1.14
# Wed, 14 Sep 2022 21:57:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Sep 2022 21:58:17 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:58:19 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Sep 2022 21:58:20 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Sep 2022 21:58:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:58:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 14 Sep 2022 21:58:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 14 Sep 2022 21:58:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 14 Sep 2022 21:58:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Wed, 14 Sep 2022 21:59:25 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 14 Sep 2022 21:59:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Sep 2022 21:59:28 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Wed, 14 Sep 2022 21:59:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Sep 2022 21:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Sep 2022 21:59:30 GMT
EXPOSE 3306 33060
# Wed, 14 Sep 2022 21:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c023923f622f4a64d561898afe3142f49c5ed26cb2f27f22d6e8877ba87092`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af22db8f5e1863d738d7c6fbc4f3e66ce8192417c4c59ccc89660f88f75826f0`  
		Last Modified: Wed, 14 Sep 2022 22:00:06 GMT  
		Size: 857.1 KB (857150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428c3a923aa34c4af8180e555667ca6db39a920b02de2154c873486de062b6bd`  
		Last Modified: Wed, 14 Sep 2022 22:00:05 GMT  
		Size: 4.4 MB (4433575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830d9608cd584343e51f4b7e372689596389d335cf96fa70d4ef31a2cb3c8337`  
		Last Modified: Wed, 14 Sep 2022 22:00:03 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914654f8cd5683bc7bf3f7025aa7fd9b5fe827c2cf69f81d1ba90b930a25090`  
		Last Modified: Wed, 14 Sep 2022 22:00:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a35992845d8a14e6a802651fb7b44463b3e032e0662761af253d27a2c31054`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 53.8 MB (53817808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4540528c83e950b7d415eb645620fd2f038d5e74b6cec9af48f0c2d352223`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec168f6cfd418dda7322375cdd92a8218f3b7ea07bc7abe882ae7d9d960cf`  
		Last Modified: Wed, 14 Sep 2022 22:00:09 GMT  
		Size: 44.1 MB (44105600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742f8a782c5d9f0a1ad0052513356440cad2abe1c334cfac66792f7fddd691a`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 5.4 KB (5382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e5cc37f4b17fb6bbb5c7c41abeb9ca6f2967b2e0755d65f34d85918eb49963`  
		Last Modified: Wed, 14 Sep 2022 22:00:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
