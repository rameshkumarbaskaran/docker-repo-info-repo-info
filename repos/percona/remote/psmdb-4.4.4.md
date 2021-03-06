## `percona:psmdb-4.4.4`

```console
$ docker pull percona@sha256:2b958c2305038a92ba26b3e09ee6c5acf6940e1f1ebf41b136f26671a72964ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-4.4.4` - linux; amd64

```console
$ docker pull percona@sha256:3855f01242af229df48fc2e25d91d3c75e7c1c55fcb0672552a61aa5196e4626
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200326846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022632a287c73d6bba30048d50504a5fe4790e405262376848b13a21f271619`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 01:08:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 06 Mar 2021 01:11:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Sat, 06 Mar 2021 01:11:09 GMT
ENV PSMDB_VERSION=4.4.4-6
# Sat, 06 Mar 2021 01:11:09 GMT
ENV OS_VER=el8
# Sat, 06 Mar 2021 01:11:10 GMT
ENV FULL_PERCONA_VERSION=4.4.4-6.el8
# Sat, 06 Mar 2021 01:11:10 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 06 Mar 2021 01:11:34 GMT
RUN set -ex;     dnf install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         oniguruma         jq         dnf-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     dnf clean all;     dnf -y remove dnf-utils;     rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 06 Mar 2021 01:11:36 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Sat, 06 Mar 2021 01:11:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 06 Mar 2021 01:11:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 06 Mar 2021 01:11:37 GMT
ENV GOSU_VERSION=1.11
# Sat, 06 Mar 2021 01:11:41 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 06 Mar 2021 01:11:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 06 Mar 2021 01:11:45 GMT
COPY file:1e164890dbc426ff0038117af76a47815ae534b64e95a15a83e6e5d7f79a4d77 in /entrypoint.sh 
# Sat, 06 Mar 2021 01:11:45 GMT
VOLUME [/data/db]
# Sat, 06 Mar 2021 01:11:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Mar 2021 01:11:45 GMT
EXPOSE 27017
# Sat, 06 Mar 2021 01:11:45 GMT
USER 1001
# Sat, 06 Mar 2021 01:11:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c19d5477b917e9aca5ec7c79025855d9b4f3e6d8ad363dab7aa269834ec222`  
		Last Modified: Sat, 06 Mar 2021 01:17:06 GMT  
		Size: 19.4 MB (19434174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f23d71b091dfbae759954870dcb79903f277eee07f7f2f38c67f3b6bf7b8d6`  
		Last Modified: Sat, 06 Mar 2021 01:17:17 GMT  
		Size: 96.6 MB (96637439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adf7fa84ba4c1a9148df59d0a327674023ca1231e995837269d825f63fe2bb6`  
		Last Modified: Sat, 06 Mar 2021 01:17:03 GMT  
		Size: 1.5 KB (1548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56014f467bc4bb08a63e10eab8db82e7e84af097723ba14602d9d8ea65187009`  
		Last Modified: Sat, 06 Mar 2021 01:17:00 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f16f798b4ea8295cd51788046bb49cf717471f3b0d50c73eb677e15322acd6`  
		Last Modified: Sat, 06 Mar 2021 01:17:01 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a50bdbc9e73881b96a367b6dce60d0bd4b8b41c92bbbc7feac758c3fe2f9e9`  
		Last Modified: Sat, 06 Mar 2021 01:17:04 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da0eeef0cdb8ed8501bc9a5590a95f4d12676622beac246ee00e8d358e247df`  
		Last Modified: Sat, 06 Mar 2021 01:17:02 GMT  
		Size: 8.1 MB (8137909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb5ef9fd15e3c9199bf2e583eefa64bd39383ef8f14605cc79f64361180c443`  
		Last Modified: Sat, 06 Mar 2021 01:17:00 GMT  
		Size: 4.5 KB (4544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
