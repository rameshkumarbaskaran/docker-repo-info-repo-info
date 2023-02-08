## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:c8bd8deb2e19c2dcf511d48058698b53ab022d363bba9d1f5b00595091dc5b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:a3c4f8fc5a98863141f3e349c817b04fe8e7788276604bfbb5385ca1a90a92d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198144014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7103da694c397d72e32bd1da39b3ea014591ff0544529c50ee4a55e201bb72c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:18 GMT
ADD file:345fe34a9ba268db9f89b4c0a24f29fee1910b875b520412a6d6ad5d94e1c29c in / 
# Wed, 08 Feb 2023 19:27:19 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:52:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Feb 2023 19:55:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 08 Feb 2023 19:55:17 GMT
ENV PSMDB_VERSION=4.4.15-15
# Wed, 08 Feb 2023 19:55:18 GMT
ENV OS_VER=el8
# Wed, 08 Feb 2023 19:55:18 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Wed, 08 Feb 2023 19:55:18 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Feb 2023 19:55:57 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 08 Feb 2023 19:55:58 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 08 Feb 2023 19:55:58 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 08 Feb 2023 19:55:59 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 08 Feb 2023 19:55:59 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Feb 2023 19:56:01 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 08 Feb 2023 19:56:03 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 08 Feb 2023 19:56:04 GMT
VOLUME [/data/db]
# Wed, 08 Feb 2023 19:56:04 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 08 Feb 2023 19:56:05 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 08 Feb 2023 19:56:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Feb 2023 19:56:05 GMT
EXPOSE 27017
# Wed, 08 Feb 2023 19:56:05 GMT
USER 1001
# Wed, 08 Feb 2023 19:56:05 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:96ce6f03051e96688aa6d88b3c4959386deafef4048331e1b8f48bd9062e1571`  
		Last Modified: Wed, 08 Feb 2023 19:28:46 GMT  
		Size: 88.4 MB (88416695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad58fb1133e8f81bfb74c83c3ffec7a8ac9f1e9529cc0d6799d2de9d57736ee`  
		Last Modified: Wed, 08 Feb 2023 19:59:07 GMT  
		Size: 3.8 MB (3758748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4319c9c1e5327814037e2b78b5ca78007322b3bb9b9b28f52fd8f874dd42c1a`  
		Last Modified: Wed, 08 Feb 2023 19:59:18 GMT  
		Size: 96.9 MB (96882529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb6c43796b56c7a87760df2165e66ebfbdf9b094fa02477203889f7ced3b70e`  
		Last Modified: Wed, 08 Feb 2023 19:59:05 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3803a88602e8d058c6d90b76bc6ba24daade08b016919d6e6562e3ec2b6c24`  
		Last Modified: Wed, 08 Feb 2023 19:59:06 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ef9fff9466f95b1e0f66a5fa1b5df7afa885f519d6043d6221e5c18dccc48d`  
		Last Modified: Wed, 08 Feb 2023 19:59:04 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc2ce27784683e82732f698f814f8c1c545a8c0cf3524c037a034ea71c58688`  
		Last Modified: Wed, 08 Feb 2023 19:59:04 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a14656ba8c7679c195d487433179f220f35a290820881e895422eb77b1ce06`  
		Last Modified: Wed, 08 Feb 2023 19:59:05 GMT  
		Size: 8.1 MB (8137885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541254f88763f590768ef7e9962e1c45a8f92d5852eb5ba2169aec8fa6ffe851`  
		Last Modified: Wed, 08 Feb 2023 19:59:04 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171444ce228a3a5addb9e00a75d27835c957e04c1da0de18141150afccaf2871`  
		Last Modified: Wed, 08 Feb 2023 19:59:04 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
