## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:bafce326af2e71c855dc0df3121049e6b1182e7f9098d5c9ae4e4b4612943650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1e755fd5ab6cd782256827067603dbef93493c4a91bbb88d51362dbf1f57e8b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125246919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca04d328ed5ac0823dd3252bdf8432e49da9fdf36631d6850ddcf1284a8bbdee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:12:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:12:23 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:12:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:12:36 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 31 Mar 2022 02:12:37 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Thu, 31 Mar 2022 02:12:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 31 Mar 2022 02:12:52 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 31 Mar 2022 02:12:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 31 Mar 2022 02:12:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Thu, 31 Mar 2022 02:13:10 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 31 Mar 2022 02:13:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 31 Mar 2022 02:13:11 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 31 Mar 2022 02:13:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:13:11 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:13:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1268f9b69b4d2dfc0086f5426266fd97bb99c37e0dc2db707e3e7a5667bba3c`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1084d021338c13d9afc0d3fa5ab8ff753ddd7d97abc2a81074b6fff0807a96`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ad34fb0ede94774c93b333cbdc752915f8d0b45eda981588615248b8fbad9e`  
		Last Modified: Thu, 31 Mar 2022 02:14:12 GMT  
		Size: 3.8 MB (3755164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341499385aec2522efd754b4ba03c458add9de6802a7834b941209fb793dc0f`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31c594d2051139e02d66cb9398ff3c5a88a0028582d910412000794e0bdf8cb`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10402a7aeb1ec24fc39bb20fb660442e97663d31323f62ef129df564b2028e0a`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 25.5 MB (25471062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb1127c3ae153f55defbf50395e6dfccffdf83d2ced9935588799d02e261632`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c376f51d5a2e25c8a3858cb731885b73c177d96433a1e9a591d757ebbb61f3c7`  
		Last Modified: Thu, 31 Mar 2022 02:14:18 GMT  
		Size: 46.3 MB (46323475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144aebf1e30feeda4a8dcd3e7abbab3bc10d0fbe37018acf6d4ff6f0c67742c7`  
		Last Modified: Thu, 31 Mar 2022 02:14:09 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
