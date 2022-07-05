## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:2e9cd41553530153611177dd9322ea59db782e5ec03efa3df6186b633607a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:b1982c2abb7804ccfe706cbd95bfdc4946cf50c9e9abae15a7c1638ea2b564f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210786815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19419ae69c670e4351fef58bed58febf8420c7830f42f4090480a12557f3dc07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:24 GMT
ADD file:05afe15e1c394de999f38bb2413c80af18f129511261f53511fe21e4606b6353 in / 
# Tue, 05 Jul 2022 22:20:24 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:42:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 05 Jul 2022 22:43:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Tue, 05 Jul 2022 22:43:34 GMT
ENV PSMDB_VERSION=5.0.9-8
# Tue, 05 Jul 2022 22:43:34 GMT
ENV OS_VER=el8
# Tue, 05 Jul 2022 22:43:34 GMT
ENV FULL_PERCONA_VERSION=5.0.9-8.el8
# Tue, 05 Jul 2022 22:43:34 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 05 Jul 2022 22:44:11 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 05 Jul 2022 22:44:12 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 05 Jul 2022 22:44:12 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 05 Jul 2022 22:44:12 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 05 Jul 2022 22:44:13 GMT
ENV GOSU_VERSION=1.11
# Tue, 05 Jul 2022 22:44:16 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 05 Jul 2022 22:44:20 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 05 Jul 2022 22:44:20 GMT
VOLUME [/data/db]
# Tue, 05 Jul 2022 22:44:21 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 05 Jul 2022 22:44:21 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Tue, 05 Jul 2022 22:44:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Jul 2022 22:44:21 GMT
EXPOSE 27017
# Tue, 05 Jul 2022 22:44:21 GMT
USER 1001
# Tue, 05 Jul 2022 22:44:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:15a6facc77411902de6b8de2d42125695286cd602d17db01f09239a7f6f8992a`  
		Last Modified: Tue, 05 Jul 2022 22:21:25 GMT  
		Size: 84.6 MB (84566504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507bb491470da74e13470538d02b492fbae683cb1f62930a68a14d1db4a5cc81`  
		Last Modified: Tue, 05 Jul 2022 22:47:47 GMT  
		Size: 3.7 MB (3734429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1207174de860b44477fbc12462da0e077faac5d67dc87ecef7392619747c6033`  
		Last Modified: Tue, 05 Jul 2022 22:48:01 GMT  
		Size: 113.4 MB (113399838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbd6880ef33557f3982cf169a3b3a081f6f86af70967a6a91b644e4e922d104`  
		Last Modified: Tue, 05 Jul 2022 22:47:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a065986fdd0fbf790a4935199ede32f0cf0b9e795479ddfe6e199221996a05d`  
		Last Modified: Tue, 05 Jul 2022 22:47:46 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaef3d6be6236c98e3785b6656d576a72ece114f7c9d2ed1ae32fcb00323219`  
		Last Modified: Tue, 05 Jul 2022 22:47:44 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7600d91c5bdc53affcf3ac842adbfac2e4f029d8f79801b8b8e397589322319a`  
		Last Modified: Tue, 05 Jul 2022 22:47:44 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22440636dfa67ed159580b257d168deb4f58c8e70d08fc2ff4cfbe39607dc8d3`  
		Last Modified: Tue, 05 Jul 2022 22:47:45 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da529862b3a676cedeb438fb830a752aee0cdfaf68c09af642ca4205eb2a7b4`  
		Last Modified: Tue, 05 Jul 2022 22:47:44 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07e92862ceac036cd21b3524e5bd4baab1e893f9307ff2fbb2f96b6398773f0`  
		Last Modified: Tue, 05 Jul 2022 22:47:44 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
