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
