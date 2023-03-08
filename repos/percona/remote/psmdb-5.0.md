## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:cb0c3af7479a63040fca56896728fdb8b21da5ed4a9486e6b4e7903f99a03374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:1bd1b55299fbf7603618cf9687b15b325d33bb2e5e1690328c19c60bf292c80f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213563676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55f60d859f490ebabe0c8f371a71fbe6978f341b901e5e69b07c455f19fb60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Mar 2023 20:22:21 GMT
ADD file:59635cb4a05af7cf47897b040053d3efd0d1398a3b8add59c5c8e0dcadbe35bf in / 
# Wed, 08 Mar 2023 20:22:22 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 20:45:02 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Mar 2023 20:46:48 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Wed, 08 Mar 2023 20:46:48 GMT
ENV PSMDB_VERSION=5.0.10-9
# Wed, 08 Mar 2023 20:46:48 GMT
ENV OS_VER=el8
# Wed, 08 Mar 2023 20:46:48 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Wed, 08 Mar 2023 20:46:48 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Mar 2023 20:47:36 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 08 Mar 2023 20:47:37 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 08 Mar 2023 20:47:38 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 08 Mar 2023 20:47:38 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 08 Mar 2023 20:47:38 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Mar 2023 20:47:41 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 08 Mar 2023 20:47:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 08 Mar 2023 20:47:44 GMT
VOLUME [/data/db]
# Wed, 08 Mar 2023 20:47:45 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 08 Mar 2023 20:47:45 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 08 Mar 2023 20:47:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Mar 2023 20:47:45 GMT
EXPOSE 27017
# Wed, 08 Mar 2023 20:47:45 GMT
USER 1001
# Wed, 08 Mar 2023 20:47:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5e01956c53d898e172d8db363562f69df2f624c2cd6eaf3bea39c918d4dcbd89`  
		Last Modified: Wed, 08 Mar 2023 20:23:51 GMT  
		Size: 88.4 MB (88425286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28021a8c67e8f4ef72da241c6033ceb0fed1f90013d8665becf1daa24b0a6781`  
		Last Modified: Wed, 08 Mar 2023 20:51:27 GMT  
		Size: 3.8 MB (3765847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4d15625d1ed25282648361eceffe3d0a232f995ec140ee59980374e0199a57`  
		Last Modified: Wed, 08 Mar 2023 20:51:39 GMT  
		Size: 112.3 MB (112286486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fee4f00e9a6772516fad193eee8ff708359211a66201ff02bf72a9c619c2e26`  
		Last Modified: Wed, 08 Mar 2023 20:51:26 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4208956ac8c285823dde20c8c64b65d5f90e53e4dc3543da84bac6762594bf`  
		Last Modified: Wed, 08 Mar 2023 20:51:26 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532a2957e07e21d35a1b908ff307dbef2ab494799aa0e180601d14cfd1960d4f`  
		Last Modified: Wed, 08 Mar 2023 20:51:24 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1dd5ddcb9887d3449496b7277301d317395a686c3bb880ff20e81ad905fa39`  
		Last Modified: Wed, 08 Mar 2023 20:51:24 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d9d73f63ba0bb1cbafe92f681b62748d75decf38deb626b200563eb51da2e9`  
		Last Modified: Wed, 08 Mar 2023 20:51:25 GMT  
		Size: 8.1 MB (8137902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04fa742fba0092a589d9af2de942bcd33b6e80366dbcc14d452483981015849`  
		Last Modified: Wed, 08 Mar 2023 20:51:24 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f6f6319f0474b8b068b6a0ffdce75375fc0f7f65342ae9af8d8b318a758b2d`  
		Last Modified: Wed, 08 Mar 2023 20:51:24 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
