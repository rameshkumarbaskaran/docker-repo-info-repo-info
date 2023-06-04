## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:65651336424d5f7623ca89b61a2702631f1b37fa0293c3c500816ea14a665b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:90113da057b15c9567b7b62c0b6660e6fa0b5c544358cdd74e150fd84e5112f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179338901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51e4c6974817f7007b15d6e363474daf7dc327bcb58634ea79f5547c677501`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sun, 04 Jun 2023 17:54:21 GMT
ADD file:7d5910516ba3a0fdff1b226873dd448ed4e09ac326aecf5969218af0c0ef16c4 in / 
# Sun, 04 Jun 2023 17:54:22 GMT
CMD ["/bin/bash"]
# Sun, 04 Jun 2023 18:56:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sun, 04 Jun 2023 18:58:07 GMT
ENV PSMDB_VERSION=4.2.21-21
# Sun, 04 Jun 2023 18:58:07 GMT
ENV OS_VER=el8
# Sun, 04 Jun 2023 18:58:07 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Sun, 04 Jun 2023 18:58:07 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sun, 04 Jun 2023 18:58:10 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Sun, 04 Jun 2023 18:58:50 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sun, 04 Jun 2023 18:58:51 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Sun, 04 Jun 2023 18:58:51 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sun, 04 Jun 2023 18:58:52 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sun, 04 Jun 2023 18:58:52 GMT
ENV GOSU_VERSION=1.11
# Sun, 04 Jun 2023 18:58:54 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sun, 04 Jun 2023 18:58:56 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sun, 04 Jun 2023 18:58:56 GMT
VOLUME [/data/db]
# Sun, 04 Jun 2023 18:58:56 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sun, 04 Jun 2023 18:58:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 04 Jun 2023 18:58:56 GMT
EXPOSE 27017
# Sun, 04 Jun 2023 18:58:56 GMT
USER 1001
# Sun, 04 Jun 2023 18:58:57 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9a1b78eb1a7062e225815cd9252c9264239b37a648b7938fb84cf53ac7823b1b`  
		Last Modified: Sun, 04 Jun 2023 17:55:17 GMT  
		Size: 88.9 MB (88872322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979fc5f1ca070d0a4653e0029099725c1d7e4c8e03622d67a8765c0efeb1f508`  
		Last Modified: Sun, 04 Jun 2023 19:00:21 GMT  
		Size: 3.8 MB (3788625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29be248314a62c5798402bb220fb3cf6f580fd8a3de5910fb5b4ba5452ae626`  
		Last Modified: Sun, 04 Jun 2023 19:00:30 GMT  
		Size: 77.6 MB (77605113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a81e7c958e8ba3fc05b60d1fd918a03ce40ff261a7eb100a414bee2ef36e7a8`  
		Last Modified: Sun, 04 Jun 2023 19:00:21 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86405a2fb78b0fc7d70fc7e8928e867e743667dc98606b75a025c5b924c634d`  
		Last Modified: Sun, 04 Jun 2023 19:00:19 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee021cd63ae62758033711d0c616d57b1851386100c9c7851410a996e70f8954`  
		Last Modified: Sun, 04 Jun 2023 19:00:19 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20afd8c13c843cbc8be164d01c5d731ca5e28d6c27eb0b03a101ad25f5b6507`  
		Last Modified: Sun, 04 Jun 2023 19:00:19 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965b05da7783031677e345f509ab5d068529f17e8fd2c0e5b706dd01c008d04a`  
		Last Modified: Sun, 04 Jun 2023 19:00:20 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19c3a87ad2743924ff2bef93a9de6335323c31d0c842f2ba6e2f0f0cf5d289c`  
		Last Modified: Sun, 04 Jun 2023 19:00:19 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
