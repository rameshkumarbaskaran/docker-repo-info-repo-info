## `percona:psmdb-4.2.21`

```console
$ docker pull percona@sha256:edf1d3c3d5f552443567ccbfd34e20ae0e4f771c9118f6f916a274abe362a14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.21` - linux; amd64

```console
$ docker pull percona@sha256:13f58b324b0916a2535a470304f21611c28fd018fb790cf263a8900df822e3ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178841965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd3dbcbcea433117ecfe2152e33ef0e4733dd15c2f247a0b1624a27b8208659`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Feb 2023 19:36:57 GMT
ADD file:38641c1822a4aea5527f6e7429caaa41595e7c7e63f993b0b4787b70ca1e56e2 in / 
# Thu, 23 Feb 2023 19:36:58 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:00:32 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 23 Feb 2023 20:04:21 GMT
ENV PSMDB_VERSION=4.2.21-21
# Thu, 23 Feb 2023 20:04:21 GMT
ENV OS_VER=el8
# Thu, 23 Feb 2023 20:04:21 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Thu, 23 Feb 2023 20:04:21 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 23 Feb 2023 20:04:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Thu, 23 Feb 2023 20:05:02 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 23 Feb 2023 20:05:03 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 23 Feb 2023 20:05:03 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 23 Feb 2023 20:05:03 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 23 Feb 2023 20:05:03 GMT
ENV GOSU_VERSION=1.11
# Thu, 23 Feb 2023 20:05:06 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 23 Feb 2023 20:05:08 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 23 Feb 2023 20:05:08 GMT
VOLUME [/data/db]
# Thu, 23 Feb 2023 20:05:08 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Thu, 23 Feb 2023 20:05:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Feb 2023 20:05:09 GMT
EXPOSE 27017
# Thu, 23 Feb 2023 20:05:09 GMT
USER 1001
# Thu, 23 Feb 2023 20:05:09 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3f135a9ee79c5ecc3e253037715137cd16bdf017f4dcf3900b517a7a2e0c1e8`  
		Last Modified: Thu, 23 Feb 2023 19:37:47 GMT  
		Size: 88.4 MB (88421873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3433ae86afb1be8657ef13f3193e9da9c6677806c50b86bae2a88e2d06c8f776`  
		Last Modified: Thu, 23 Feb 2023 20:07:42 GMT  
		Size: 3.8 MB (3765167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f175aa9ed6b4909704314fa51d4d55706b6c87233ce72a1f214607d1af0228`  
		Last Modified: Thu, 23 Feb 2023 20:07:51 GMT  
		Size: 77.6 MB (77582076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35c73429198df8a2156b8b3a6ae8074c71a28c98d84e1051b8ef135c1c428d4`  
		Last Modified: Thu, 23 Feb 2023 20:07:41 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5d2ed0a51a8734f5c5bb7af6fc23b666f224201de7f5dedb1075f583e606e`  
		Last Modified: Thu, 23 Feb 2023 20:07:39 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2c492cdaaadb3985076e7ec6df62ff9776852a4fe4eb5a814f071f063af783`  
		Last Modified: Thu, 23 Feb 2023 20:07:39 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2c2c7fe7b1e9be6ec1afb4e004f7179d0d87645a06bb38148acfb2dc4779d7`  
		Last Modified: Thu, 23 Feb 2023 20:07:40 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33fc31d8b34213fd71b8c02a8af8418a45a826b44970bf3923055c28784063e`  
		Last Modified: Thu, 23 Feb 2023 20:07:41 GMT  
		Size: 8.1 MB (8137896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b78679d88f6179ab04c9df1a9ebe6c36bdf83ac0e9967add506f0d76e14f54`  
		Last Modified: Thu, 23 Feb 2023 20:07:39 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
