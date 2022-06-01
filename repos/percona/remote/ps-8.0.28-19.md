## `percona:ps-8.0.28-19`

```console
$ docker pull percona@sha256:f10d0b90ecb6254b013628a84d45e5da6baaa4b13cf994ab3ec9ba601992fe3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.28-19` - linux; amd64

```console
$ docker pull percona@sha256:a6124078ae148ec7394f3f982d20e611fca9046f71a47fdba5d3c1bcabed1f26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.5 MB (407454916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3154773563b6a00247d2bcfd0781fe587c84cbb1042ca6dbc78ab683e44a69`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 Jun 2022 17:05:47 GMT
ADD file:48aa8cc19fd94c8679e43b263d7eec6d7f5d19f4288991eb0c68f52c91068a90 in / 
# Wed, 01 Jun 2022 17:05:48 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 18:00:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 01 Jun 2022 18:00:51 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 01 Jun 2022 18:01:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Wed, 01 Jun 2022 18:01:20 GMT
ENV PS_VERSION=8.0.28-19.1
# Wed, 01 Jun 2022 18:01:21 GMT
ENV OS_VER=el8
# Wed, 01 Jun 2022 18:01:21 GMT
ENV FULL_PERCONA_VERSION=8.0.28-19.1.el8
# Wed, 01 Jun 2022 18:02:04 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 01 Jun 2022 18:02:06 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 01 Jun 2022 18:02:06 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 01 Jun 2022 18:02:06 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Wed, 01 Jun 2022 18:02:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 18:02:06 GMT
USER mysql
# Wed, 01 Jun 2022 18:02:06 GMT
EXPOSE 3306 33060
# Wed, 01 Jun 2022 18:02:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ec2c52e89d2aa80aa01fc0e5f2ca1dc539d07b8f53e020f0c5af0f3e3c482525`  
		Last Modified: Wed, 01 Jun 2022 17:06:38 GMT  
		Size: 84.6 MB (84568422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff3d33a86d3ae8f548ce307ef8fd866966a3676d0b85be07e56f4671be14c1c`  
		Last Modified: Wed, 01 Jun 2022 18:06:20 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debf63d29c47dfe0969d3673b8e679b70dc4f3f5588cb8775d50435bf243d25d`  
		Last Modified: Wed, 01 Jun 2022 18:06:29 GMT  
		Size: 147.8 MB (147803530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5693a8b48bebdbdbf4ed4b7328f5c1bf8dd64cc8da2683cf61ec0c6b197bf5`  
		Last Modified: Wed, 01 Jun 2022 18:06:46 GMT  
		Size: 175.1 MB (175077542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c426d6872127ce56461605be593ff4721e4aadec8a8d30bc3bf573a13c23f7`  
		Last Modified: Wed, 01 Jun 2022 18:06:20 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8a5cab69f40eb3e74cf1a69e6df23b565a11b92625f8fdf7a949865302d5f0`  
		Last Modified: Wed, 01 Jun 2022 18:06:20 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
