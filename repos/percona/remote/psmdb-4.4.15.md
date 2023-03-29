## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:d4e08d846c52b0ee130be4f34062460ff3d3756315acdc3ae8b73437e1110787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:54474aadbbfc48378b2d04d3c5def3078ecf23763c23d9fc9fccbaef75b7c50f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198172724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21dc1afab801800fee460ea085f57f1dc7f1b3ff65f5129653a951406ce8db37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:26 GMT
ADD file:727407c52e11ec0d0d70de3b26944ebac2213dd17723ae375a55557b4b5968fc in / 
# Wed, 29 Mar 2023 00:21:27 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:46:28 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 29 Mar 2023 00:48:55 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 29 Mar 2023 00:48:56 GMT
ENV PSMDB_VERSION=4.4.15-15
# Wed, 29 Mar 2023 00:48:56 GMT
ENV OS_VER=el8
# Wed, 29 Mar 2023 00:48:56 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Wed, 29 Mar 2023 00:48:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 29 Mar 2023 00:49:36 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 29 Mar 2023 00:49:36 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 29 Mar 2023 00:49:37 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 29 Mar 2023 00:49:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 29 Mar 2023 00:49:37 GMT
ENV GOSU_VERSION=1.11
# Wed, 29 Mar 2023 00:49:40 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 29 Mar 2023 00:49:42 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 29 Mar 2023 00:49:42 GMT
VOLUME [/data/db]
# Wed, 29 Mar 2023 00:49:42 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 29 Mar 2023 00:49:43 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 29 Mar 2023 00:49:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 00:49:43 GMT
EXPOSE 27017
# Wed, 29 Mar 2023 00:49:43 GMT
USER 1001
# Wed, 29 Mar 2023 00:49:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f060192256a938b97a2f291b041c8c46b60220b4a2bf48c91f4339976bb3703b`  
		Last Modified: Wed, 29 Mar 2023 00:22:46 GMT  
		Size: 88.4 MB (88436352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab6bf536ade3d3cacef02d69d50de3e83853de47f2a2f8943d4ca1a9d0d11ba`  
		Last Modified: Wed, 29 Mar 2023 00:52:17 GMT  
		Size: 3.8 MB (3760844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2beaad4ed3c277a70c12969074c9253f723d4222666e87bc795ac807e1936e1`  
		Last Modified: Wed, 29 Mar 2023 00:52:28 GMT  
		Size: 96.9 MB (96889488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbddab8f18bc75b3963b3c7c606474ec51a74c03fdb96d52a093291b28b88fe8`  
		Last Modified: Wed, 29 Mar 2023 00:52:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7592e7bc497d8e22855c6ded4cf4d866131d6d8313673dbfc72ca7c5b811eb70`  
		Last Modified: Wed, 29 Mar 2023 00:52:16 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d80a5e06c9f24a45a818b10bf93a1424feb82997ec2fe14047fd59370acb48`  
		Last Modified: Wed, 29 Mar 2023 00:52:15 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff918403122db9d31fa3357344ead22bf792b915adac45626573bdc248a697b1`  
		Last Modified: Wed, 29 Mar 2023 00:52:15 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec96027701b88dbfcf9188c334b59eb7836e0157fcae96052a48e9bd01216eb`  
		Last Modified: Wed, 29 Mar 2023 00:52:16 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b660e9c82f271194d2a5f9bec1b38e2cd9c6a91cf83a8fe787500dfc4a5dfa2`  
		Last Modified: Wed, 29 Mar 2023 00:52:15 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddb517dc128e15bff3d32ae980e9febbfbdf1dfe3b75ca7d751ebc6ce769eb9`  
		Last Modified: Wed, 29 Mar 2023 00:52:15 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
