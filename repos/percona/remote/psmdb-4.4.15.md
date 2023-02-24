## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:d1297dd011435ddeefe13982fb876cf3b000e4ee73fa6818c6c02dd800e0c2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:18360fc4e7a07207abb636852d2aee1979bb4c19510e5fea851b15d8ababd966
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198161454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f1d7f380bb867abd42f1f39bb3a217858c88d924ac28662a1c665ee7529cc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Feb 2023 00:20:17 GMT
ADD file:5f598291e33fcd7b12df14fa7590698aa2e9e6ca13213106e687967d63b873e9 in / 
# Fri, 24 Feb 2023 00:20:18 GMT
CMD ["/bin/bash"]
# Fri, 24 Feb 2023 00:44:20 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 24 Feb 2023 00:46:48 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Fri, 24 Feb 2023 00:46:48 GMT
ENV PSMDB_VERSION=4.4.15-15
# Fri, 24 Feb 2023 00:46:48 GMT
ENV OS_VER=el8
# Fri, 24 Feb 2023 00:46:48 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Fri, 24 Feb 2023 00:46:48 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 24 Feb 2023 00:47:28 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 24 Feb 2023 00:47:29 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 24 Feb 2023 00:47:29 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 24 Feb 2023 00:47:29 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 24 Feb 2023 00:47:30 GMT
ENV GOSU_VERSION=1.11
# Fri, 24 Feb 2023 00:47:32 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 24 Feb 2023 00:47:34 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 24 Feb 2023 00:47:35 GMT
VOLUME [/data/db]
# Fri, 24 Feb 2023 00:47:35 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 24 Feb 2023 00:47:35 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 24 Feb 2023 00:47:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Feb 2023 00:47:36 GMT
EXPOSE 27017
# Fri, 24 Feb 2023 00:47:36 GMT
USER 1001
# Fri, 24 Feb 2023 00:47:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0ab55f1557cebb691aa3bfcb8c3158e4ae49db126ce68cc3238746c379e091c7`  
		Last Modified: Fri, 24 Feb 2023 00:21:06 GMT  
		Size: 88.4 MB (88424514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe212a6e8f5352e9ef560e6ddfbf9e180ac74b9ebf5243ca612da377c9aaafc`  
		Last Modified: Fri, 24 Feb 2023 00:50:42 GMT  
		Size: 3.8 MB (3765525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27460fa2371662410c291892de544aa1e6df8c96aeef7c798136ba78ef329b15`  
		Last Modified: Fri, 24 Feb 2023 00:50:52 GMT  
		Size: 96.9 MB (96885363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd40a4cefc2dfd272901ce1bb54e75ae200a73f7e3c80f67a7e329817ee0eceb`  
		Last Modified: Fri, 24 Feb 2023 00:50:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0672d8d7526e2656b18b94f105cd55e03532346d394a9559a172bdae3eb562`  
		Last Modified: Fri, 24 Feb 2023 00:50:40 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c872fa91ef37ef62d66ccbfc84a89eaaf0c267c5cee0f3995160088e11f9e3e3`  
		Last Modified: Fri, 24 Feb 2023 00:50:38 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b546d38fb6aac7c8fa313bf7eb8d5c7be5968a95a8053e4014ea61098bb3c08`  
		Last Modified: Fri, 24 Feb 2023 00:50:39 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a123b8aa6374372285bd1b7e280e365aedb9e6394ed590b932f9d98dd8a91c`  
		Last Modified: Fri, 24 Feb 2023 00:50:40 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddbc7b42a98794fc05947a3332f1265142552d60385c691ac2c1d4a48ba963c`  
		Last Modified: Fri, 24 Feb 2023 00:50:38 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4ae8dca663192d16731192e2288acdd38b8d6612afcde6bbbc91ee476d4d60`  
		Last Modified: Fri, 24 Feb 2023 00:50:38 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
