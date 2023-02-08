## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:34265f75880b5381fba0eab263729955f20ed4e1dc3601c2a691421d0414223c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:fd0749d786b1c457979b1fd07bd3d78e7d673add8fbc04645e04705e4102b4ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178819376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd79e31db19ed2fd6a17ef546abe20601244353343bb4df7061a8b826eda98e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:18 GMT
ADD file:345fe34a9ba268db9f89b4c0a24f29fee1910b875b520412a6d6ad5d94e1c29c in / 
# Wed, 08 Feb 2023 19:27:19 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:52:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Feb 2023 19:56:13 GMT
ENV PSMDB_VERSION=4.2.21-21
# Wed, 08 Feb 2023 19:56:13 GMT
ENV OS_VER=el8
# Wed, 08 Feb 2023 19:56:13 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Wed, 08 Feb 2023 19:56:13 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Feb 2023 19:56:16 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Wed, 08 Feb 2023 19:56:52 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 08 Feb 2023 19:56:53 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 08 Feb 2023 19:56:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 08 Feb 2023 19:56:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 08 Feb 2023 19:56:54 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Feb 2023 19:56:57 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 08 Feb 2023 19:56:58 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 08 Feb 2023 19:56:58 GMT
VOLUME [/data/db]
# Wed, 08 Feb 2023 19:56:58 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 08 Feb 2023 19:56:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Feb 2023 19:56:59 GMT
EXPOSE 27017
# Wed, 08 Feb 2023 19:56:59 GMT
USER 1001
# Wed, 08 Feb 2023 19:56:59 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:96ce6f03051e96688aa6d88b3c4959386deafef4048331e1b8f48bd9062e1571`  
		Last Modified: Wed, 08 Feb 2023 19:28:46 GMT  
		Size: 88.4 MB (88416695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bba9cc17ac56ca4c7e31cf1fc06c7b04871b1c4b7552be8db44b21e1a192a9`  
		Last Modified: Wed, 08 Feb 2023 19:59:30 GMT  
		Size: 3.8 MB (3758710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d607524095f6e687bc3a27eeb2f0d562d7ed26ad1ce72db71bfa4db4ed98c7`  
		Last Modified: Wed, 08 Feb 2023 19:59:39 GMT  
		Size: 77.6 MB (77571130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dd677c5830033a0eeb58dc1256adb01ccd2327535f66beb97264e1e7cb99ba`  
		Last Modified: Wed, 08 Feb 2023 19:59:29 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09f468422a89ccc5c0b3a65dae56ad6edd9423ed7da764b4a9c0115abd91430`  
		Last Modified: Wed, 08 Feb 2023 19:59:28 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cbf0395630f4aeacb1a8c38e67c1a3b3eebb68deaabd541782431f397b7e8b`  
		Last Modified: Wed, 08 Feb 2023 19:59:28 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039b319793e4e79292cd3e1cd9495232345a4ca08b87a8ff1715249705f4de74`  
		Last Modified: Wed, 08 Feb 2023 19:59:28 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd608d53355381822db7c796dc0dd2120715064a57aea3f815a9478a4059c22c`  
		Last Modified: Wed, 08 Feb 2023 19:59:29 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b0005ffb05aece5965ab34f8550a272e0e8860ebcbe06245d99e7e1ad463a6`  
		Last Modified: Wed, 08 Feb 2023 19:59:28 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
