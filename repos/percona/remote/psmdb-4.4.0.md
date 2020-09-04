## `percona:psmdb-4.4.0`

```console
$ docker pull percona@sha256:76d0a39e5f27563e6550bec3d05c54cd0167c55f0e5a2c98eb7b1d63f326eeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-4.4.0` - linux; amd64

```console
$ docker pull percona@sha256:cf67aefa641eee02a12914fba9af876820ccb4559d5ec79ff1b05db0766b4ed7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180653878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710e2969fbcc3db74bc2c95ab55b71c758bf00ea8803ec20311d09737783b3dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.schema-version=1.0
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.name=Percona Server for MongoDB
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.vendor=Percona
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.description=Percona Server for MongoDB is our free and open-source drop-in replacement for MongoDB Community Edition. It offers all the features and benefits of MongoDB Community Edition, plus additional enterprise-grade functionality.
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.license=SSPLv1
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.opencontainers.image.title=Percona Server for MongoDB
# Fri, 04 Sep 2020 19:25:42 GMT
LABEL org.opencontainers.image.vendor=Percona
# Fri, 04 Sep 2020 19:25:42 GMT
LABEL org.opencontainers.image.description=Percona Server for MongoDB is our free and open-source drop-in replacement for MongoDB Community Edition. It offers all the features and benefits of MongoDB Community Edition, plus additional enterprise-grade functionality.
# Fri, 04 Sep 2020 19:25:42 GMT
LABEL org.opencontainers.image.license=SSPLv1
# Fri, 04 Sep 2020 19:25:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 04 Sep 2020 19:25:42 GMT
ENV PSMDB_VERSION=4.4.0-1
# Fri, 04 Sep 2020 19:25:42 GMT
ENV OS_VER=el8
# Fri, 04 Sep 2020 19:25:43 GMT
ENV FULL_PERCONA_VERSION=4.4.0-1.el8
# Fri, 04 Sep 2020 19:25:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 04 Sep 2020 19:25:43 GMT
LABEL org.label-schema.schema-version=4.4.0-1
# Fri, 04 Sep 2020 19:25:43 GMT
LABEL org.opencontainers.image.version=4.4.0-1
# Fri, 04 Sep 2020 19:25:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Fri, 04 Sep 2020 19:26:08 GMT
RUN set -ex;     dnf install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         oniguruma         jq         dnf-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     dnf clean all;     dnf -y remove dnf-utils;     rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 04 Sep 2020 19:26:08 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 04 Sep 2020 19:26:09 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 04 Sep 2020 19:26:09 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 04 Sep 2020 19:26:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 04 Sep 2020 19:26:12 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 04 Sep 2020 19:26:14 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 04 Sep 2020 19:26:14 GMT
COPY file:1e164890dbc426ff0038117af76a47815ae534b64e95a15a83e6e5d7f79a4d77 in /entrypoint.sh 
# Fri, 04 Sep 2020 19:26:14 GMT
VOLUME [/data/db]
# Fri, 04 Sep 2020 19:26:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 04 Sep 2020 19:26:15 GMT
EXPOSE 27017
# Fri, 04 Sep 2020 19:26:15 GMT
USER 1001
# Fri, 04 Sep 2020 19:26:15 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2f3cb101c12c3cdc68c57fe58ba793d84589ec48fe556f029af583d49fd251`  
		Last Modified: Fri, 04 Sep 2020 19:26:50 GMT  
		Size: 18.5 MB (18483550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e75c4a852585b5b4a7c8e417b47c4fbeaaaf810d087d53f10540924b756456c`  
		Last Modified: Fri, 04 Sep 2020 19:27:00 GMT  
		Size: 78.2 MB (78229025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb021baf74ad34bbb3003e7750e790785016e2fee7b6c25ed3ccee3d6238b5ce`  
		Last Modified: Fri, 04 Sep 2020 19:26:48 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f492105672b79ccd19b7ac51f9767bad906ea1f2d1c1b4bb798f6b8080bf2798`  
		Last Modified: Fri, 04 Sep 2020 19:26:47 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0203f2a6182f0cdfaf67b4e2b199a4ce0d1a869d1eb87dc04a7f098434cc3`  
		Last Modified: Fri, 04 Sep 2020 19:26:47 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b55da8540d6366286f5dad5a925c067fe036eda1c87711ba180be81e636d44`  
		Last Modified: Fri, 04 Sep 2020 19:26:47 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c0f4ce97284942e50943ab07b796c13456fdff5395573e5e48e712efe7f555`  
		Last Modified: Fri, 04 Sep 2020 19:26:48 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cab2aee661afc5c386c7e7bd174db7cb84927ef88fd7c700485dd3586876d3`  
		Last Modified: Fri, 04 Sep 2020 19:26:47 GMT  
		Size: 4.5 KB (4544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
