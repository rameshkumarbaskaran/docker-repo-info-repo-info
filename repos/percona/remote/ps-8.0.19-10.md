## `percona:ps-8.0.19-10`

```console
$ docker pull percona@sha256:95b64ef7f23021ea64ca8626bf04d7f9a052aa7481ee1f38e8fda6d5a98dae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-8.0.19-10` - linux; amd64

```console
$ docker pull percona@sha256:30f000dc85bd13397c346bf1e3a228e850a8869b1da00d6e987a2fa7a30fb448
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224496206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e269b673aa2af7f9d8abf157fc1460094bf886f0a4a1887842f45a8cf5d59262`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2020 23:33:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 30 Jan 2020 23:33:00 GMT
RUN groupadd -g 1001 mysql
# Thu, 30 Jan 2020 23:33:01 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Thu, 30 Jan 2020 23:33:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     yum install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release setup ps80
# Mon, 23 Mar 2020 21:20:10 GMT
ENV PERCONA_VERSION=8.0.19-10.1.el7
# Mon, 23 Mar 2020 21:21:02 GMT
RUN set -ex;     yum install -y         percona-server-server-${PERCONA_VERSION}         percona-server-tokudb-${PERCONA_VERSION}         percona-server-devel-${PERCONA_VERSION}         percona-server-rocksdb-${PERCONA_VERSION}         jemalloc         which         policycoreutils;         yum clean all;     rm -rf /var/cache/yum /var/lib/mysql
# Mon, 23 Mar 2020 21:21:03 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Mon, 23 Mar 2020 21:21:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 23 Mar 2020 21:21:04 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Mon, 23 Mar 2020 21:21:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:21:04 GMT
USER mysql
# Mon, 23 Mar 2020 21:21:04 GMT
EXPOSE 3306 33060
# Mon, 23 Mar 2020 21:21:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296eab8cb2767bf28303443e7bc3a4a0cbc14383b23c877b7b8c2f776fdf81b5`  
		Last Modified: Thu, 30 Jan 2020 23:36:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed24ac5fd1f63a28eaf64c5435879cc6199b8433c5f68df137d2c364e1c11a3b`  
		Last Modified: Thu, 30 Jan 2020 23:36:40 GMT  
		Size: 1.6 KB (1569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303807e74badcc2b04a965236de0c98f0a8339a3525041b2cbe9e1b4a0ba16ed`  
		Last Modified: Thu, 30 Jan 2020 23:36:41 GMT  
		Size: 6.4 MB (6438611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b90f167fb2a76e1742630dec20b9071a652cd47b9da24a39e19d1707478b470`  
		Last Modified: Mon, 23 Mar 2020 21:22:09 GMT  
		Size: 142.3 MB (142270573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962beccc99b2c7576801e02694f56db43953528e83fdee44aeb8138742b8de37`  
		Last Modified: Mon, 23 Mar 2020 21:21:42 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c63f042185c82285c5bcd15c1624ab9de38042bca2b66748d7d1d4ef15f737`  
		Last Modified: Mon, 23 Mar 2020 21:21:42 GMT  
		Size: 3.1 KB (3067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
