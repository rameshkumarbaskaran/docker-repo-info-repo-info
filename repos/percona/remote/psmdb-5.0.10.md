## `percona:psmdb-5.0.10`

```console
$ docker pull percona@sha256:0ac1180c20af3780d4e60afe79c79081164d8c91165e2c53b31823ca9850a9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.10` - linux; amd64

```console
$ docker pull percona@sha256:85c032829baaccd0d7bf36bb59ceeb9c6130404f11dcaaaa7ede32e44e6fa1fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214054760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957d5e887d1f8a91f0b9988bb8a2e5581a7f994cb4fcbff0622e8d5f91aae85c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sun, 04 Jun 2023 17:54:21 GMT
ADD file:7d5910516ba3a0fdff1b226873dd448ed4e09ac326aecf5969218af0c0ef16c4 in / 
# Sun, 04 Jun 2023 17:54:22 GMT
CMD ["/bin/bash"]
# Sun, 04 Jun 2023 18:56:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sun, 04 Jun 2023 18:56:14 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Sun, 04 Jun 2023 18:56:14 GMT
ENV PSMDB_VERSION=5.0.10-9
# Sun, 04 Jun 2023 18:56:14 GMT
ENV OS_VER=el8
# Sun, 04 Jun 2023 18:56:14 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Sun, 04 Jun 2023 18:56:15 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sun, 04 Jun 2023 18:56:57 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sun, 04 Jun 2023 18:56:58 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Sun, 04 Jun 2023 18:56:59 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sun, 04 Jun 2023 18:56:59 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sun, 04 Jun 2023 18:56:59 GMT
ENV GOSU_VERSION=1.11
# Sun, 04 Jun 2023 18:57:02 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sun, 04 Jun 2023 18:57:05 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sun, 04 Jun 2023 18:57:05 GMT
VOLUME [/data/db]
# Sun, 04 Jun 2023 18:57:06 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sun, 04 Jun 2023 18:57:06 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sun, 04 Jun 2023 18:57:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 04 Jun 2023 18:57:06 GMT
EXPOSE 27017
# Sun, 04 Jun 2023 18:57:06 GMT
USER 1001
# Sun, 04 Jun 2023 18:57:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9a1b78eb1a7062e225815cd9252c9264239b37a648b7938fb84cf53ac7823b1b`  
		Last Modified: Sun, 04 Jun 2023 17:55:17 GMT  
		Size: 88.9 MB (88872322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7e202cd4958725cc44665b463eb76c21f9195ba659677eeeecec35522cba5b`  
		Last Modified: Sun, 04 Jun 2023 18:59:35 GMT  
		Size: 3.8 MB (3788670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b812ede180e463f9774ea9005f42ee88c5ab41346d8d01e372215d2aa36ffd61`  
		Last Modified: Sun, 04 Jun 2023 18:59:48 GMT  
		Size: 112.3 MB (112307722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7669b954669d105cc06efa79c6161f70559f1eafd1a5752a172e3449dd793a2a`  
		Last Modified: Sun, 04 Jun 2023 18:59:34 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e8ec7d25a31451146597675b5d77a9236436ce420cf10f342ec054e7bd371e`  
		Last Modified: Sun, 04 Jun 2023 18:59:34 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385ed0e2e457564ec68ece5180a4845a2a55577caef4413960f1b94418bc79ac`  
		Last Modified: Sun, 04 Jun 2023 18:59:32 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f05462036dcf7ba833bffe7587786c7febe527ae767ad2d1e9268e94012f81`  
		Last Modified: Sun, 04 Jun 2023 18:59:32 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb507d826ccf375dad4d586531a97647c860a63344b6840d04b05b4a5d314c69`  
		Last Modified: Sun, 04 Jun 2023 18:59:33 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cac9732f1b164300e21839ada662cbac2b961499e9b51fe7eb78f57e00710a`  
		Last Modified: Sun, 04 Jun 2023 18:59:32 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af13100454cdf419264ab393277acccc2df91508c353b00fc417d058bdbea3e`  
		Last Modified: Sun, 04 Jun 2023 18:59:32 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
