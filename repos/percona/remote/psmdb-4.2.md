## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:90d4aa3a092a6cd546ffb00be518036cf94ef0a2d3e5605fa04e159f1b56e661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:0b5b5412d4c644e8db8afabe56491d98e8f2f32667b6ce04c4a4a221430b4d7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188281960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bce754a40626f23ad72ce27d07323660236466bc2a2c535351c28d335ac1883`
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
# Mon, 26 Jul 2021 18:40:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Mon, 26 Jul 2021 18:40:48 GMT
ENV PSMDB_VERSION=4.2.15-16
# Mon, 26 Jul 2021 18:40:48 GMT
ENV OS_VER=el8
# Mon, 26 Jul 2021 18:40:48 GMT
ENV FULL_PERCONA_VERSION=4.2.15-16.el8
# Mon, 26 Jul 2021 18:40:49 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 26 Jul 2021 18:41:14 GMT
RUN set -ex;     dnf install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         oniguruma         jq         dnf-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     dnf clean all;     dnf -y remove dnf-utils;     rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Mon, 26 Jul 2021 18:41:15 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Mon, 26 Jul 2021 18:41:15 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Mon, 26 Jul 2021 18:41:16 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Mon, 26 Jul 2021 18:41:16 GMT
ENV GOSU_VERSION=1.11
# Mon, 26 Jul 2021 18:41:20 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Mon, 26 Jul 2021 18:41:24 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Mon, 26 Jul 2021 18:41:24 GMT
COPY file:36bd7798a7bd236f79a692385b6877519fd05ff40f92de87cb1d5c527c35d799 in /entrypoint.sh 
# Mon, 26 Jul 2021 18:41:24 GMT
VOLUME [/data/db]
# Mon, 26 Jul 2021 18:41:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Jul 2021 18:41:25 GMT
EXPOSE 27017
# Mon, 26 Jul 2021 18:41:25 GMT
USER 1001
# Mon, 26 Jul 2021 18:41:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab302d7bd891e51f71409538ce92e66075c79099fa1b0e8b0752345acc4710bb`  
		Last Modified: Mon, 26 Jul 2021 18:42:49 GMT  
		Size: 25.2 MB (25194684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aee968df54def2f0804902ed5b26e0e0f0d9acc8c8bf110a5e2017a273bc7b`  
		Last Modified: Mon, 26 Jul 2021 18:42:59 GMT  
		Size: 78.8 MB (78832063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a646fad9a469983bbb01cb0a1f1021be737663f61cb58f1e791956b798483249`  
		Last Modified: Mon, 26 Jul 2021 18:42:44 GMT  
		Size: 1.6 KB (1550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7786d2aba95dca58b62a7e23f16e445383e482f81878bb29d5eda746ba390ed`  
		Last Modified: Mon, 26 Jul 2021 18:42:42 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444e84ec18616343d39faa540f58b0a0f8f618aa5543c9846cbd42df09d0ebf3`  
		Last Modified: Mon, 26 Jul 2021 18:42:42 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6f74158458ee259040b7030398cfba2f1d2f11c86c5a96a976f48d76e637ea`  
		Last Modified: Mon, 26 Jul 2021 18:42:42 GMT  
		Size: 914.5 KB (914548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb8d0b527cf418f186953935ffd11be7f7d0b9d183de553fdf516f89a3b8728`  
		Last Modified: Mon, 26 Jul 2021 18:42:44 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4238bd433acb71e466b0da08fd6e0bc59cb35865e518ee132abc492d424cb031`  
		Last Modified: Mon, 26 Jul 2021 18:42:42 GMT  
		Size: 4.5 KB (4542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
