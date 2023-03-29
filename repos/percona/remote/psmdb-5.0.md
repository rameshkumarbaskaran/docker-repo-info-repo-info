## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:5fd59911a31a3a93ed47826dba54db05721df7724129e4c8ba4e46cf88d7e24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:bc7cea94acbd3afed80df7128e3135f295adc40f42bf1d511ac36ca9a521fd73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213564635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa40547a452608df7002751f3896c5019226f87e1e9435d2c9b7ee6fbfdeef40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:26 GMT
ADD file:727407c52e11ec0d0d70de3b26944ebac2213dd17723ae375a55557b4b5968fc in / 
# Wed, 29 Mar 2023 00:21:27 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:46:28 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 29 Mar 2023 00:47:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Wed, 29 Mar 2023 00:47:58 GMT
ENV PSMDB_VERSION=5.0.10-9
# Wed, 29 Mar 2023 00:47:58 GMT
ENV OS_VER=el8
# Wed, 29 Mar 2023 00:47:58 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Wed, 29 Mar 2023 00:47:58 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 29 Mar 2023 00:48:39 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 29 Mar 2023 00:48:40 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 29 Mar 2023 00:48:40 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 29 Mar 2023 00:48:40 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 29 Mar 2023 00:48:40 GMT
ENV GOSU_VERSION=1.11
# Wed, 29 Mar 2023 00:48:44 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 29 Mar 2023 00:48:46 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 29 Mar 2023 00:48:47 GMT
VOLUME [/data/db]
# Wed, 29 Mar 2023 00:48:47 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 29 Mar 2023 00:48:47 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 29 Mar 2023 00:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 00:48:47 GMT
EXPOSE 27017
# Wed, 29 Mar 2023 00:48:47 GMT
USER 1001
# Wed, 29 Mar 2023 00:48:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f060192256a938b97a2f291b041c8c46b60220b4a2bf48c91f4339976bb3703b`  
		Last Modified: Wed, 29 Mar 2023 00:22:46 GMT  
		Size: 88.4 MB (88436352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202189d90bc96ae565d32533e854a180c0886f7608b1530743de0f057786fadc`  
		Last Modified: Wed, 29 Mar 2023 00:51:54 GMT  
		Size: 3.8 MB (3760834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41147e0833585fab7184dceae5776c3a71ae58c4bb6e5835bc6b967951af0b8`  
		Last Modified: Wed, 29 Mar 2023 00:52:06 GMT  
		Size: 112.3 MB (112281408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55c96271459fffbf1104131ee15aec7d7086b588af4ee8fd12b016cab490854`  
		Last Modified: Wed, 29 Mar 2023 00:51:53 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61133588d650d61b4e3c5dd30e61d1e409e0a401104376d8bf51a6760629509f`  
		Last Modified: Wed, 29 Mar 2023 00:51:53 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa7ca2168f68eeef252bef579b9fad81e5d90b7551d95b1290af3b48574ee1f`  
		Last Modified: Wed, 29 Mar 2023 00:51:51 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953af200220b3eee9342846a9835bd09f58abba9e4d86d95dc5d6aea83e216e2`  
		Last Modified: Wed, 29 Mar 2023 00:51:51 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0c51fede780f10a886d75284b0f6118d50909949e9e77e707fce2cd38922e`  
		Last Modified: Wed, 29 Mar 2023 00:51:53 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58b8375cd54bb7b057ca7da339980b216fb81771f7a4095b48b0ebbaef758cf`  
		Last Modified: Wed, 29 Mar 2023 00:51:51 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8627fa7c5f42146642bc747d1e24324f3cd16c12c46ab4990619b4bc4f14a1b`  
		Last Modified: Wed, 29 Mar 2023 00:51:51 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
