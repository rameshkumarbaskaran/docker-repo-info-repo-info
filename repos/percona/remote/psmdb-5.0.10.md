## `percona:psmdb-5.0.10`

```console
$ docker pull percona@sha256:f994e0002d07665044334c1f133dab21f8ee0823f1ddcf128c91be749509e4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.10` - linux; amd64

```console
$ docker pull percona@sha256:93cbea506facd73822b8b14e577be5af3602e4107364b5cedc3d4e6b9ac9ca31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214061480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11887508cc7722a9a5db73315d108f3010e290c7002b1da1f292dd237b65b4a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 24 May 2023 21:20:20 GMT
ADD file:9fa6758e3fa61a51e989e74b7f3adf02abe0e1b0a77e5a2118655b36ec4b9863 in / 
# Wed, 24 May 2023 21:20:20 GMT
CMD ["/bin/bash"]
# Wed, 24 May 2023 21:36:58 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 24 May 2023 21:37:02 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Wed, 24 May 2023 21:37:02 GMT
ENV PSMDB_VERSION=5.0.10-9
# Wed, 24 May 2023 21:37:02 GMT
ENV OS_VER=el8
# Wed, 24 May 2023 21:37:02 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Wed, 24 May 2023 21:37:02 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 24 May 2023 21:37:44 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 24 May 2023 21:37:45 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 24 May 2023 21:37:45 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 24 May 2023 21:37:45 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 24 May 2023 21:37:46 GMT
ENV GOSU_VERSION=1.11
# Wed, 24 May 2023 21:37:48 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 24 May 2023 21:37:51 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 24 May 2023 21:37:51 GMT
VOLUME [/data/db]
# Wed, 24 May 2023 21:37:52 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 24 May 2023 21:37:52 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 24 May 2023 21:37:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 May 2023 21:37:52 GMT
EXPOSE 27017
# Wed, 24 May 2023 21:37:52 GMT
USER 1001
# Wed, 24 May 2023 21:37:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d786df39362960174459800752e5106f3f2ca0fcb3dcb8fd19d47d5be2ec379c`  
		Last Modified: Wed, 24 May 2023 21:21:10 GMT  
		Size: 88.9 MB (88874316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a801d50a0a6ca69954a17d82d014c8166294474b7a1c413bcf7ecb980137288b`  
		Last Modified: Wed, 24 May 2023 21:40:20 GMT  
		Size: 3.8 MB (3790019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2676460bdc65d6a56aefe38ec0789b4a2858b8683f8b2e5cac3074b66fc5e1b`  
		Last Modified: Wed, 24 May 2023 21:40:31 GMT  
		Size: 112.3 MB (112311079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f54d253179c93f9a799cf88464f7c13a04c104b13fe66f85049597cc19ec2ca`  
		Last Modified: Wed, 24 May 2023 21:40:18 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aceaf7b74e79e6f1d72f9c623e4e0593ab6311a03651684b3d33ba77003cab9`  
		Last Modified: Wed, 24 May 2023 21:40:18 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be290fe57986951253129989af766c38504fc8429cf4730c40c88ee072f54694`  
		Last Modified: Wed, 24 May 2023 21:40:16 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22c1690ddc4ff8af4e93372db377f9ec4082200651a85bf853ec9225c84b47d`  
		Last Modified: Wed, 24 May 2023 21:40:17 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a85e3b977fafaea70866a38d5c2937280572b7f92fbe93521635cf1f2d2bec7`  
		Last Modified: Wed, 24 May 2023 21:40:18 GMT  
		Size: 8.1 MB (8137904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e886aa604ee1b5d4e8c7fdb8663a906adc11f1a2dc09b0ede5e7e0251bf6f7d`  
		Last Modified: Wed, 24 May 2023 21:40:16 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633b75dbd9d4e2137f03938f8ec9ae0f970d32093f91d3421ae60ef098a1bcb5`  
		Last Modified: Wed, 24 May 2023 21:40:16 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
