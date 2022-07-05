## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:cd913e78333700b16d3f429d5637be57caf014d7c750ebd1db694393ef4f154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:06f89f7614bd3cf6fc2c0c68670f27dee235230ab1de41ffe805bdc2e6c8727b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176205662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f40c95739cf3cae6258518f6d4a970622af0cf8329f7d3494d4a3f9263191a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:24 GMT
ADD file:05afe15e1c394de999f38bb2413c80af18f129511261f53511fe21e4606b6353 in / 
# Tue, 05 Jul 2022 22:20:24 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:42:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 05 Jul 2022 22:45:17 GMT
ENV PSMDB_VERSION=4.2.21-21
# Tue, 05 Jul 2022 22:45:17 GMT
ENV OS_VER=el8
# Tue, 05 Jul 2022 22:45:17 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Tue, 05 Jul 2022 22:45:17 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 05 Jul 2022 22:45:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Tue, 05 Jul 2022 22:45:54 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 05 Jul 2022 22:45:55 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 05 Jul 2022 22:45:55 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 05 Jul 2022 22:45:55 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 05 Jul 2022 22:45:55 GMT
ENV GOSU_VERSION=1.11
# Tue, 05 Jul 2022 22:45:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 05 Jul 2022 22:46:00 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 05 Jul 2022 22:46:00 GMT
VOLUME [/data/db]
# Tue, 05 Jul 2022 22:46:00 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Tue, 05 Jul 2022 22:46:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Jul 2022 22:46:00 GMT
EXPOSE 27017
# Tue, 05 Jul 2022 22:46:00 GMT
USER 1001
# Tue, 05 Jul 2022 22:46:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:15a6facc77411902de6b8de2d42125695286cd602d17db01f09239a7f6f8992a`  
		Last Modified: Tue, 05 Jul 2022 22:21:25 GMT  
		Size: 84.6 MB (84566504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33574b4a4a9c9c090d35cd59b820850637846f6ab488ac81821a7e2caea64d05`  
		Last Modified: Tue, 05 Jul 2022 22:48:39 GMT  
		Size: 3.7 MB (3734471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb497f65669ff0c20013440904bd3c9243727019e68c839b9fe3cb15f1a43d3`  
		Last Modified: Tue, 05 Jul 2022 22:48:48 GMT  
		Size: 78.8 MB (78831845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334ceb5e1a1c8a6dd44bb6be49f8dd515ce7d8ae50164d78b14461aa65458012`  
		Last Modified: Tue, 05 Jul 2022 22:48:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a559e7e5221dff70e23366365a827dbde512a4c97b2c33b034e5c3bac731f5e`  
		Last Modified: Tue, 05 Jul 2022 22:48:36 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1eff91a51b030cdb5087f22df9bbb1f3dbcfc87384310b35f3fce55fd4c1c8f`  
		Last Modified: Tue, 05 Jul 2022 22:48:36 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11a7f5c0df7ce18aa5a12c9ce089c0d89ac66f8e2efb9e20a0ca3dad75c7279`  
		Last Modified: Tue, 05 Jul 2022 22:48:36 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93acb233823a3d4bb16ca2942d86554b64c42c11daf7ae4bc84dcc48c932fb6`  
		Last Modified: Tue, 05 Jul 2022 22:48:38 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc955866ab5a36ffb9728269166bda4e19fe505a517e88d8c8ef8338f97779f1`  
		Last Modified: Tue, 05 Jul 2022 22:48:36 GMT  
		Size: 4.6 KB (4555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
