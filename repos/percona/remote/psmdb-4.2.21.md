## `percona:psmdb-4.2.21`

```console
$ docker pull percona@sha256:5d3c4f8e9b75e634ff213ace1d3af87e3ff306245b280cab878f2f414d3d9aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.21` - linux; amd64

```console
$ docker pull percona@sha256:8f73b58b7e887e5221856f3a15936bc9c1d84776f643b481af6d363eb16f0a0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178843711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53159930254895cbff45da43898e7996f18cf23490f94937c20384e3155431a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:26 GMT
ADD file:727407c52e11ec0d0d70de3b26944ebac2213dd17723ae375a55557b4b5968fc in / 
# Wed, 29 Mar 2023 00:21:27 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:46:28 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 29 Mar 2023 00:49:51 GMT
ENV PSMDB_VERSION=4.2.21-21
# Wed, 29 Mar 2023 00:49:51 GMT
ENV OS_VER=el8
# Wed, 29 Mar 2023 00:49:51 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Wed, 29 Mar 2023 00:49:51 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 29 Mar 2023 00:49:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Wed, 29 Mar 2023 00:50:31 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 29 Mar 2023 00:50:31 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 29 Mar 2023 00:50:31 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 29 Mar 2023 00:50:32 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 29 Mar 2023 00:50:32 GMT
ENV GOSU_VERSION=1.11
# Wed, 29 Mar 2023 00:50:35 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 29 Mar 2023 00:50:36 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 29 Mar 2023 00:50:36 GMT
VOLUME [/data/db]
# Wed, 29 Mar 2023 00:50:36 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 29 Mar 2023 00:50:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 00:50:37 GMT
EXPOSE 27017
# Wed, 29 Mar 2023 00:50:37 GMT
USER 1001
# Wed, 29 Mar 2023 00:50:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f060192256a938b97a2f291b041c8c46b60220b4a2bf48c91f4339976bb3703b`  
		Last Modified: Wed, 29 Mar 2023 00:22:46 GMT  
		Size: 88.4 MB (88436352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8f9183c508112a37554d94358790067ea6d4a1101bcf7c6e265ce25f4705f2`  
		Last Modified: Wed, 29 Mar 2023 00:52:39 GMT  
		Size: 3.8 MB (3760820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645d6f12caf43803919c79fcde7d306fe0b55b1b774e870397716584cd2f8ad7`  
		Last Modified: Wed, 29 Mar 2023 00:52:47 GMT  
		Size: 77.6 MB (77573708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc60b17df9c422cf7a7f53298ea9d7dde3b33efdb6d5135dd74f103a09d11ad`  
		Last Modified: Wed, 29 Mar 2023 00:52:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdd81c197c8047ccbb8a5bcb794a8d822bd29e2e8ff8d692c44753f12848cd3`  
		Last Modified: Wed, 29 Mar 2023 00:52:37 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324d5238d0de65d3c8d900428007fc55420dd2e51a73d9faa032f50a47a762e3`  
		Last Modified: Wed, 29 Mar 2023 00:52:37 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dd4155cbbf7ac2d500bb9090e0d00af6ed2b1f4916b24b7843ae14ad73e32`  
		Last Modified: Wed, 29 Mar 2023 00:52:37 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf742dd81e67d3ac4b14c21a3b35b9a736a7e0ffdd8bce1f46213ed7b727ae44`  
		Last Modified: Wed, 29 Mar 2023 00:52:38 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f9f779781defc8118f5897201df7005efb9c64f1dd4f956f8173a4cd95d97`  
		Last Modified: Wed, 29 Mar 2023 00:52:37 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
