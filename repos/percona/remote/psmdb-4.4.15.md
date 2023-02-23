## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:1bac1eec82407d9a258d7e9aed6018912680e8afb09aa7a06d232b68221338e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:f3ed02514e06b292ef4a2fad0851318443810beed3fbae2ce29c1d4844afb3cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198158203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c5b545219a0c51b7e900b2026a4e0676bd70f00eab4180d5bcff5a85af3632`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Feb 2023 19:36:57 GMT
ADD file:38641c1822a4aea5527f6e7429caaa41595e7c7e63f993b0b4787b70ca1e56e2 in / 
# Thu, 23 Feb 2023 19:36:58 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:00:32 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 23 Feb 2023 20:03:25 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Thu, 23 Feb 2023 20:03:26 GMT
ENV PSMDB_VERSION=4.4.15-15
# Thu, 23 Feb 2023 20:03:26 GMT
ENV OS_VER=el8
# Thu, 23 Feb 2023 20:03:26 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Thu, 23 Feb 2023 20:03:26 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 23 Feb 2023 20:04:06 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 23 Feb 2023 20:04:07 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 23 Feb 2023 20:04:07 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 23 Feb 2023 20:04:07 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 23 Feb 2023 20:04:07 GMT
ENV GOSU_VERSION=1.11
# Thu, 23 Feb 2023 20:04:10 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 23 Feb 2023 20:04:12 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 23 Feb 2023 20:04:12 GMT
VOLUME [/data/db]
# Thu, 23 Feb 2023 20:04:12 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 23 Feb 2023 20:04:12 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Thu, 23 Feb 2023 20:04:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Feb 2023 20:04:13 GMT
EXPOSE 27017
# Thu, 23 Feb 2023 20:04:13 GMT
USER 1001
# Thu, 23 Feb 2023 20:04:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3f135a9ee79c5ecc3e253037715137cd16bdf017f4dcf3900b517a7a2e0c1e8`  
		Last Modified: Thu, 23 Feb 2023 19:37:47 GMT  
		Size: 88.4 MB (88421873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1ebecd5f91dad278f98503fc18d37bbca49f0bf3850471b492fd5ebee01fc2`  
		Last Modified: Thu, 23 Feb 2023 20:07:20 GMT  
		Size: 3.8 MB (3765185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda230c12a0123e23cf951a49ee98310d04b857f67e4341a7d19a52c219ed554`  
		Last Modified: Thu, 23 Feb 2023 20:07:30 GMT  
		Size: 96.9 MB (96885091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd00f99480e5b4b6cc814559aad01fb79091c8b9d3b7be5db1239463413c556`  
		Last Modified: Thu, 23 Feb 2023 20:07:19 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c37e93cf588401d13867a71c715ba7205cfb481a6278c8ccd8537f84beac158`  
		Last Modified: Thu, 23 Feb 2023 20:07:18 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a7a8566f6b39422c9c4d06179263c931975363529afcbf4c46637fd81f73fd`  
		Last Modified: Thu, 23 Feb 2023 20:07:17 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0d27bd8b5bca098c2dc956742e1a5fc82f83f09b6a2e916c3b59cdb49014a8`  
		Last Modified: Thu, 23 Feb 2023 20:07:17 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559115bad7537924e7e50406ec74636dca271f514b80799f02d87a0f24e76f`  
		Last Modified: Thu, 23 Feb 2023 20:07:18 GMT  
		Size: 8.1 MB (8137896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f98cefc27b4335b8c5db2971785308ebe1722533cae6dda6e744214679b69`  
		Last Modified: Thu, 23 Feb 2023 20:07:17 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b024c028c5106d56190844d6d723cd5501126f0fd2c66f152cf57600665d32`  
		Last Modified: Thu, 23 Feb 2023 20:07:17 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
