## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:016a88c4c7965bfc53aeedd5e85e41ba85c52f31547e79ea1f9ba4bbd32102fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:ee383ec645430096c991223e027824c70d4fb916397abc9e047a5e6453715d8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213554350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b78aec69013dc280defef196996807c5dab5b50215e7beb8e282a78cc9d09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Feb 2023 19:36:57 GMT
ADD file:38641c1822a4aea5527f6e7429caaa41595e7c7e63f993b0b4787b70ca1e56e2 in / 
# Thu, 23 Feb 2023 19:36:58 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:00:32 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 23 Feb 2023 20:02:02 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Thu, 23 Feb 2023 20:02:02 GMT
ENV PSMDB_VERSION=5.0.10-9
# Thu, 23 Feb 2023 20:02:02 GMT
ENV OS_VER=el8
# Thu, 23 Feb 2023 20:02:02 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Thu, 23 Feb 2023 20:02:02 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 23 Feb 2023 20:02:43 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 23 Feb 2023 20:02:44 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 23 Feb 2023 20:02:44 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 23 Feb 2023 20:02:45 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 23 Feb 2023 20:02:45 GMT
ENV GOSU_VERSION=1.11
# Thu, 23 Feb 2023 20:02:49 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 23 Feb 2023 20:03:09 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 23 Feb 2023 20:03:10 GMT
VOLUME [/data/db]
# Thu, 23 Feb 2023 20:03:10 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 23 Feb 2023 20:03:10 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Thu, 23 Feb 2023 20:03:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Feb 2023 20:03:11 GMT
EXPOSE 27017
# Thu, 23 Feb 2023 20:03:11 GMT
USER 1001
# Thu, 23 Feb 2023 20:03:11 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3f135a9ee79c5ecc3e253037715137cd16bdf017f4dcf3900b517a7a2e0c1e8`  
		Last Modified: Thu, 23 Feb 2023 19:37:47 GMT  
		Size: 88.4 MB (88421873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb779f19b957e705134e941e014a5ee77c4aa054eed329b99ef7998ef82ba03e`  
		Last Modified: Thu, 23 Feb 2023 20:06:55 GMT  
		Size: 3.8 MB (3765137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d16fd9cc8477af66c58e397e87f58c1a6e08630d88679cfa6d152a5a540aa59`  
		Last Modified: Thu, 23 Feb 2023 20:07:07 GMT  
		Size: 112.3 MB (112281292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44774ae4df5ca9343cb794f0b5c384cb08511903383761b9a3f2a165ec894e`  
		Last Modified: Thu, 23 Feb 2023 20:06:54 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a5b7b7e73e756f7faa5d069d23a56a4a49f0a3c21a89f95d1a82fcd0c7afb8`  
		Last Modified: Thu, 23 Feb 2023 20:06:54 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4618c6070682f9b2a1174014cada71f740420dc2373fcecb24d6f0192651c4e`  
		Last Modified: Thu, 23 Feb 2023 20:06:52 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51126c3b56982af48bc9e73517ec035e51005adfc522542b87565d7ef9ae1c92`  
		Last Modified: Thu, 23 Feb 2023 20:06:52 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5fb7eb941b63de8cd437ab8f840a6d50f78845eb9dfd6ff6e2c93255876ecd`  
		Last Modified: Thu, 23 Feb 2023 20:06:53 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f4abe305702c8a8546992a0f240239ebac024b12c884d691db3c04881c745`  
		Last Modified: Thu, 23 Feb 2023 20:06:52 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ea0e20e79f5c20f15a4ef3c43134779b9e942710d504188aa5fc77a543af84`  
		Last Modified: Thu, 23 Feb 2023 20:06:52 GMT  
		Size: 4.6 KB (4560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
