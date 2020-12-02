## `percona:psmdb-3.6`

```console
$ docker pull percona@sha256:a19fdb91f51ae4847d634b9059e525e4d268fe5e3e650ee898c69a6f70e07d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-3.6` - linux; amd64

```console
$ docker pull percona@sha256:382298887cdacf669c3900a95fd4f4af7f00f23a4411735542688f869df660df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157990711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a79f21e347a50d2add7d417a4923cda153c5b4e6f37a676d9a94412b9bc3ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Mon, 16 Nov 2020 19:39:12 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 02 Dec 2020 00:04:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 02 Dec 2020 00:04:49 GMT
ENV PSMDB_VERSION=3.6.21-10.0
# Wed, 02 Dec 2020 00:04:50 GMT
ENV OS_VER=el8
# Wed, 02 Dec 2020 00:04:50 GMT
ENV FULL_PERCONA_VERSION=3.6.21-10.0.el8
# Wed, 02 Dec 2020 00:04:50 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 02 Dec 2020 00:05:37 GMT
RUN set -ex;     dnf install -y         dnf-utils         shadow-utils         curl         procps-ng         jq         oniguruma         Percona-Server-MongoDB-36-shell-${FULL_PERCONA_VERSION}         Percona-Server-MongoDB-36-mongos-${FULL_PERCONA_VERSION};         repoquery -a --location             policycoreutils                 | xargs curl -Lf -o /tmp/policycoreutils.rpm;         repoquery -a --location             Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}                 | xargs curl -Lf -o /tmp/Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}.rpm;         rpm -iv /tmp/policycoreutils.rpm /tmp/Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}.rpm --nodeps;                 rm -rf /tmp/policycoreutils.rpm /tmp/Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}.rpm;         dnf remove -y dnf-utils;         dnf clean all;         rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;         chown -R 1001:0 /data/db
# Wed, 02 Dec 2020 00:05:38 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 02 Dec 2020 00:05:39 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 02 Dec 2020 00:05:40 GMT
RUN cp /usr/share/doc/Percona-Server-MongoDB-36-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 02 Dec 2020 00:05:42 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 02 Dec 2020 00:05:42 GMT
VOLUME [/data/db]
# Wed, 02 Dec 2020 00:05:42 GMT
COPY file:36bd7798a7bd236f79a692385b6877519fd05ff40f92de87cb1d5c527c35d799 in /entrypoint.sh 
# Wed, 02 Dec 2020 00:05:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 00:05:43 GMT
EXPOSE 27017
# Wed, 02 Dec 2020 00:05:43 GMT
USER 1001
# Wed, 02 Dec 2020 00:05:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa1d8e958e720d06c8b4bd568c3893efe01cbc0ab813c5f4709cb4c2ac612a2`  
		Last Modified: Wed, 02 Dec 2020 00:06:46 GMT  
		Size: 18.5 MB (18495761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b271426e34d8c29edf36a53265e30ad898ed2e899452b75d2aceee023291d31`  
		Last Modified: Wed, 02 Dec 2020 00:06:57 GMT  
		Size: 56.5 MB (56468205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d853919d0fce4e48fc29ae40c417a3dd34fc00a1e79b9f3501d69f336c65ed`  
		Last Modified: Wed, 02 Dec 2020 00:06:42 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfa702a0e9759449cdc2fbfa86f911ac208ba5474c77a7d86ac45e23bbfb5f8`  
		Last Modified: Wed, 02 Dec 2020 00:06:42 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc9139665173c685fdcce9f39cce3433d51b2559ec92bc185c08c71a9d17eb0`  
		Last Modified: Wed, 02 Dec 2020 00:06:42 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a5e9f40ed1570c071421535c5a0cc71cb33d6fc0590fd716de99390e5bb6bf`  
		Last Modified: Wed, 02 Dec 2020 00:06:45 GMT  
		Size: 8.1 MB (8137885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873d40ebc4a5830d12f93cf40ed95dd64a97b0e521187ad837b59e3e8927820`  
		Last Modified: Wed, 02 Dec 2020 00:06:43 GMT  
		Size: 4.5 KB (4543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
