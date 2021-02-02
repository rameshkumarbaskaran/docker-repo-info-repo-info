## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:a09c214c83518b975700a0fd2a27e770d5d4774a20e9b89fe969361964c396b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:30eb0671e148351c94d7c14f94979b7f615d6309d7dc4e62708840ed48c831c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200313722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56f28a168f65096821f9493308543a1e404138fdefe6713d2004aed7077c1d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 08 Dec 2020 00:48:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 21 Dec 2020 20:52:15 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Tue, 02 Feb 2021 02:17:01 GMT
ENV PSMDB_VERSION=4.4.3-5
# Tue, 02 Feb 2021 02:17:02 GMT
ENV OS_VER=el8
# Tue, 02 Feb 2021 02:17:02 GMT
ENV FULL_PERCONA_VERSION=4.4.3-5.el8
# Tue, 02 Feb 2021 02:17:02 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 02 Feb 2021 02:17:37 GMT
RUN set -ex;     dnf install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         oniguruma         jq         dnf-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     dnf clean all;     dnf -y remove dnf-utils;     rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 02 Feb 2021 02:17:38 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 02 Feb 2021 02:17:38 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 02 Feb 2021 02:17:39 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 02 Feb 2021 02:17:39 GMT
ENV GOSU_VERSION=1.11
# Tue, 02 Feb 2021 02:17:42 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 02 Feb 2021 02:17:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 02 Feb 2021 02:17:44 GMT
COPY file:1e164890dbc426ff0038117af76a47815ae534b64e95a15a83e6e5d7f79a4d77 in /entrypoint.sh 
# Tue, 02 Feb 2021 02:17:44 GMT
VOLUME [/data/db]
# Tue, 02 Feb 2021 02:17:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Feb 2021 02:17:44 GMT
EXPOSE 27017
# Tue, 02 Feb 2021 02:17:45 GMT
USER 1001
# Tue, 02 Feb 2021 02:17:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2acf9799d0998bd2c0650b3450cdfa5c5a4dd09a53a5d2107305b0e99b208b8`  
		Last Modified: Mon, 21 Dec 2020 20:58:18 GMT  
		Size: 19.5 MB (19481136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be45162f63f6b96b82e92bd9872c6360d28e921c29089175b1ff5135de42f5d`  
		Last Modified: Tue, 02 Feb 2021 02:19:00 GMT  
		Size: 96.6 MB (96577404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb45148c3ae37f22062bdef25a3a38f7fb3fbd6644608c7701970424d424f64f`  
		Last Modified: Tue, 02 Feb 2021 02:18:45 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf5ed8c5b1f23d8df2648229243e90ad020be2dc0df89f25dff07209503a1fc`  
		Last Modified: Tue, 02 Feb 2021 02:18:45 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75ada0f6c49845565be69dea6d0393a387a525ae3f66c527f498bd124ecf9fd`  
		Last Modified: Tue, 02 Feb 2021 02:18:46 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169c8e02832c39bebb549462da84ec7a49ffcf173611b8051e7c7b6a85f2d815`  
		Last Modified: Tue, 02 Feb 2021 02:18:45 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97ad666fb33f6d96ddb8709395f7afc61d17c3b3189d2f567165284ef31b028`  
		Last Modified: Tue, 02 Feb 2021 02:18:56 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ed30031fdabe29eaa40e1f6211ea4fcb8b2eb8b10288f61a1d4cfd83f3885`  
		Last Modified: Tue, 02 Feb 2021 02:18:44 GMT  
		Size: 4.5 KB (4544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
