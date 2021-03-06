## `percona:psmdb-3.6`

```console
$ docker pull percona@sha256:a72d3c22450d4361ae8eb46c4737ecae27e748360adb43de79e31bd3f7dc5ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-3.6` - linux; amd64

```console
$ docker pull percona@sha256:063d6077d9b0fd3b97b9e598d54fbc6c4924203e26cf54f5b2c46ff3c93fae71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159823292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f66a663c8b4e5fd5c6c53e2b286233279a80c8f3001833583bc2244bbc9b5d`
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
# Sat, 06 Mar 2021 01:13:23 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 06 Mar 2021 01:13:23 GMT
ENV PSMDB_VERSION=3.6.22-12.0
# Sat, 06 Mar 2021 01:13:23 GMT
ENV OS_VER=el8
# Sat, 06 Mar 2021 01:13:23 GMT
ENV FULL_PERCONA_VERSION=3.6.22-12.0.el8
# Sat, 06 Mar 2021 01:13:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 06 Mar 2021 01:13:40 GMT
RUN set -ex;     dnf install -y         dnf-utils         shadow-utils         curl         procps-ng         jq         oniguruma         Percona-Server-MongoDB-36-shell-${FULL_PERCONA_VERSION}         Percona-Server-MongoDB-36-mongos-${FULL_PERCONA_VERSION};         repoquery -a --location             policycoreutils                 | xargs curl -Lf -o /tmp/policycoreutils.rpm;         repoquery -a --location             Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}                 | xargs curl -Lf -o /tmp/Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}.rpm;         rpm -iv /tmp/policycoreutils.rpm /tmp/Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}.rpm --nodeps;                 rm -rf /tmp/policycoreutils.rpm /tmp/Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}.rpm;         dnf remove -y dnf-utils;         dnf clean all;         rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;         chown -R 1001:0 /data/db
# Sat, 06 Mar 2021 01:13:41 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Sat, 06 Mar 2021 01:13:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 06 Mar 2021 01:13:42 GMT
RUN cp /usr/share/doc/Percona-Server-MongoDB-36-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 06 Mar 2021 01:13:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 06 Mar 2021 01:13:45 GMT
VOLUME [/data/db]
# Sat, 06 Mar 2021 01:13:45 GMT
COPY file:36bd7798a7bd236f79a692385b6877519fd05ff40f92de87cb1d5c527c35d799 in /entrypoint.sh 
# Sat, 06 Mar 2021 01:13:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Mar 2021 01:13:45 GMT
EXPOSE 27017
# Sat, 06 Mar 2021 01:13:45 GMT
USER 1001
# Sat, 06 Mar 2021 01:13:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8176e0284a0c41f02f78757cacdf88b3f1960714b38d4a744494aa7311865ea`  
		Last Modified: Sat, 06 Mar 2021 01:18:25 GMT  
		Size: 19.4 MB (19434033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbff9f6f55652d7f60784fd6bbdeba54c69ab934ade376cc8a1b953677da203`  
		Last Modified: Sat, 06 Mar 2021 01:18:32 GMT  
		Size: 57.0 MB (57048600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f72d51069a340d68b5e68ee582c2678bc9f96f48e1d5f3cc53e4ca17f1ab8`  
		Last Modified: Sat, 06 Mar 2021 01:18:20 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16932ab507235097304e5ff5b6866678a64c57a1d787fb04ff09fafd46343435`  
		Last Modified: Sat, 06 Mar 2021 01:18:20 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f026c3f0b3355c313a03cff902efc79c6440238c2f4ee80d50b2552bb8d639`  
		Last Modified: Sat, 06 Mar 2021 01:18:20 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322494d314bebae7c22ee754bb2f86b61d366086f7168679928e17513fd38205`  
		Last Modified: Sat, 06 Mar 2021 01:18:22 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d34f9391c585f7a9592d7766501dcf1b814a6bce157f9cf6b9de457c5228d4`  
		Last Modified: Sat, 06 Mar 2021 01:18:20 GMT  
		Size: 4.5 KB (4542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
