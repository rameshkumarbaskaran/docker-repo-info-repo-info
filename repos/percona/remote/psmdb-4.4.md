## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:963097e2642b1d2319b6de9cba2845f3b5155d25107ec6762eeebd7d3933bcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:c78cb3a0c4f1627fe0dc4ca98a3b270ee511ec02f859d844f569f09e137b43c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198660719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5f1a0c5965e732b35f343d4c12ec18e7592b8253e62d624a6980faecd7d213`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 24 May 2023 21:20:20 GMT
ADD file:9fa6758e3fa61a51e989e74b7f3adf02abe0e1b0a77e5a2118655b36ec4b9863 in / 
# Wed, 24 May 2023 21:20:20 GMT
CMD ["/bin/bash"]
# Wed, 24 May 2023 21:36:58 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 24 May 2023 21:37:59 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 24 May 2023 21:37:59 GMT
ENV PSMDB_VERSION=4.4.15-15
# Wed, 24 May 2023 21:37:59 GMT
ENV OS_VER=el8
# Wed, 24 May 2023 21:37:59 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Wed, 24 May 2023 21:37:59 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 24 May 2023 21:38:40 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 24 May 2023 21:38:40 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 24 May 2023 21:38:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 24 May 2023 21:38:41 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 24 May 2023 21:38:41 GMT
ENV GOSU_VERSION=1.11
# Wed, 24 May 2023 21:38:44 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 24 May 2023 21:38:46 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 24 May 2023 21:38:46 GMT
VOLUME [/data/db]
# Wed, 24 May 2023 21:38:46 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 24 May 2023 21:38:46 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 24 May 2023 21:38:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 May 2023 21:38:47 GMT
EXPOSE 27017
# Wed, 24 May 2023 21:38:47 GMT
USER 1001
# Wed, 24 May 2023 21:38:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d786df39362960174459800752e5106f3f2ca0fcb3dcb8fd19d47d5be2ec379c`  
		Last Modified: Wed, 24 May 2023 21:21:10 GMT  
		Size: 88.9 MB (88874316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8902ac1b020783bc080701aa8ce8db66397a022265f5984a3f80eb8a5cee01`  
		Last Modified: Wed, 24 May 2023 21:40:44 GMT  
		Size: 3.8 MB (3790021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad3f8a5d8b3e8f100ddc3005239b7c711565e9727cd9a931ed374b4e118f4a3`  
		Last Modified: Wed, 24 May 2023 21:40:54 GMT  
		Size: 96.9 MB (96910332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60d549d519efd427f28e3fd86dee221f3c9f4b2fca401f897c5ea96ff35655f`  
		Last Modified: Wed, 24 May 2023 21:40:43 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345592fd0472af5b2a5b8f0bd5bb33b61309c5f61cebdc5ecf9cd800be62f0e`  
		Last Modified: Wed, 24 May 2023 21:40:43 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da097c5cd240168f000062bb7aa4fd417ba91e4daec8783af11c7268e646881f`  
		Last Modified: Wed, 24 May 2023 21:40:41 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbf5a26948f504f852ab3225e97fe301307ab58260b6ad8a1d23e05e8a0de38`  
		Last Modified: Wed, 24 May 2023 21:40:41 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cb4e2af96629c4a6eb54f03aeee5da8204f1cb6ab43171914a36d4a647686e`  
		Last Modified: Wed, 24 May 2023 21:40:42 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f99debabbdfdc83b334546bcdf383b0c99e38530e4af03abd8593e9c749398`  
		Last Modified: Wed, 24 May 2023 21:40:41 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7209754943294c3b22d9cb9ca5f5f4e69756cf0c14b178a33820097af7c157a`  
		Last Modified: Wed, 24 May 2023 21:40:41 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
