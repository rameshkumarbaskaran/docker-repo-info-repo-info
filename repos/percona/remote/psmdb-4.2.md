## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:36dfa9efc13fec3e1e901b4e3aef16308322b8f3c9d98c7f77a3b91c60664e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:508c2cb5cb77277246c82b373cf9d265f24141043c998ffc36c6bf7de7c21542
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178844382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4d147dd9d13d52e6e4a5e0eb08e3ad1382d8e02c8c3fcfb17468aa8584b7e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Mar 2023 20:22:21 GMT
ADD file:59635cb4a05af7cf47897b040053d3efd0d1398a3b8add59c5c8e0dcadbe35bf in / 
# Wed, 08 Mar 2023 20:22:22 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 20:45:02 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Mar 2023 20:48:53 GMT
ENV PSMDB_VERSION=4.2.21-21
# Wed, 08 Mar 2023 20:48:53 GMT
ENV OS_VER=el8
# Wed, 08 Mar 2023 20:48:54 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Wed, 08 Mar 2023 20:48:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Mar 2023 20:48:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Wed, 08 Mar 2023 20:49:34 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 08 Mar 2023 20:49:35 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 08 Mar 2023 20:49:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 08 Mar 2023 20:49:36 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 08 Mar 2023 20:49:36 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Mar 2023 20:49:39 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 08 Mar 2023 20:49:41 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 08 Mar 2023 20:49:41 GMT
VOLUME [/data/db]
# Wed, 08 Mar 2023 20:49:41 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 08 Mar 2023 20:49:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Mar 2023 20:49:42 GMT
EXPOSE 27017
# Wed, 08 Mar 2023 20:49:42 GMT
USER 1001
# Wed, 08 Mar 2023 20:49:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5e01956c53d898e172d8db363562f69df2f624c2cd6eaf3bea39c918d4dcbd89`  
		Last Modified: Wed, 08 Mar 2023 20:23:51 GMT  
		Size: 88.4 MB (88425286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17f43e22f1ef6c3ac273b9c5c6ba0373e6cd19dfc5dc91fcb8a175f0be6d3a7`  
		Last Modified: Wed, 08 Mar 2023 20:52:15 GMT  
		Size: 3.8 MB (3765853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67b4fc960d1a22f3980506274b35c503d3354f1e8ca9ba8cbf104673c320f3e`  
		Last Modified: Wed, 08 Mar 2023 20:52:23 GMT  
		Size: 77.6 MB (77580396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fa06a66aaff52653d630c73869b2c390647fde8806b3a99762f0cafa1c0c48`  
		Last Modified: Wed, 08 Mar 2023 20:52:14 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beac43ee568c7ee001407a04f87373e8ce5ece0b67491897c690abf5d5e7f329`  
		Last Modified: Wed, 08 Mar 2023 20:52:12 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5ca0e5a4eb1b6e35c267765a5bee135009aa0b8bacb6d0600cb780f05e2789`  
		Last Modified: Wed, 08 Mar 2023 20:52:12 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67b6b0b896a4e23c15f4373b878c06908fd73d820797e3e8a4a62f9588f3bcb`  
		Last Modified: Wed, 08 Mar 2023 20:52:12 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173232ec9f38bd08478df6c6e8e170dc2a7d17228b897621fc02fa6766c55eed`  
		Last Modified: Wed, 08 Mar 2023 20:52:13 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472997ddc216f0e7314a93aef00236912dc4930b1bbb04809c0c0834d35f92ea`  
		Last Modified: Wed, 08 Mar 2023 20:52:12 GMT  
		Size: 4.6 KB (4556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
