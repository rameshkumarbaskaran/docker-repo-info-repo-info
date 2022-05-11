## `percona:psmdb-5.0.8`

```console
$ docker pull percona@sha256:a776090666cf582af39ab1e8c3754d097c4b6cc0bffbcfca919edac3d1b48726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.8` - linux; amd64

```console
$ docker pull percona@sha256:cce07547e3924d89deada69f2368d294cd81212393da27c67fb1e427bc789861
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213691454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8196f080dcb0e2e52b95eb7b3fc6e3651ca33719e860bba97ff1db49a56c2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 02 May 2022 20:50:56 GMT
ADD file:84bf324680059e085907eb7d75c8cb37d4d01aff3cc8241463bbc7d042db93d9 in / 
# Mon, 02 May 2022 20:50:56 GMT
CMD ["/bin/bash"]
# Mon, 02 May 2022 21:18:32 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 02 May 2022 21:19:52 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Wed, 11 May 2022 00:23:11 GMT
ENV PSMDB_VERSION=5.0.8-7
# Wed, 11 May 2022 00:23:11 GMT
ENV OS_VER=el8
# Wed, 11 May 2022 00:23:12 GMT
ENV FULL_PERCONA_VERSION=5.0.8-7.el8
# Wed, 11 May 2022 00:23:12 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 11 May 2022 00:23:54 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 11 May 2022 00:23:55 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 11 May 2022 00:23:55 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 11 May 2022 00:23:55 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 11 May 2022 00:23:55 GMT
ENV GOSU_VERSION=1.11
# Wed, 11 May 2022 00:23:59 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 11 May 2022 00:24:02 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 11 May 2022 00:24:02 GMT
VOLUME [/data/db]
# Wed, 11 May 2022 00:24:03 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 11 May 2022 00:24:03 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 11 May 2022 00:24:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 00:24:03 GMT
EXPOSE 27017
# Wed, 11 May 2022 00:24:03 GMT
USER 1001
# Wed, 11 May 2022 00:24:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:42405d186b2e7939aa51dc1bcc0f4cf0ce1236f4d6e38f2fae9822c41e98078e`  
		Last Modified: Mon, 02 May 2022 20:51:41 GMT  
		Size: 87.5 MB (87479695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acac54c59b32792a2363b5cd85242c5762c2455e2f4e7a2dda2983e394c9c79`  
		Last Modified: Mon, 02 May 2022 21:24:24 GMT  
		Size: 3.8 MB (3759061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe11cbe4303b49a6936220782a8a360acfb5aa9b9d580a16d9936d9b40d6fdc3`  
		Last Modified: Wed, 11 May 2022 00:25:16 GMT  
		Size: 113.4 MB (113366646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfddfd638828714a8a79e0bbbd5bbdb0c16fe5175abdb99841d61daa95f5afd`  
		Last Modified: Wed, 11 May 2022 00:25:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1331032ddd0ad84abd3de9cea903f4f32e10fd37d37c6786f5fbd1ea4637a`  
		Last Modified: Wed, 11 May 2022 00:25:02 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0809c7b41c05c349ad55d06fe747eddadfa0b3547021c81ed4a0abfa57fc9036`  
		Last Modified: Wed, 11 May 2022 00:25:00 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0c5f0417d50cb1c30c0e6a09c04992ec1a18a557748a2c2068c1d9e8f5a616`  
		Last Modified: Wed, 11 May 2022 00:25:00 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef3b9c06e03e7067e9d9b8a9d353a9824933c07fce2c37610a608a879c045f`  
		Last Modified: Wed, 11 May 2022 00:25:01 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5d1d6b1755c139d848ec509cb73451c18954f97b88a7148607c2d19ed32a26`  
		Last Modified: Wed, 11 May 2022 00:25:00 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934a15cd1e44b5f44dfd5ec211fa8d61b490092fcb7ba90f705042e3629ecca4`  
		Last Modified: Wed, 11 May 2022 00:25:00 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
