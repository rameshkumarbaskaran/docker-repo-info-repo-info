## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:278a8b476021a3c464aed6adca6a2765b30cf4163e9dbbfa1c14764411c6cbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:1a6cfff71c21f8ba9e525d959ca6cd2638cec1685d82244a0c68b76e185f5104
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198163085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c43d7fb2e22e14d6bcc9469eac88eaa3b7082022525aa144d5435a4ce06083`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Mar 2023 20:22:21 GMT
ADD file:59635cb4a05af7cf47897b040053d3efd0d1398a3b8add59c5c8e0dcadbe35bf in / 
# Wed, 08 Mar 2023 20:22:22 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 20:45:02 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Mar 2023 20:47:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 08 Mar 2023 20:47:58 GMT
ENV PSMDB_VERSION=4.4.15-15
# Wed, 08 Mar 2023 20:47:58 GMT
ENV OS_VER=el8
# Wed, 08 Mar 2023 20:47:58 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Wed, 08 Mar 2023 20:47:58 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Mar 2023 20:48:38 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 08 Mar 2023 20:48:39 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 08 Mar 2023 20:48:39 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 08 Mar 2023 20:48:40 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 08 Mar 2023 20:48:40 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Mar 2023 20:48:43 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 08 Mar 2023 20:48:45 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 08 Mar 2023 20:48:45 GMT
VOLUME [/data/db]
# Wed, 08 Mar 2023 20:48:46 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 08 Mar 2023 20:48:46 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 08 Mar 2023 20:48:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Mar 2023 20:48:46 GMT
EXPOSE 27017
# Wed, 08 Mar 2023 20:48:46 GMT
USER 1001
# Wed, 08 Mar 2023 20:48:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5e01956c53d898e172d8db363562f69df2f624c2cd6eaf3bea39c918d4dcbd89`  
		Last Modified: Wed, 08 Mar 2023 20:23:51 GMT  
		Size: 88.4 MB (88425286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9036a3a4cad7e36430e1e76bac8cedb5ad5c0df388737b4449407364d8659033`  
		Last Modified: Wed, 08 Mar 2023 20:51:52 GMT  
		Size: 3.8 MB (3765849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2896ab73bb1f87cbeada305ce82e8b7ab75a383e7aae33213b11d0f9dfa860d`  
		Last Modified: Wed, 08 Mar 2023 20:52:03 GMT  
		Size: 96.9 MB (96885901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3e090e823175287ad48bc22342b3c8ba03e88579e78dae315cad5db2a73d9f`  
		Last Modified: Wed, 08 Mar 2023 20:51:51 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8208c2a70ea7ba8a5d038a65f5bd96040eb4f73a81610e55cfd0197402051e92`  
		Last Modified: Wed, 08 Mar 2023 20:51:50 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9638e6a358b3cbf3eac1aa565eb863286c7b17a29b8c9b1c238c4ec1a81293b`  
		Last Modified: Wed, 08 Mar 2023 20:51:49 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c48c5dc2977b6437933c9cee95bd393beaf2fc4e40b4dec841b81eaf31e093`  
		Last Modified: Wed, 08 Mar 2023 20:51:49 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431c883ae6bb31c159a5a083e91928904370010c5e09608c61ff28af1ea0edbf`  
		Last Modified: Wed, 08 Mar 2023 20:51:50 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28aaa31bc7c8eda3c6805c807b5d981284ed8b285de809d7785c0d5a9e5b203b`  
		Last Modified: Wed, 08 Mar 2023 20:51:49 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f79753562eb64b7aca6d842e15d8614c1f139b0c9957f730b8b8b602287799`  
		Last Modified: Wed, 08 Mar 2023 20:51:49 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
