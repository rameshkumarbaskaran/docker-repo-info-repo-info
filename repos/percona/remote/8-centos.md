## `percona:8-centos`

```console
$ docker pull percona@sha256:2e8a863d166b043470ec2be07da2d3d7eb8c04a03f408b1b417b77c042dfadde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:3a3e9a916063a81a842255d8b677b3e9c45ad20d16bd26e4e308f40821a9d508
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383052355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18daf83726a941be811ffd00f9b6469c810d10898931ff4e3025814651e1e464`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 09 Aug 2023 22:20:38 GMT
ADD file:3bf7b15ac2bdaf92627b391a1b57ce768c85c6a8ad9a7daa8c05a86a8d3ae187 in / 
# Wed, 09 Aug 2023 22:20:39 GMT
CMD ["/bin/bash"]
# Wed, 09 Aug 2023 22:38:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 09 Aug 2023 22:38:58 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 09 Aug 2023 22:38:58 GMT
ENV PS_VERSION=8.0.33-25.1
# Wed, 09 Aug 2023 22:38:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Wed, 09 Aug 2023 22:38:58 GMT
ENV OS_VER=el9
# Wed, 09 Aug 2023 22:38:58 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Wed, 09 Aug 2023 22:38:58 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Wed, 09 Aug 2023 22:38:58 GMT
ENV PS_REPO=testing
# Wed, 09 Aug 2023 22:39:01 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 09 Aug 2023 22:39:52 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 09 Aug 2023 22:39:56 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 09 Aug 2023 22:39:57 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 09 Aug 2023 22:39:57 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Wed, 09 Aug 2023 22:39:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 09 Aug 2023 22:39:57 GMT
USER mysql
# Wed, 09 Aug 2023 22:39:57 GMT
EXPOSE 3306 33060
# Wed, 09 Aug 2023 22:39:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ddbe763672c63d02bc8f1cf38a192f5dd0279d733ac8dd1e1ac188c26b0137c`  
		Last Modified: Wed, 09 Aug 2023 22:21:49 GMT  
		Size: 88.0 MB (87963363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ee6ede7325b2fb60070c216792f89b265f962ced9680467bfda599d86d4f4f`  
		Last Modified: Wed, 09 Aug 2023 22:40:40 GMT  
		Size: 1.6 KB (1629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7740bd0f93b41d2c8277b952134399e7589c058512174de29c5e5a964f6421ba`  
		Last Modified: Wed, 09 Aug 2023 22:40:41 GMT  
		Size: 7.3 MB (7330665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da338f6e39e51376e6028d4a90268b14000ebcda4843571dd8ac88e70894fe78`  
		Last Modified: Wed, 09 Aug 2023 22:41:19 GMT  
		Size: 287.8 MB (287752441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d4c17e304c12ee8c7ecc1c47c5a4692276f07076ebb4be0f1a1cbd5ed7333a`  
		Last Modified: Wed, 09 Aug 2023 22:40:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6f706f823b779e2f55824fa936af7ff827a2ee8ac77b8195db042a71bd36c`  
		Last Modified: Wed, 09 Aug 2023 22:40:40 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
