## `percona:ps-8.0.29-21`

```console
$ docker pull percona@sha256:10d464d97387911995af1305247b40cf27897cfd803134e71514e5b4ca19c899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.29-21` - linux; amd64

```console
$ docker pull percona@sha256:9965c500e913fd3419fd8bda2dba8b8d324d77de7e1c3d1042fe90d013f8d155
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.2 MB (442222113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ae8d2f67942f6cacdb76bbee4e9ea8a35d31960ae73a1d1ad17015ca3467f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:36:57 GMT
ADD file:38641c1822a4aea5527f6e7429caaa41595e7c7e63f993b0b4787b70ca1e56e2 in / 
# Thu, 23 Feb 2023 19:36:58 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:00:32 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 23 Feb 2023 20:00:33 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 23 Feb 2023 20:01:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Thu, 23 Feb 2023 20:01:05 GMT
ENV PS_VERSION=8.0.29-21.1
# Thu, 23 Feb 2023 20:01:05 GMT
ENV OS_VER=el8
# Thu, 23 Feb 2023 20:01:05 GMT
ENV FULL_PERCONA_VERSION=8.0.29-21.1.el8
# Thu, 23 Feb 2023 20:01:41 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 23 Feb 2023 20:01:43 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 23 Feb 2023 20:01:43 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 23 Feb 2023 20:01:43 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 23 Feb 2023 20:01:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:01:44 GMT
USER mysql
# Thu, 23 Feb 2023 20:01:44 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:01:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f3f135a9ee79c5ecc3e253037715137cd16bdf017f4dcf3900b517a7a2e0c1e8`  
		Last Modified: Thu, 23 Feb 2023 19:37:47 GMT  
		Size: 88.4 MB (88421873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aeb0e4010e1564c71143cb54e836ddcbdcb2e0648f5df32d5d9d099cead2fb`  
		Last Modified: Thu, 23 Feb 2023 20:05:55 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7d873c618c80b0beda44a43d2e55f0f2a3782c19a80ed3a5d83537a1799c62`  
		Last Modified: Thu, 23 Feb 2023 20:06:05 GMT  
		Size: 175.4 MB (175444930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ffb72b10c19c1996e29dca2e620901f5fa007a0fbde6d7feef33d5aab19ba6`  
		Last Modified: Thu, 23 Feb 2023 20:06:20 GMT  
		Size: 178.3 MB (178349889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eeb6625761c47c4435003620a3b273218d6aaf0dd286ae25c48508e99b4260`  
		Last Modified: Thu, 23 Feb 2023 20:05:55 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d942a3ec335a60567d2b4b0fd2187dc73b02e54c76917f6bc240dcd49755c75`  
		Last Modified: Thu, 23 Feb 2023 20:05:55 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
