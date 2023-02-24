## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:4654b391952f971b0db07ad7ebe2fa535db6a911fa9ad3c620eeaa3e3dcc1f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:6d4103de988c2f293bbfebd8d00445c4ede5baa937e4358ce28ef796d2b8f66d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213558945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16576139886d5e63b30486858913d498f560abba70c2c6a38715a7b0aa143bae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Feb 2023 00:20:17 GMT
ADD file:5f598291e33fcd7b12df14fa7590698aa2e9e6ca13213106e687967d63b873e9 in / 
# Fri, 24 Feb 2023 00:20:18 GMT
CMD ["/bin/bash"]
# Fri, 24 Feb 2023 00:44:20 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 24 Feb 2023 00:45:50 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Fri, 24 Feb 2023 00:45:50 GMT
ENV PSMDB_VERSION=5.0.10-9
# Fri, 24 Feb 2023 00:45:50 GMT
ENV OS_VER=el8
# Fri, 24 Feb 2023 00:45:50 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Fri, 24 Feb 2023 00:45:50 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 24 Feb 2023 00:46:31 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 24 Feb 2023 00:46:32 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 24 Feb 2023 00:46:32 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 24 Feb 2023 00:46:33 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 24 Feb 2023 00:46:33 GMT
ENV GOSU_VERSION=1.11
# Fri, 24 Feb 2023 00:46:36 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 24 Feb 2023 00:46:39 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 24 Feb 2023 00:46:39 GMT
VOLUME [/data/db]
# Fri, 24 Feb 2023 00:46:40 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 24 Feb 2023 00:46:40 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 24 Feb 2023 00:46:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Feb 2023 00:46:40 GMT
EXPOSE 27017
# Fri, 24 Feb 2023 00:46:41 GMT
USER 1001
# Fri, 24 Feb 2023 00:46:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0ab55f1557cebb691aa3bfcb8c3158e4ae49db126ce68cc3238746c379e091c7`  
		Last Modified: Fri, 24 Feb 2023 00:21:06 GMT  
		Size: 88.4 MB (88424514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7aef72fe99ba75ddb1c703c9dedc79a31751d90959df11cd59075282c34da2`  
		Last Modified: Fri, 24 Feb 2023 00:50:17 GMT  
		Size: 3.8 MB (3765529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca18d60e6e49bf9659b9fdfe71eb41af4c7745a03a7cada846a2799c13fe52f`  
		Last Modified: Fri, 24 Feb 2023 00:50:29 GMT  
		Size: 112.3 MB (112282850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45187234d63e26eeb662c3185ecbede31e8111563f4a27fb8b7ee95a4a95d619`  
		Last Modified: Fri, 24 Feb 2023 00:50:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8167d2a9107fc89a30e251077fe03c86a7f3de1a731a9d053f29372506d306a`  
		Last Modified: Fri, 24 Feb 2023 00:50:16 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c059b697dbd9bcfdeb45dbd90534b2999a5ce7821ad82e3d7e838a9eba6405`  
		Last Modified: Fri, 24 Feb 2023 00:50:14 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3330ee23727db9b9018eb21fa314d73db5e42a0f1d161564e6de541a485f030`  
		Last Modified: Fri, 24 Feb 2023 00:50:14 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2f87611b6527a404c63203c79acd87ea0694eebc7fd85525484f2cfd60df47`  
		Last Modified: Fri, 24 Feb 2023 00:50:15 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11df44d7bfc06fcc3ad4e003e933be3c7642fce740c80e1aa093281dcdedb5ce`  
		Last Modified: Fri, 24 Feb 2023 00:50:14 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c956fc2533f2d9ba2f8d0fdb85a6b1e171286107d865f4c935f34c72403e7bdf`  
		Last Modified: Fri, 24 Feb 2023 00:50:14 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
