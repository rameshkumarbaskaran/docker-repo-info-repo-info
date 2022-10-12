## `percona:psmdb-5.0.10`

```console
$ docker pull percona@sha256:da4923d92294d94250bbdb66a57c6489ad0165c152c330dc418bdba848c06a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.10` - linux; amd64

```console
$ docker pull percona@sha256:9126c09308bd12c23279a15e458553f0bf9ae111bdf21253ab044343853b6a58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211135382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f49582568f033a5d0070e38a3b01ba6ea219fa8a926d28880222629562de0b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 12 Oct 2022 21:20:32 GMT
ADD file:2c7deb13100ea9b7487f0e37a557426c2f4639ed9100b1a0f13b30916ce6bcb4 in / 
# Wed, 12 Oct 2022 21:20:32 GMT
CMD ["/bin/bash"]
# Wed, 12 Oct 2022 21:47:02 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Oct 2022 21:48:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Wed, 12 Oct 2022 21:48:34 GMT
ENV PSMDB_VERSION=5.0.10-9
# Wed, 12 Oct 2022 21:48:34 GMT
ENV OS_VER=el8
# Wed, 12 Oct 2022 21:48:34 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Wed, 12 Oct 2022 21:48:34 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 12 Oct 2022 21:49:13 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 12 Oct 2022 21:49:14 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 12 Oct 2022 21:49:14 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 12 Oct 2022 21:49:14 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 12 Oct 2022 21:49:15 GMT
ENV GOSU_VERSION=1.11
# Wed, 12 Oct 2022 21:49:19 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 12 Oct 2022 21:49:22 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 12 Oct 2022 21:49:22 GMT
VOLUME [/data/db]
# Wed, 12 Oct 2022 21:49:23 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 12 Oct 2022 21:49:23 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 12 Oct 2022 21:49:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 21:49:23 GMT
EXPOSE 27017
# Wed, 12 Oct 2022 21:49:23 GMT
USER 1001
# Wed, 12 Oct 2022 21:49:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d36fda030a05490a75e03359f0fb6861fc9de2e4ae6dd9631ff0c65bde586bc0`  
		Last Modified: Wed, 12 Oct 2022 21:21:52 GMT  
		Size: 86.0 MB (85968038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e11c24269e59c838412a6cfa8d4ba4d2cb6a2cee080fca1b30b85052e01ab82`  
		Last Modified: Wed, 12 Oct 2022 21:53:01 GMT  
		Size: 3.8 MB (3775600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f722c19611e216e0628636a0eba6e678f47f50997f5dfd1ae38cd68b5be48f7`  
		Last Modified: Wed, 12 Oct 2022 21:53:14 GMT  
		Size: 112.3 MB (112305692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47563a4108fed08402e77212506b6327919a72683a8856fc5ad6d090a7cbb6ea`  
		Last Modified: Wed, 12 Oct 2022 21:53:00 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e3fe29cd62faace9ad3adc1435f45119d8af7c7204a3a4edc7cee082f7bca`  
		Last Modified: Wed, 12 Oct 2022 21:52:59 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638291bb5acfa4caa98e76219cfb424ae785ffc23914e545143fec9e4ce68f82`  
		Last Modified: Wed, 12 Oct 2022 21:52:58 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473723bbd9f4d086a47e971c7fd5e0e890f014fa4df967ae88719ed3b8a50a95`  
		Last Modified: Wed, 12 Oct 2022 21:52:58 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff718c3cbcea31f6dfb649da96c66fb2a687c4d57b89f7238511b327421b74d`  
		Last Modified: Wed, 12 Oct 2022 21:52:59 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3e4728e28de9309a29a27934d9acedd843a86d1635df25d6ae41c0aa4fa67d`  
		Last Modified: Wed, 12 Oct 2022 21:52:58 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db4168ee76a45a8773ad54219d71ae50928cd6152702978236036c1a886c58a`  
		Last Modified: Wed, 12 Oct 2022 21:52:57 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
