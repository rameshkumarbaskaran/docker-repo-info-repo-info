## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:14eb8b85b033cbd621592f7d6c32776b5ef0f31f7b8a1ccd2eb6b9b396568e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:6d3963aa2f5da3dc825764b25051d1d50dbd2f6300bb4096eee9a3fc16694d5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195743888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e574daad289ea20c2b3de914659d21c7459c556cef407cdc50feee3c575d208`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 12 Oct 2022 21:20:32 GMT
ADD file:2c7deb13100ea9b7487f0e37a557426c2f4639ed9100b1a0f13b30916ce6bcb4 in / 
# Wed, 12 Oct 2022 21:20:32 GMT
CMD ["/bin/bash"]
# Wed, 12 Oct 2022 21:47:02 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Oct 2022 21:49:32 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 12 Oct 2022 21:49:32 GMT
ENV PSMDB_VERSION=4.4.15-15
# Wed, 12 Oct 2022 21:49:32 GMT
ENV OS_VER=el8
# Wed, 12 Oct 2022 21:49:32 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Wed, 12 Oct 2022 21:49:32 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 12 Oct 2022 21:50:11 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 12 Oct 2022 21:50:12 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 12 Oct 2022 21:50:12 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 12 Oct 2022 21:50:13 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 12 Oct 2022 21:50:13 GMT
ENV GOSU_VERSION=1.11
# Wed, 12 Oct 2022 21:50:16 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 12 Oct 2022 21:50:19 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 12 Oct 2022 21:50:19 GMT
VOLUME [/data/db]
# Wed, 12 Oct 2022 21:50:20 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 12 Oct 2022 21:50:20 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 12 Oct 2022 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 21:50:20 GMT
EXPOSE 27017
# Wed, 12 Oct 2022 21:50:20 GMT
USER 1001
# Wed, 12 Oct 2022 21:50:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d36fda030a05490a75e03359f0fb6861fc9de2e4ae6dd9631ff0c65bde586bc0`  
		Last Modified: Wed, 12 Oct 2022 21:21:52 GMT  
		Size: 86.0 MB (85968038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2df7259560c6f22da1c0f9b3d401138a2a126bcf67e787431217ca52e443d7`  
		Last Modified: Wed, 12 Oct 2022 21:53:29 GMT  
		Size: 3.8 MB (3775606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b8e122c1727b3e6a9c0afcb09ed78e3e36a5380d5af297499e8a36854fad30`  
		Last Modified: Wed, 12 Oct 2022 21:53:40 GMT  
		Size: 96.9 MB (96914191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3beec83c0fb0de8db8cd8421fcd6d8499b82dbb227493aae450d4efc1635b41`  
		Last Modified: Wed, 12 Oct 2022 21:53:27 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c5bd0ed8aa4fae82c60ef96cd0cd4ffd1af50d8ecf69aca280fd49954f591e`  
		Last Modified: Wed, 12 Oct 2022 21:53:27 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27eae25e96613165d08377359919ffc03a5f63336eda754405a45f06eb2248d`  
		Last Modified: Wed, 12 Oct 2022 21:53:25 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62a11a1acb0d0e3c65325cb59a33ee6c1d442eea5b92e854f288e163098ef16`  
		Last Modified: Wed, 12 Oct 2022 21:53:26 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefcc5eea36a0cbf4a0d866bc03872f7a9cb3585f410b78c0670a8d73280ea8d`  
		Last Modified: Wed, 12 Oct 2022 21:53:27 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e498bb66b95682b99567f7a95e68c72229c11162bffea82a309a1c695241f31b`  
		Last Modified: Wed, 12 Oct 2022 21:53:25 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeffcbcbcc154c02ca0f1e04e744ba9d52a1e8993ae25bd884b83459695168ec`  
		Last Modified: Wed, 12 Oct 2022 21:53:25 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
