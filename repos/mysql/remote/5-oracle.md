## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:6a7a8a0c15fa4ca0d9ec85ac3fda70b4749e52fd13c9ca4d5eb0d16efc192e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:847a9c4e83c6bd9fe737e8fb841a2d6197d1407a4657ddb810060a9fff475e76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124779861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63e577980bf587f2bafeea4ae79d9eb41c5744cde8f9d24501a7c3a806a23da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:33:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:33:55 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:33:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 08 Mar 2022 19:26:31 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 08 Mar 2022 19:27:03 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Tue, 08 Mar 2022 19:27:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:27:18 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:27:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:27:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Tue, 08 Mar 2022 19:27:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:27:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:27:38 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:27:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:27:38 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:27:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4915557694f2e99ba4f3c31018dd343c5dd684cc17dfc82bc6907c0ad8b7c7be`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda14bdaa732132cfb0a98e28a5372b750b07f7c701dd3f23b27209d91359dd0`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 930.2 KB (930235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b5fb768db2157c6bdb3a1bcac58e3652bf1543d39f8a81f3ee8be220b3a712`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 3.7 MB (3708422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd86b448d395b76436c8bbfc3b07df034056a757f7420243eb4e4c8783d9503`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a856e87d733fdb342899ec85fff5eb1f64b798a865fa1cda8a2aea57ec9c6f31`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af78d167e47009381ea4d0fe0033d991f03d879159801424084ffca52ed2a075`  
		Last Modified: Tue, 08 Mar 2022 19:29:50 GMT  
		Size: 25.4 MB (25445899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f23017b8e617195316dee8808ceb16ecb9c4e1da4e8230a88af69a9070c077f`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e418ba1e823bddac09c2b166a2d7cbcc06166878249d85ad07119637d8d4a`  
		Last Modified: Tue, 08 Mar 2022 19:29:54 GMT  
		Size: 46.4 MB (46354930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d661b191f612f8741ee6366a28d4f6231833fed59ccf3b145a95c68fd49bcfbf`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
