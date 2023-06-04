## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:c71c8b1393a18e3bec343c1ade319179355d23256e6ab8795e55fd3d140c319b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:4f018a6af44d8dd91564c047a8e47da22601309ccac82b822d85ad7f06a9c0e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198664157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab9ec138df2a6d7cdad1570dbb29f27a0a164d84798f4c9181ccbfbeddf31a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sun, 04 Jun 2023 17:54:21 GMT
ADD file:7d5910516ba3a0fdff1b226873dd448ed4e09ac326aecf5969218af0c0ef16c4 in / 
# Sun, 04 Jun 2023 17:54:22 GMT
CMD ["/bin/bash"]
# Sun, 04 Jun 2023 18:56:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sun, 04 Jun 2023 18:57:11 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Sun, 04 Jun 2023 18:57:11 GMT
ENV PSMDB_VERSION=4.4.15-15
# Sun, 04 Jun 2023 18:57:12 GMT
ENV OS_VER=el8
# Sun, 04 Jun 2023 18:57:12 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Sun, 04 Jun 2023 18:57:12 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sun, 04 Jun 2023 18:57:53 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sun, 04 Jun 2023 18:57:54 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Sun, 04 Jun 2023 18:57:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sun, 04 Jun 2023 18:57:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sun, 04 Jun 2023 18:57:54 GMT
ENV GOSU_VERSION=1.11
# Sun, 04 Jun 2023 18:57:57 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sun, 04 Jun 2023 18:57:59 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sun, 04 Jun 2023 18:57:59 GMT
VOLUME [/data/db]
# Sun, 04 Jun 2023 18:58:00 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sun, 04 Jun 2023 18:58:00 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sun, 04 Jun 2023 18:58:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 04 Jun 2023 18:58:00 GMT
EXPOSE 27017
# Sun, 04 Jun 2023 18:58:00 GMT
USER 1001
# Sun, 04 Jun 2023 18:58:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9a1b78eb1a7062e225815cd9252c9264239b37a648b7938fb84cf53ac7823b1b`  
		Last Modified: Sun, 04 Jun 2023 17:55:17 GMT  
		Size: 88.9 MB (88872322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be953913a161211ad4c09a9cd9942ea3c5fa7f8af76c0d761a8c97b874e3e6d2`  
		Last Modified: Sun, 04 Jun 2023 18:59:59 GMT  
		Size: 3.8 MB (3788631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd12aa6478ee2a9c7ffe680949a49156a5e64fb31600d516f9ed9a261d264d7`  
		Last Modified: Sun, 04 Jun 2023 19:00:10 GMT  
		Size: 96.9 MB (96917156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e92be9fe7c005b8096f16473fca4db1869d38aa68bd02d5b0fdab676013e51b`  
		Last Modified: Sun, 04 Jun 2023 18:59:58 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1583ca873e74642d7cef32799ee48ceb926b6bb36ef9dbf354b5aba3662d8fda`  
		Last Modified: Sun, 04 Jun 2023 18:59:58 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d525a42329792ae08a21903a52e0983421e6d4c9847ae0b9f259e285dfe9960`  
		Last Modified: Sun, 04 Jun 2023 18:59:56 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a84ff28692e9237a182f3a47a0f0c264c6a85469b9b4c619b87caa2d70835b2`  
		Last Modified: Sun, 04 Jun 2023 18:59:57 GMT  
		Size: 914.5 KB (914548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2c0d1de7afaadcdffdae9ac57b69d86b3537a24d5235085bfa53452c0bb88c`  
		Last Modified: Sun, 04 Jun 2023 18:59:58 GMT  
		Size: 8.1 MB (8137893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4736dba3be323fc12f50255a1c2e2aa6a4c85383a0651394e823485f88fbe806`  
		Last Modified: Sun, 04 Jun 2023 18:59:56 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd78aa6e620ecc1db7a0bdfd463f670a58b8e7f3ba83cb3cdb4e0f361dd22aa`  
		Last Modified: Sun, 04 Jun 2023 18:59:56 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
