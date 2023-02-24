## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:2baeef3cff160b32d44e37cd6d0e2ec258f7a81d681c705832dfede4c8ea78ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:87c15af2aa26de4320624d38e10ca746cdd45a988a61390df5df03be875704c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178843069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db208a076daba1832c0bfac339771b90a1f38182c5a3d0ab1587a612c882c94a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Feb 2023 00:20:17 GMT
ADD file:5f598291e33fcd7b12df14fa7590698aa2e9e6ca13213106e687967d63b873e9 in / 
# Fri, 24 Feb 2023 00:20:18 GMT
CMD ["/bin/bash"]
# Fri, 24 Feb 2023 00:44:20 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 24 Feb 2023 00:47:43 GMT
ENV PSMDB_VERSION=4.2.21-21
# Fri, 24 Feb 2023 00:47:43 GMT
ENV OS_VER=el8
# Fri, 24 Feb 2023 00:47:44 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Fri, 24 Feb 2023 00:47:44 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 24 Feb 2023 00:47:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Fri, 24 Feb 2023 00:48:25 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 24 Feb 2023 00:48:26 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 24 Feb 2023 00:48:26 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 24 Feb 2023 00:48:27 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 24 Feb 2023 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Fri, 24 Feb 2023 00:48:30 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 24 Feb 2023 00:48:32 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 24 Feb 2023 00:48:32 GMT
VOLUME [/data/db]
# Fri, 24 Feb 2023 00:48:32 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 24 Feb 2023 00:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Feb 2023 00:48:33 GMT
EXPOSE 27017
# Fri, 24 Feb 2023 00:48:33 GMT
USER 1001
# Fri, 24 Feb 2023 00:48:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0ab55f1557cebb691aa3bfcb8c3158e4ae49db126ce68cc3238746c379e091c7`  
		Last Modified: Fri, 24 Feb 2023 00:21:06 GMT  
		Size: 88.4 MB (88424514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7beb4e64ecbf9a9354f37a7a621d61164c5f24556ae18dd2a2a37a6056340`  
		Last Modified: Fri, 24 Feb 2023 00:51:04 GMT  
		Size: 3.8 MB (3765553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2197b721f6cd79bc7426179545a22736cce4642453f3e3dec28a4bd2ebe57da1`  
		Last Modified: Fri, 24 Feb 2023 00:51:12 GMT  
		Size: 77.6 MB (77580158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b6227cbdb9061b641a2d5a1c46d6adedfabe0c5cf5048ad705528af5dfa4cd`  
		Last Modified: Fri, 24 Feb 2023 00:51:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fce49e1b7b69b39943448ed5a793c4104a63a9f166021f36ce9a047e595ca5`  
		Last Modified: Fri, 24 Feb 2023 00:51:01 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc315b649e5e2cf97b1b511ce13c831f5ec4bf3fc4af14958c090db082e2b58`  
		Last Modified: Fri, 24 Feb 2023 00:51:01 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d1ed798f982fdfa76c18982fff4e3b097d033ea8c2a9a23664c99c8091baa`  
		Last Modified: Fri, 24 Feb 2023 00:51:01 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57a34c43542df0b2039068180c6eb9b5cb7df7731dc6cca068017554540fc32`  
		Last Modified: Fri, 24 Feb 2023 00:51:02 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd5666b8a92a4165963525c215e4459b0c39043faa91aa57cf1b6f7c7a5b0de`  
		Last Modified: Fri, 24 Feb 2023 00:51:01 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
