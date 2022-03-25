## `percona:psmdb-4.4.13`

```console
$ docker pull percona@sha256:ee40d17b867471c650431e7450e66671e8eacdec42d39d73765a1587fb219092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.13` - linux; amd64

```console
$ docker pull percona@sha256:4e9375aa9350eca0b54a5842eb9b5724e1c8335af464901984c6ac82383ea1ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.4 MB (198377353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f5dcc334cefa84c40fd991ed8ffa4a4dde81aaa63cafbc4e5b466d90f4f078`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 24 Mar 2022 22:26:07 GMT
ADD file:8de122754f28308c5a43ec6c9d2e21a84f88ce3d857c57ceebdbb006ec4218ea in / 
# Thu, 24 Mar 2022 22:26:08 GMT
CMD ["/bin/bash"]
# Thu, 24 Mar 2022 22:28:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 24 Mar 2022 22:29:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Thu, 24 Mar 2022 22:29:37 GMT
ENV PSMDB_VERSION=4.4.13-13
# Thu, 24 Mar 2022 22:29:37 GMT
ENV OS_VER=el8
# Thu, 24 Mar 2022 22:29:37 GMT
ENV FULL_PERCONA_VERSION=4.4.13-13.el8
# Thu, 24 Mar 2022 22:29:37 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 24 Mar 2022 22:30:29 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 24 Mar 2022 22:30:29 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 24 Mar 2022 22:30:30 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 24 Mar 2022 22:30:30 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 24 Mar 2022 22:30:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 24 Mar 2022 22:30:33 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 24 Mar 2022 22:30:36 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 24 Mar 2022 22:30:37 GMT
VOLUME [/data/db]
# Thu, 24 Mar 2022 22:30:37 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 24 Mar 2022 22:30:37 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Thu, 24 Mar 2022 22:30:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 22:30:37 GMT
EXPOSE 27017
# Thu, 24 Mar 2022 22:30:38 GMT
USER 1001
# Thu, 24 Mar 2022 22:30:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:00e01bb8b231e8861500c644bc1bd18c32cf5bb204a4e618d2bae1dcfee66836`  
		Last Modified: Thu, 24 Mar 2022 22:27:07 GMT  
		Size: 87.5 MB (87478984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01286792c772da9e6eac01033dbfa6099f0d1105c4f52e53731476c38967cf4e`  
		Last Modified: Thu, 24 Mar 2022 22:32:27 GMT  
		Size: 3.8 MB (3758917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042b45107ed5067aa1ef3ef9bcd0de602e64a9bbbbe08caa0d2d698499be1e0`  
		Last Modified: Thu, 24 Mar 2022 22:32:38 GMT  
		Size: 98.1 MB (98053403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc11abe74b2c5176c796dc6661a6f78212aa478a3594ee0f32a8321e2c4794bf`  
		Last Modified: Thu, 24 Mar 2022 22:32:25 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f863ba1bdda0ffe9f5f436f06cea437ddec40c4389ca35659d95b530b17b62d`  
		Last Modified: Thu, 24 Mar 2022 22:32:25 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a99ece30adeb87836f98d023973389712ab30295784852bfc1293c288233655`  
		Last Modified: Thu, 24 Mar 2022 22:32:23 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89161c12d0ca30973699d0dddcd76b74ef86dd8e874daecb31e8370dc142cc`  
		Last Modified: Thu, 24 Mar 2022 22:32:24 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91617e9382b21ee70cba99bf35547aa12168c263d001bb28368cc1056d2cb0e`  
		Last Modified: Thu, 24 Mar 2022 22:32:24 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad14c681b2dad0c73d7803daea960f31b1a938b1d8b34c14ee8ce3a540a9211`  
		Last Modified: Thu, 24 Mar 2022 22:32:23 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d10bfb026577be35e9e4a07bfabdb6c050fcccf3f72bf2e8576dc468736d32`  
		Last Modified: Thu, 24 Mar 2022 22:32:23 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
