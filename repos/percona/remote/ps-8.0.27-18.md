## `percona:ps-8.0.27-18`

```console
$ docker pull percona@sha256:ef6b1fd59b07b6790ddff13828eaf428a3bf260f44a627b61599a1775c1ff56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.27-18` - linux; amd64

```console
$ docker pull percona@sha256:a03109c29c0cb497599cc32597b25fa090124b04d0602b5fa9fe028f36b9f82e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.1 MB (387104175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40609c750253841560e92386eb3ca1579e0f79d6032a894df9adbce3eb17e820`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 24 Mar 2022 22:26:07 GMT
ADD file:8de122754f28308c5a43ec6c9d2e21a84f88ce3d857c57ceebdbb006ec4218ea in / 
# Thu, 24 Mar 2022 22:26:08 GMT
CMD ["/bin/bash"]
# Thu, 24 Mar 2022 22:28:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 24 Mar 2022 22:28:17 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 24 Mar 2022 22:28:43 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Thu, 24 Mar 2022 22:28:44 GMT
ENV PS_VERSION=8.0.27-18.1
# Thu, 24 Mar 2022 22:28:44 GMT
ENV OS_VER=el8
# Thu, 24 Mar 2022 22:28:44 GMT
ENV FULL_PERCONA_VERSION=8.0.27-18.1.el8
# Thu, 24 Mar 2022 22:29:17 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 24 Mar 2022 22:29:19 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 24 Mar 2022 22:29:20 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 24 Mar 2022 22:29:20 GMT
COPY file:fcc7e1ba857456cd0be5e7e73c551fe742d4b08d93a5cc538710f4731b28e602 in /docker-entrypoint.sh 
# Thu, 24 Mar 2022 22:29:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Mar 2022 22:29:20 GMT
USER mysql
# Thu, 24 Mar 2022 22:29:20 GMT
EXPOSE 3306 33060
# Thu, 24 Mar 2022 22:29:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:00e01bb8b231e8861500c644bc1bd18c32cf5bb204a4e618d2bae1dcfee66836`  
		Last Modified: Thu, 24 Mar 2022 22:27:07 GMT  
		Size: 87.5 MB (87478984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca18a40015b8e04c884f29979a8e256d3fbd77612baeb927edb9f0e3e361b5c`  
		Last Modified: Thu, 24 Mar 2022 22:31:21 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6d08cc8f4e2bcdb05c4cc6ed982c58ac0c608e1dd78080520c977b394990e7`  
		Last Modified: Thu, 24 Mar 2022 22:31:30 GMT  
		Size: 137.3 MB (137318899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05edb4e83b4b2d92ec3a4db3a46ac772febaf181d94ab28ecbfcf8ed032a3c32`  
		Last Modified: Thu, 24 Mar 2022 22:31:46 GMT  
		Size: 162.3 MB (162300866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7efe18e4f9c4b1f74e097563d301e5ca46a7b67a307bb3121b5fd01b80c1301`  
		Last Modified: Thu, 24 Mar 2022 22:31:21 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3cafbc522b01a5f8fff47cd552a156dea70c6ec77be9512b774086993208cb`  
		Last Modified: Thu, 24 Mar 2022 22:31:21 GMT  
		Size: 3.1 KB (3088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
