## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:3b3288074ba41224f475737d211cfcbcf067ceab8bcc33bce335e7e68733eb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c9fec3bd72bbe0b2823c8146e6496127c2956f0a8b5f8ccfc55182a2721400e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131397757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c40e8c9733a486a75f03c9b38d2487e2a2ed3176b4b2e4b635fde969c7cb10`
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
# Fri, 25 Feb 2022 03:32:07 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 03:32:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 03:32:49 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:32:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 03:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 03:33:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 03:33:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:33:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:33:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:33:44 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:33:45 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:33:45 GMT
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
	-	`sha256:b69cc9c42213611889f94baffd34bae26e70b5c649f08f8413b11e768c161a2f`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 3.1 MB (3113129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7216bd700f0e78596085fdfe14df3b52f8a1ffa74c36fb1347ecebd666f43565`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed60440ccffd47e25d61aae903ee39fe7e94f84279b00ed2ac45519e617c096b`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f9c0fb50c73b47a6985efcb852651a804c512dc2435ea248c0c391d3384d9`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 47.2 MB (47216437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea56ac1a1fe9b67a35c85910563c7cb4515c4f6fec5422685442c76f32b16f9`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66437fa01c48af6a7230b921b18cd451d7c9f7c4d55b6dd2660595c954b4e5df`  
		Last Modified: Fri, 25 Feb 2022 03:36:03 GMT  
		Size: 38.2 MB (38248768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad48a805d9f1a437c87f20327806cb37f7b44f9c0d1d14d1664efd505b7de5`  
		Last Modified: Fri, 25 Feb 2022 03:35:55 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed9f0eb3b100fc28d9a5946b48de127cbbe846af0a49c07e1b3488f70bad6000
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139932347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ba820812516512aad540266121d6b6f5ff261efef5e1a30e43537c90ecc250`
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
# Fri, 25 Feb 2022 02:58:41 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Fri, 25 Feb 2022 02:59:17 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 25 Feb 2022 02:59:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 25 Feb 2022 02:59:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 02:59:20 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 25 Feb 2022 02:59:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 25 Feb 2022 02:59:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 25 Feb 2022 02:59:47 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 25 Feb 2022 03:00:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 25 Feb 2022 03:00:30 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 03:00:32 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Fri, 25 Feb 2022 03:00:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:00:33 GMT
EXPOSE 3306 33060
# Fri, 25 Feb 2022 03:00:34 GMT
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
	-	`sha256:e99e7cda9427a7e16e3c00fd2d0e3c09a589a827177c9b3bd00562cd23fcc290`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 3.3 MB (3257102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7073284934f73f97f317a638af1c6f296e22717b7384f524497183dfae152`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97067f99c33d1d930cdeb33ead10f729fc121dfa0030bed96bae455c3cb190c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea6bac00966feeb96a990385efe9d1ae852191034ba52b0f15bf244f76d4ef`  
		Last Modified: Fri, 25 Feb 2022 03:01:01 GMT  
		Size: 53.4 MB (53380825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b97d6d1f3243fd9432aa48783caf6738ba38e70cd4d2ac02a7e4ec0de0811f`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96691f58fb8e44a6255e1f0e4915ebf5f1abc3a8072b1955d65bc7c5d76e44f8`  
		Last Modified: Fri, 25 Feb 2022 03:01:00 GMT  
		Size: 40.5 MB (40476174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc29ad3e8e8b2ca29d8e03393fe1ced3c309a955cf8943fa0f33a670b74e7c4`  
		Last Modified: Fri, 25 Feb 2022 03:00:53 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
