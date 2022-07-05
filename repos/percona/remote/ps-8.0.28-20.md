## `percona:ps-8.0.28-20`

```console
$ docker pull percona@sha256:7672758885b7e57c929c1fba4cbb8cc71bd4478e1109683a33462a0227a4567c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.28-20` - linux; amd64

```console
$ docker pull percona@sha256:f171893b9e49f6d75b3c23009b4322a928e802e59935a39c58ce63242dc3d45f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411682157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f29e5acb3e955f066fdce3e6a1ce304080252c528414212b4ed3fca3fb2348`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:24 GMT
ADD file:05afe15e1c394de999f38bb2413c80af18f129511261f53511fe21e4606b6353 in / 
# Tue, 05 Jul 2022 22:20:24 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:42:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 05 Jul 2022 22:42:17 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 05 Jul 2022 22:42:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Tue, 05 Jul 2022 22:42:45 GMT
ENV PS_VERSION=8.0.28-20.1
# Tue, 05 Jul 2022 22:42:45 GMT
ENV OS_VER=el8
# Tue, 05 Jul 2022 22:42:45 GMT
ENV FULL_PERCONA_VERSION=8.0.28-20.1.el8
# Tue, 05 Jul 2022 22:43:19 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 05 Jul 2022 22:43:21 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 05 Jul 2022 22:43:21 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 05 Jul 2022 22:43:21 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Tue, 05 Jul 2022 22:43:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:43:22 GMT
USER mysql
# Tue, 05 Jul 2022 22:43:22 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:43:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15a6facc77411902de6b8de2d42125695286cd602d17db01f09239a7f6f8992a`  
		Last Modified: Tue, 05 Jul 2022 22:21:25 GMT  
		Size: 84.6 MB (84566504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b258a01c0dd8c14b90422a55e46eea06a4c23c368c6a0296bf72c6c519d39a99`  
		Last Modified: Tue, 05 Jul 2022 22:46:42 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f727c918d4202f2a2dd57b0779c0625d555b28dd99a88cd61cc9f20fe29546`  
		Last Modified: Tue, 05 Jul 2022 22:46:52 GMT  
		Size: 150.6 MB (150623792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563c23dfc8042de9b5cf633d446f5fd0706b2850aabd2395110ccbd2e5b881e6`  
		Last Modified: Tue, 05 Jul 2022 22:47:09 GMT  
		Size: 176.5 MB (176486431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345cf7d23d45fbc108afddc49d535479077abd645a0861862ace99c3e451ed7`  
		Last Modified: Tue, 05 Jul 2022 22:46:43 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c47f6230566413222ae679265ca4e52cf7ceb00f6937dba022e3de32b45458`  
		Last Modified: Tue, 05 Jul 2022 22:46:43 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
