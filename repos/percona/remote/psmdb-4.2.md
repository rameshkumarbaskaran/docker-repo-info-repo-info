## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:f0e8100a12d3b4ff7acbe8cd33b077dd0d1eb71848a1c634b14819f37c5c4e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:7971912a5ebcded5adbf2460ac3a4ccac26fbda83498cbe3eebc6ac4178672b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176426014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cb4e6d4d9b3b921f455aa20aa64a26edd23ec48d04fcd62ca79fa4ad511819`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 12 Oct 2022 21:20:32 GMT
ADD file:2c7deb13100ea9b7487f0e37a557426c2f4639ed9100b1a0f13b30916ce6bcb4 in / 
# Wed, 12 Oct 2022 21:20:32 GMT
CMD ["/bin/bash"]
# Wed, 12 Oct 2022 21:47:02 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Oct 2022 21:50:27 GMT
ENV PSMDB_VERSION=4.2.21-21
# Wed, 12 Oct 2022 21:50:27 GMT
ENV OS_VER=el8
# Wed, 12 Oct 2022 21:50:27 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Wed, 12 Oct 2022 21:50:27 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 12 Oct 2022 21:50:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Wed, 12 Oct 2022 21:51:06 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 12 Oct 2022 21:51:07 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 12 Oct 2022 21:51:07 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 12 Oct 2022 21:51:08 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 12 Oct 2022 21:51:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 12 Oct 2022 21:51:10 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 12 Oct 2022 21:51:13 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 12 Oct 2022 21:51:13 GMT
VOLUME [/data/db]
# Wed, 12 Oct 2022 21:51:13 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 12 Oct 2022 21:51:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 21:51:13 GMT
EXPOSE 27017
# Wed, 12 Oct 2022 21:51:13 GMT
USER 1001
# Wed, 12 Oct 2022 21:51:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d36fda030a05490a75e03359f0fb6861fc9de2e4ae6dd9631ff0c65bde586bc0`  
		Last Modified: Wed, 12 Oct 2022 21:21:52 GMT  
		Size: 86.0 MB (85968038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dee57872756bd331c93f02f42c28040b5353774e9c6c0ad23d91a99644b602`  
		Last Modified: Wed, 12 Oct 2022 21:53:57 GMT  
		Size: 3.8 MB (3775629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94202d12c20c220a417c2b4e6fdb86e22c3fa8b95f681f7f8fc72a8e6562dd7f`  
		Last Modified: Wed, 12 Oct 2022 21:54:05 GMT  
		Size: 77.6 MB (77609503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e808a547c731a750abf0067d8d00338932b41b6510661e8197dbb10e5eca7535`  
		Last Modified: Wed, 12 Oct 2022 21:53:56 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccb5526489522c9eb93094a95f2bbcf41c9cc89c81bc5cb00466fae8bbe7d`  
		Last Modified: Wed, 12 Oct 2022 21:53:54 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df291232996b7eac69eff38a7e4a698a6570cb14292abdd31b1c278a6fe28d6`  
		Last Modified: Wed, 12 Oct 2022 21:53:54 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced2f4fb0c959c7a74a36a8faed7174fc5d4583ba87bd356e0ce65baefe154c1`  
		Last Modified: Wed, 12 Oct 2022 21:53:54 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9829f2896ed8058314ae48b2058f0b1d00e226e7c82d134f75bf3084f70b462`  
		Last Modified: Wed, 12 Oct 2022 21:53:55 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bf6877532d17ce54cc246504a7125749a029b4d188156809228603fd6a26f4`  
		Last Modified: Wed, 12 Oct 2022 21:53:54 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
