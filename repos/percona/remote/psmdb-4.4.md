## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:ddb1e8795cdbe8a14c87e55fd827967922c7b461159d0a8e9499abc24251ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:f56d3c08f9875dc190a62af51e25c5480d687cbedfde6cde2dffdb8d5d937338
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195490733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e65a6ddaf7ca7db2ff36dd753fe046386af91259af61a618d9ddc745561e0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Jun 2022 17:05:47 GMT
ADD file:48aa8cc19fd94c8679e43b263d7eec6d7f5d19f4288991eb0c68f52c91068a90 in / 
# Wed, 01 Jun 2022 17:05:48 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 18:00:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 01 Jun 2022 18:03:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 01 Jun 2022 18:03:22 GMT
ENV PSMDB_VERSION=4.4.14-14
# Wed, 01 Jun 2022 18:03:22 GMT
ENV OS_VER=el8
# Wed, 01 Jun 2022 18:03:22 GMT
ENV FULL_PERCONA_VERSION=4.4.14-14.el8
# Wed, 01 Jun 2022 18:03:22 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 01 Jun 2022 18:04:04 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 01 Jun 2022 18:04:05 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 01 Jun 2022 18:04:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 01 Jun 2022 18:04:05 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 01 Jun 2022 18:04:05 GMT
ENV GOSU_VERSION=1.11
# Wed, 01 Jun 2022 18:04:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 01 Jun 2022 18:04:12 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 01 Jun 2022 18:04:12 GMT
VOLUME [/data/db]
# Wed, 01 Jun 2022 18:04:13 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 01 Jun 2022 18:04:13 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 01 Jun 2022 18:04:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jun 2022 18:04:13 GMT
EXPOSE 27017
# Wed, 01 Jun 2022 18:04:13 GMT
USER 1001
# Wed, 01 Jun 2022 18:04:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ec2c52e89d2aa80aa01fc0e5f2ca1dc539d07b8f53e020f0c5af0f3e3c482525`  
		Last Modified: Wed, 01 Jun 2022 17:06:38 GMT  
		Size: 84.6 MB (84568422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30ed689396a1f47fc6a31699d549ce08609b8386ba2ba54907ed6913c26bb30`  
		Last Modified: Wed, 01 Jun 2022 18:08:05 GMT  
		Size: 3.7 MB (3744801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6fdfce4f623101633ca0491738f9841b7d6571bf79a0fdc5add650b47b10db`  
		Last Modified: Wed, 01 Jun 2022 18:08:17 GMT  
		Size: 98.1 MB (98091452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64047ed7e89baa8e8e0648851dcf53bd7449a3dcdca55e8053376440d626017e`  
		Last Modified: Wed, 01 Jun 2022 18:08:04 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a3154e24697eb0e0aef76117642416571ce9a982f77c54c4830d025749e07`  
		Last Modified: Wed, 01 Jun 2022 18:08:04 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ee431f98537cc5600ccc46258c70ea15a668f0b45331e8da4f633ccf570f8`  
		Last Modified: Wed, 01 Jun 2022 18:08:01 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6591968f590d126a4618cdca274f9839c2c5d85068f5abb491fb189e31513b`  
		Last Modified: Wed, 01 Jun 2022 18:08:02 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e94d1345456d91262a9fe7ea9251b7e33677683f655745abf882e87532e073f`  
		Last Modified: Wed, 01 Jun 2022 18:08:04 GMT  
		Size: 8.1 MB (8137896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da9760a81cfeb1a55e130280ed189b6e08a6a5782e227f026ed682577ae811`  
		Last Modified: Wed, 01 Jun 2022 18:08:01 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c56ec9a190affe81f652d2dac0f9040d78ea8b4dc6082ba48a699aaa8b0e19`  
		Last Modified: Wed, 01 Jun 2022 18:08:01 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
