## `percona:8-centos`

```console
$ docker pull percona@sha256:55acff48f9effec3d62a2e225662940d959836ec4b8110eb58440321f55fd785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:276403c53deb65339e7e46de7fcb67d990f0c9abdc92917eca1f02b2a9f7102c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.8 MB (443844644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eba0410133303a62077cc13737158d38505b5d731b117a75dfe84886474c91f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Mar 2023 20:22:21 GMT
ADD file:59635cb4a05af7cf47897b040053d3efd0d1398a3b8add59c5c8e0dcadbe35bf in / 
# Wed, 08 Mar 2023 20:22:22 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 20:45:02 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Mar 2023 20:45:03 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 08 Mar 2023 20:45:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Wed, 08 Mar 2023 20:45:38 GMT
ENV PS_VERSION=8.0.29-21.1
# Wed, 08 Mar 2023 20:45:38 GMT
ENV OS_VER=el8
# Wed, 08 Mar 2023 20:45:38 GMT
ENV FULL_PERCONA_VERSION=8.0.29-21.1.el8
# Wed, 08 Mar 2023 20:46:24 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 08 Mar 2023 20:46:27 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 08 Mar 2023 20:46:27 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Mar 2023 20:46:27 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Wed, 08 Mar 2023 20:46:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Mar 2023 20:46:27 GMT
USER mysql
# Wed, 08 Mar 2023 20:46:27 GMT
EXPOSE 3306 33060
# Wed, 08 Mar 2023 20:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5e01956c53d898e172d8db363562f69df2f624c2cd6eaf3bea39c918d4dcbd89`  
		Last Modified: Wed, 08 Mar 2023 20:23:51 GMT  
		Size: 88.4 MB (88425286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ed3d7977020bf025fc1446200ec4821ca7516d3c399e79be9c94ffbb4e746`  
		Last Modified: Wed, 08 Mar 2023 20:50:27 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5568358bb55c4387e2b5948d7d402ede69cb51fcf1edee4e49e8aff62aef64a3`  
		Last Modified: Wed, 08 Mar 2023 20:50:37 GMT  
		Size: 175.9 MB (175949597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5904685a750cd8cc88f650c24dc706aec1d916982557083d61d09baa075beb66`  
		Last Modified: Wed, 08 Mar 2023 20:50:53 GMT  
		Size: 179.5 MB (179464338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3fbb9760e54457411051c49b67d53bd61f96663be56015d92a92b0197b4ae4`  
		Last Modified: Wed, 08 Mar 2023 20:50:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a540aa082d3ca21586e728f03b3f8e6bc90f76590d6e7ec17b05df047215290`  
		Last Modified: Wed, 08 Mar 2023 20:50:27 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
