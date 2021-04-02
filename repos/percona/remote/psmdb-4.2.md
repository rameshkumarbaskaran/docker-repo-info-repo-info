## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:03d77507487be573be039b4df815855fbd76bdd4b71a477eb7329f7e7f19cab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:8558f47b0c9fb4f4421c12fa45b5fcbc2d7120b797bcc5274235eb69b54956c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181507804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b84c018763c48a7ee90ab6ce77cbb4e44a6b64851bbf14c0a2faec4650ac8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 01:08:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 06 Mar 2021 01:11:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Fri, 02 Apr 2021 18:36:50 GMT
ENV PSMDB_VERSION=4.2.13-14
# Fri, 02 Apr 2021 18:36:50 GMT
ENV OS_VER=el8
# Fri, 02 Apr 2021 18:36:50 GMT
ENV FULL_PERCONA_VERSION=4.2.13-14.el8
# Fri, 02 Apr 2021 18:36:50 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 02 Apr 2021 18:37:13 GMT
RUN set -ex;     dnf install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         oniguruma         jq         dnf-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     dnf clean all;     dnf -y remove dnf-utils;     rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 02 Apr 2021 18:37:14 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 02 Apr 2021 18:37:15 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 02 Apr 2021 18:37:15 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 02 Apr 2021 18:37:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 02 Apr 2021 18:37:20 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 02 Apr 2021 18:37:24 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 02 Apr 2021 18:37:24 GMT
COPY file:36bd7798a7bd236f79a692385b6877519fd05ff40f92de87cb1d5c527c35d799 in /entrypoint.sh 
# Fri, 02 Apr 2021 18:37:24 GMT
VOLUME [/data/db]
# Fri, 02 Apr 2021 18:37:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Apr 2021 18:37:24 GMT
EXPOSE 27017
# Fri, 02 Apr 2021 18:37:25 GMT
USER 1001
# Fri, 02 Apr 2021 18:37:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5955ec99a73fae1b78a68b7968fca70bf2afe08a634ac6d892e26a6baa19c39`  
		Last Modified: Sat, 06 Mar 2021 01:17:34 GMT  
		Size: 19.4 MB (19434105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5591aab873345993c519738ce11c0a5e0c5f19d7bbafda93e94333d2bdb16146`  
		Last Modified: Fri, 02 Apr 2021 18:38:31 GMT  
		Size: 77.8 MB (77818485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9323e154cd559d2a2de0e56fe4dc2b8cdfdf72617114f61bc97f678f3a1cc4`  
		Last Modified: Fri, 02 Apr 2021 18:38:20 GMT  
		Size: 1.5 KB (1548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5860ad807289da7e0fdc9c68af797f6fcf5610bf78c40797f4e572f5fe77fbc8`  
		Last Modified: Fri, 02 Apr 2021 18:38:17 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0257c07484a96193de17bff93f16b8db8e1b7ceaaff01674beaf6ccb28265d44`  
		Last Modified: Fri, 02 Apr 2021 18:38:18 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a04068b5e62dcd2b5540acc5f047c3e9124a68a8accd41bdcc062a7821419a`  
		Last Modified: Fri, 02 Apr 2021 18:38:18 GMT  
		Size: 914.6 KB (914553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905cbd8372f5d0eb47231ace2f207f0e5e5f61e28bc4e260afc95986c27e152`  
		Last Modified: Fri, 02 Apr 2021 18:38:19 GMT  
		Size: 8.1 MB (8137892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da50750c3f71bcd1ef1b837def4b254be69d62f5f1d1f8eba48c8be9e54ebb86`  
		Last Modified: Fri, 02 Apr 2021 18:38:17 GMT  
		Size: 4.5 KB (4542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
