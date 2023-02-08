## `percona:psmdb-5.0.10`

```console
$ docker pull percona@sha256:0d0b14eeb9b9f5da768ca73ddfa3755665efdf8fb2faf38357b27c4504c6f233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.10` - linux; amd64

```console
$ docker pull percona@sha256:987ee0dfc155099be08164ade2c38292dc363475d90e54976cf0fad1246cccee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213545006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddaff7ebaf7ed78724e12016241be0379b4c3ce6ecd16eab2d02612000b8c0f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:18 GMT
ADD file:345fe34a9ba268db9f89b4c0a24f29fee1910b875b520412a6d6ad5d94e1c29c in / 
# Wed, 08 Feb 2023 19:27:19 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:52:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Feb 2023 19:54:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Wed, 08 Feb 2023 19:54:08 GMT
ENV PSMDB_VERSION=5.0.10-9
# Wed, 08 Feb 2023 19:54:08 GMT
ENV OS_VER=el8
# Wed, 08 Feb 2023 19:54:08 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Wed, 08 Feb 2023 19:54:08 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Feb 2023 19:54:48 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 08 Feb 2023 19:54:50 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 08 Feb 2023 19:54:50 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 08 Feb 2023 19:54:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 08 Feb 2023 19:54:51 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Feb 2023 19:54:55 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 08 Feb 2023 19:55:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 08 Feb 2023 19:55:01 GMT
VOLUME [/data/db]
# Wed, 08 Feb 2023 19:55:02 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 08 Feb 2023 19:55:02 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 08 Feb 2023 19:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Feb 2023 19:55:02 GMT
EXPOSE 27017
# Wed, 08 Feb 2023 19:55:02 GMT
USER 1001
# Wed, 08 Feb 2023 19:55:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:96ce6f03051e96688aa6d88b3c4959386deafef4048331e1b8f48bd9062e1571`  
		Last Modified: Wed, 08 Feb 2023 19:28:46 GMT  
		Size: 88.4 MB (88416695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94603dec2dd302469b3cb85aaf33aaa6b149bee5fcf2c2a1a9524c842e51eb9d`  
		Last Modified: Wed, 08 Feb 2023 19:58:41 GMT  
		Size: 3.8 MB (3758730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16da7f5e9e927c53da629b8022e9ddf8eae541090d8f0a6fcacfb680c644d627`  
		Last Modified: Wed, 08 Feb 2023 19:58:54 GMT  
		Size: 112.3 MB (112283542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7260c3a2863294967c5853522a3ab2b0cbbac424651c833b725b5439db621118`  
		Last Modified: Wed, 08 Feb 2023 19:58:40 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aac93a76e054b267f1b1749f33141692acb86fed5bd75686f3787fc01192409`  
		Last Modified: Wed, 08 Feb 2023 19:58:40 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccebbdd8832cd23c3ce2c3d43c59425987e8437c5da62d38dfaa118db533509`  
		Last Modified: Wed, 08 Feb 2023 19:58:39 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5d812cd276615314a3e88ec1ab9e618fb1c3e72a7c18575d2bd31ad7dedb13`  
		Last Modified: Wed, 08 Feb 2023 19:58:39 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469be6e553582ccfa17ddc4d623fe36d0f58aa80034ac08a8b265d9a22421293`  
		Last Modified: Wed, 08 Feb 2023 19:58:40 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d462e75d7ccd791c083c18f090e8aa6bea5bcff97696bda927376621a06906a2`  
		Last Modified: Wed, 08 Feb 2023 19:58:38 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0522ebb2100b5364433b7527114b7a2f84db6b9534ce9ff71a67755d10b0f89`  
		Last Modified: Wed, 08 Feb 2023 19:58:39 GMT  
		Size: 4.6 KB (4560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
