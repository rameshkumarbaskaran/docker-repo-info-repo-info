## `percona:ps-8.0.29-21`

```console
$ docker pull percona@sha256:7a83f0054a83c75d429c07f7c0e5a1f41c072e514254c3ad206f593edb80926a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.29-21` - linux; amd64

```console
$ docker pull percona@sha256:b2b0df41a3a7b5908f6f03f40ca1389e47b613a4eb8deec01e858ef26587753c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.7 MB (423664386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37fa45c6abd5b9512a791579852467c6675b42bf5167e6d0bf73d6221d0c6b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Oct 2022 21:20:32 GMT
ADD file:2c7deb13100ea9b7487f0e37a557426c2f4639ed9100b1a0f13b30916ce6bcb4 in / 
# Wed, 12 Oct 2022 21:20:32 GMT
CMD ["/bin/bash"]
# Wed, 12 Oct 2022 21:47:02 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Oct 2022 21:47:03 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 12 Oct 2022 21:47:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Wed, 12 Oct 2022 21:47:34 GMT
ENV PS_VERSION=8.0.29-21.1
# Wed, 12 Oct 2022 21:47:35 GMT
ENV OS_VER=el8
# Wed, 12 Oct 2022 21:47:35 GMT
ENV FULL_PERCONA_VERSION=8.0.29-21.1.el8
# Wed, 12 Oct 2022 21:48:10 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 12 Oct 2022 21:48:12 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 12 Oct 2022 21:48:12 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Oct 2022 21:48:12 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Wed, 12 Oct 2022 21:48:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Oct 2022 21:48:13 GMT
USER mysql
# Wed, 12 Oct 2022 21:48:13 GMT
EXPOSE 3306 33060
# Wed, 12 Oct 2022 21:48:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d36fda030a05490a75e03359f0fb6861fc9de2e4ae6dd9631ff0c65bde586bc0`  
		Last Modified: Wed, 12 Oct 2022 21:21:52 GMT  
		Size: 86.0 MB (85968038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebaebe50f42e79dcb3215e3b75da248fbebc3718aca266131b4ac0079f09b0f`  
		Last Modified: Wed, 12 Oct 2022 21:51:55 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d1b33580618f1fb6bd16bb5beb7a034b6b505e565edc973396951f101b1046`  
		Last Modified: Wed, 12 Oct 2022 21:52:05 GMT  
		Size: 159.2 MB (159221730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af01e24251be98e927111530309842421a19aceb3b9799c101566e66fe321e0`  
		Last Modified: Wed, 12 Oct 2022 21:52:22 GMT  
		Size: 178.5 MB (178469195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53babf7f8f2cbaf557f3190d71323fc0b0776852cfcafcc67f44724adf937a5a`  
		Last Modified: Wed, 12 Oct 2022 21:51:55 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84a0bac90d702d17234212a360ddf597e012e0a9f79e1f5fb5f09c04fc6856c`  
		Last Modified: Wed, 12 Oct 2022 21:51:55 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
