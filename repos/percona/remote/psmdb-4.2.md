## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:5e208711a1848112d7a37c252f5e487f08ae1659c38ce96b1a2c83bf40b4234f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:eeea627705d4aa78c44576486be4204f721415661ffeb87c6017ac757fa61d17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176200765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66304f433a53551ed2844aacfdc80da9f1a88450f75f8c8be32e3092fe2ba914`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Jun 2022 17:05:47 GMT
ADD file:48aa8cc19fd94c8679e43b263d7eec6d7f5d19f4288991eb0c68f52c91068a90 in / 
# Wed, 01 Jun 2022 17:05:48 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 18:00:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 01 Jun 2022 18:04:20 GMT
ENV PSMDB_VERSION=4.2.20-20
# Wed, 01 Jun 2022 18:04:20 GMT
ENV OS_VER=el8
# Wed, 01 Jun 2022 18:04:20 GMT
ENV FULL_PERCONA_VERSION=4.2.20-20.el8
# Wed, 01 Jun 2022 18:04:20 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 01 Jun 2022 18:04:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Wed, 01 Jun 2022 18:05:03 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 01 Jun 2022 18:05:04 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 01 Jun 2022 18:05:04 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 01 Jun 2022 18:05:04 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 01 Jun 2022 18:05:05 GMT
ENV GOSU_VERSION=1.11
# Wed, 01 Jun 2022 18:05:07 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 01 Jun 2022 18:05:09 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 01 Jun 2022 18:05:09 GMT
VOLUME [/data/db]
# Wed, 01 Jun 2022 18:05:09 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 01 Jun 2022 18:05:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jun 2022 18:05:10 GMT
EXPOSE 27017
# Wed, 01 Jun 2022 18:05:10 GMT
USER 1001
# Wed, 01 Jun 2022 18:05:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ec2c52e89d2aa80aa01fc0e5f2ca1dc539d07b8f53e020f0c5af0f3e3c482525`  
		Last Modified: Wed, 01 Jun 2022 17:06:38 GMT  
		Size: 84.6 MB (84568422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db32de69e6bff06f4619338f49c3301b0c8ddaaa5e27b6121f84f9cc739b6d2`  
		Last Modified: Wed, 01 Jun 2022 18:08:31 GMT  
		Size: 3.7 MB (3744788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75bd3d494e21c20eed998286a406a1c05cf772e3defcd8744a14c8f1c7f7e9a`  
		Last Modified: Wed, 01 Jun 2022 18:08:40 GMT  
		Size: 78.8 MB (78814711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ca3e4dba59c1a6d2d1621a21964879802eb383d8cc6cb4c2376c4cd0da76f4`  
		Last Modified: Wed, 01 Jun 2022 18:08:30 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bd00578cf8f48a80180c92c7b0dcef34f2ad498f32a1c855e99ec49d18a527`  
		Last Modified: Wed, 01 Jun 2022 18:08:28 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e549e1855d32fa26b34aa2894f2cca5fc79e62593e775c59401bb1bf7c0c9`  
		Last Modified: Wed, 01 Jun 2022 18:08:28 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f023a687209b30938f5d05213232d434eb96ebabf9747851947ad6f2b92d6057`  
		Last Modified: Wed, 01 Jun 2022 18:08:28 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471922f9d4f29d8ea192882a7a53becbf984b6505c4bc7cadad0a36694834d6c`  
		Last Modified: Wed, 01 Jun 2022 18:08:29 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6856d1f33bcc52addfea7c4cb6518e274a64b293147212af9a8f17ab67ec1364`  
		Last Modified: Wed, 01 Jun 2022 18:08:28 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
