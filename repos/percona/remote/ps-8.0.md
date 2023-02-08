## `percona:ps-8.0`

```console
$ docker pull percona@sha256:4afc66b1fd8ae88b354de80862827897d0750c3cf77e4558e6817af9488ce267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:6c635c96ee706b09aae3d25262da36849a6a59260cd853026fe60765096ddab5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.2 MB (440210315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf60f2b50505bebdcc82e9bc3cbe4bcf64294ac8333c77b8f538eefeebf1d832`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:18 GMT
ADD file:345fe34a9ba268db9f89b4c0a24f29fee1910b875b520412a6d6ad5d94e1c29c in / 
# Wed, 08 Feb 2023 19:27:19 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:52:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Feb 2023 19:52:38 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 08 Feb 2023 19:53:11 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Wed, 08 Feb 2023 19:53:11 GMT
ENV PS_VERSION=8.0.29-21.1
# Wed, 08 Feb 2023 19:53:11 GMT
ENV OS_VER=el8
# Wed, 08 Feb 2023 19:53:11 GMT
ENV FULL_PERCONA_VERSION=8.0.29-21.1.el8
# Wed, 08 Feb 2023 19:53:46 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 08 Feb 2023 19:53:49 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 08 Feb 2023 19:53:49 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Feb 2023 19:53:49 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Wed, 08 Feb 2023 19:53:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Feb 2023 19:53:49 GMT
USER mysql
# Wed, 08 Feb 2023 19:53:49 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 19:53:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:96ce6f03051e96688aa6d88b3c4959386deafef4048331e1b8f48bd9062e1571`  
		Last Modified: Wed, 08 Feb 2023 19:28:46 GMT  
		Size: 88.4 MB (88416695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3fdeeb7193dd0f4b8b968f5f8000b92c12e1b40142db474e523bd8b14423f3`  
		Last Modified: Wed, 08 Feb 2023 19:57:38 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12611dc3dfb6e5d91317bcaf0a1b30cc92596659e21d3a1721ac44658c1e4347`  
		Last Modified: Wed, 08 Feb 2023 19:57:48 GMT  
		Size: 173.4 MB (173427002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b2daa861a9f1812b4fe62134049b24088cbdf9e6bb14e25b2b41f3997dffc`  
		Last Modified: Wed, 08 Feb 2023 19:58:04 GMT  
		Size: 178.4 MB (178361191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbd9ebf4e98fd13838634a83af05149d2205705d31b01bbe1aebb30ce006b31`  
		Last Modified: Wed, 08 Feb 2023 19:57:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04aa35b06c45d52eedd5db0be982d8e925f0b37ca84c797a7b7858bd0eb3d33e`  
		Last Modified: Wed, 08 Feb 2023 19:57:38 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
