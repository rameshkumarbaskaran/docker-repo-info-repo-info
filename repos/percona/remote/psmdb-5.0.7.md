## `percona:psmdb-5.0.7`

```console
$ docker pull percona@sha256:c1a627366f95fdaa8de344045e01e866fa0734763f32c4b85c605a60ee059a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.7` - linux; amd64

```console
$ docker pull percona@sha256:0314c4c5b370a210472088f60164b08304b7f085ddb4c4735af108c05e7b369f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213595042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d785dd7efdaaaff27efac06fcc016744412d0e02b15d6933a2b659a9017b1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:33 GMT
ADD file:d94132182c035117e6c34ac6179798583b0adcdb2790160d2740b5a23dfef57b in / 
# Tue, 29 Mar 2022 18:35:34 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:14:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 21 Apr 2022 11:45:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Thu, 21 Apr 2022 11:45:04 GMT
ENV PSMDB_VERSION=5.0.7-6
# Thu, 21 Apr 2022 11:45:04 GMT
ENV OS_VER=el8
# Thu, 21 Apr 2022 11:45:04 GMT
ENV FULL_PERCONA_VERSION=5.0.7-6.el8
# Thu, 21 Apr 2022 11:45:04 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 21 Apr 2022 11:45:45 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 21 Apr 2022 11:45:45 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 21 Apr 2022 11:45:46 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 21 Apr 2022 11:45:46 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 21 Apr 2022 11:45:46 GMT
ENV GOSU_VERSION=1.11
# Thu, 21 Apr 2022 11:45:50 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 21 Apr 2022 11:45:53 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 21 Apr 2022 11:45:53 GMT
VOLUME [/data/db]
# Thu, 21 Apr 2022 11:45:54 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 21 Apr 2022 11:45:54 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Thu, 21 Apr 2022 11:45:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Apr 2022 11:45:54 GMT
EXPOSE 27017
# Thu, 21 Apr 2022 11:45:54 GMT
USER 1001
# Thu, 21 Apr 2022 11:45:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f194d33a6f3eb80ec1d36f30e468274de9bc57c56876707532a364fe1edb59b7`  
		Last Modified: Tue, 29 Mar 2022 18:36:37 GMT  
		Size: 87.5 MB (87480759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33d36c86ab7968ed2db0e3d9ed70be1c4dde05a9c1f7b85d711db681012178c`  
		Last Modified: Thu, 21 Apr 2022 11:46:49 GMT  
		Size: 3.8 MB (3754363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03099c60488f155e453252ff0e119335740caf196c5f15ecbd823cb4f04b0a5`  
		Last Modified: Thu, 21 Apr 2022 11:47:02 GMT  
		Size: 113.3 MB (113273864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60e3571c89b2888d5b9ac25b79c5ad4cba5af8ed6447c02956cc5840ee9c853`  
		Last Modified: Thu, 21 Apr 2022 11:46:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8d6122aae7b3dc08de88d337de1b34149155cedf138722e792df4d165c4455`  
		Last Modified: Thu, 21 Apr 2022 11:46:48 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73005a15da5396190f8b2e1b41ed24082876c9114ce4ffa9a852311d97e2a2db`  
		Last Modified: Thu, 21 Apr 2022 11:46:46 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5e371cb2e485065805133014622453c90225ce30e8d5ce259bd02b3662f44b`  
		Last Modified: Thu, 21 Apr 2022 11:46:46 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0277d649e2c063867b73a5ab62f1b83dbdb9dd857daa18a93febf6da121e4c`  
		Last Modified: Thu, 21 Apr 2022 11:46:47 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4f402623875bf395577f7dfa8159cd4ea60f18a25361d3dc410f612597c96e`  
		Last Modified: Thu, 21 Apr 2022 11:46:46 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07111b20db1aa8fbf9b72ef7324e88416fa9ba82be0634b1ac62512e001036`  
		Last Modified: Thu, 21 Apr 2022 11:46:46 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
