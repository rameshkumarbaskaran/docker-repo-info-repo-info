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
