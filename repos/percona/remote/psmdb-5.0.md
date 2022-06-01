## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:a42bdfb0705513f6dd07b27e2ec3b959c1c2ab32d433ea4051fe411e65283609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:8c3442218b149c7f9d295392bb976b6fb02e42949385584774b2bf0c394ad030
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210802311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fe3cd1e8787050bc1a32615085127f1512d8bef2dc4cd874df67f0e685dd6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Jun 2022 17:05:47 GMT
ADD file:48aa8cc19fd94c8679e43b263d7eec6d7f5d19f4288991eb0c68f52c91068a90 in / 
# Wed, 01 Jun 2022 17:05:48 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 18:00:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 01 Jun 2022 18:02:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Wed, 01 Jun 2022 18:02:22 GMT
ENV PSMDB_VERSION=5.0.8-7
# Wed, 01 Jun 2022 18:02:22 GMT
ENV OS_VER=el8
# Wed, 01 Jun 2022 18:02:22 GMT
ENV FULL_PERCONA_VERSION=5.0.8-7.el8
# Wed, 01 Jun 2022 18:02:22 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 01 Jun 2022 18:03:05 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 01 Jun 2022 18:03:06 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 01 Jun 2022 18:03:07 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 01 Jun 2022 18:03:07 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 01 Jun 2022 18:03:07 GMT
ENV GOSU_VERSION=1.11
# Wed, 01 Jun 2022 18:03:11 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 01 Jun 2022 18:03:14 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 01 Jun 2022 18:03:14 GMT
VOLUME [/data/db]
# Wed, 01 Jun 2022 18:03:15 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 01 Jun 2022 18:03:15 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 01 Jun 2022 18:03:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jun 2022 18:03:15 GMT
EXPOSE 27017
# Wed, 01 Jun 2022 18:03:15 GMT
USER 1001
# Wed, 01 Jun 2022 18:03:15 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ec2c52e89d2aa80aa01fc0e5f2ca1dc539d07b8f53e020f0c5af0f3e3c482525`  
		Last Modified: Wed, 01 Jun 2022 17:06:38 GMT  
		Size: 84.6 MB (84568422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d3e95969958bb86107cdfbe3d8213edbda2792c1ecd4b496419544585e2ddf`  
		Last Modified: Wed, 01 Jun 2022 18:07:38 GMT  
		Size: 3.7 MB (3744794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcbb620f28a2ec5dc58d33a24e3c37c1f62a67373f5b03d5f12a587d90f4e2d`  
		Last Modified: Wed, 01 Jun 2022 18:07:51 GMT  
		Size: 113.4 MB (113403040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c60a775fbe6434f159a16552672fb14752d7d7188a16f076dde2257e5576a99`  
		Last Modified: Wed, 01 Jun 2022 18:07:35 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0817f9328e715a15c2e08b19bdcdcbc7503d4f58b4797cd398f8d0bbaef842c7`  
		Last Modified: Wed, 01 Jun 2022 18:07:36 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d466b163bfff194c683e2c91f79d02d1bf07985244ad4d2a5fd4b0c051ac6c0`  
		Last Modified: Wed, 01 Jun 2022 18:07:33 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71067ebae95a39624819731cda3b04420465ab721f9f2936cffb671ad6a330b`  
		Last Modified: Wed, 01 Jun 2022 18:07:33 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05c72ecbb774870dc55b17461beb9cfb15d20bdf079a955890b2cf9e591a534`  
		Last Modified: Wed, 01 Jun 2022 18:07:34 GMT  
		Size: 8.1 MB (8137893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b70f79ef9bc05c2e52f3600a5c1775eea20cd753bd59cee9a0e70d3c9a1a81`  
		Last Modified: Wed, 01 Jun 2022 18:07:33 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98b065e6eab1be346a9c78f008b2f3dcfc361c5c5ecf0c6ed8d7df6baddc7b6`  
		Last Modified: Wed, 01 Jun 2022 18:07:38 GMT  
		Size: 4.6 KB (4560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
