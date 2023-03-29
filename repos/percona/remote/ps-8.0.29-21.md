## `percona:ps-8.0.29-21`

```console
$ docker pull percona@sha256:0c9ee56f9a5760d61a9b077d34a2a3a85e4ad994b98f29ed50fad72df9d9c4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.29-21` - linux; amd64

```console
$ docker pull percona@sha256:3402647da22b5492321276b9d3094a8846ecd5065cbea068b60397c2920b4ce5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.1 MB (444141784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a328b0eafdd781050236d1f341fa2d167ce884a08ef4d57c17e60a77261f9b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:26 GMT
ADD file:727407c52e11ec0d0d70de3b26944ebac2213dd17723ae375a55557b4b5968fc in / 
# Wed, 29 Mar 2023 00:21:27 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:46:28 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 29 Mar 2023 00:46:29 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 29 Mar 2023 00:47:02 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Wed, 29 Mar 2023 00:47:02 GMT
ENV PS_VERSION=8.0.29-21.1
# Wed, 29 Mar 2023 00:47:02 GMT
ENV OS_VER=el8
# Wed, 29 Mar 2023 00:47:02 GMT
ENV FULL_PERCONA_VERSION=8.0.29-21.1.el8
# Wed, 29 Mar 2023 00:47:37 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 29 Mar 2023 00:47:39 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 29 Mar 2023 00:47:39 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 29 Mar 2023 00:47:39 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Wed, 29 Mar 2023 00:47:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:47:39 GMT
USER mysql
# Wed, 29 Mar 2023 00:47:40 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:47:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f060192256a938b97a2f291b041c8c46b60220b4a2bf48c91f4339976bb3703b`  
		Last Modified: Wed, 29 Mar 2023 00:22:46 GMT  
		Size: 88.4 MB (88436352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e629035fdc84d18e06d6ce8a81c13f4ca3252a3740ec0481c7e3d97970ee609a`  
		Last Modified: Wed, 29 Mar 2023 00:51:00 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d6897c108fce0ce843ccb06f3895ed0ff2ef660b69d1f782c1d7506d263561`  
		Last Modified: Wed, 29 Mar 2023 00:51:09 GMT  
		Size: 176.2 MB (176234020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1677ab56b93156731f1dc75099c04b9a2c0d7cb480501ff894f6b6afd4971a7f`  
		Last Modified: Wed, 29 Mar 2023 00:51:24 GMT  
		Size: 179.5 MB (179465992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49bc1db2d46c411b6313a5bbb1205e53e0882978b38f678541c0d64952a80d6`  
		Last Modified: Wed, 29 Mar 2023 00:51:00 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf31143e647d8a184e2b730d6738c0c97c2f79fd989717748480bf1b9629b9a`  
		Last Modified: Wed, 29 Mar 2023 00:50:59 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
