## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:1a245032443a99c2b7cc5b198b4a0037cb8c8396f580e7d1f4f35df29c637cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:70ffd342cd0aebf3d3e78ee271d64b7476c1ad85d4f82a0c40b2850b355a7c48
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218393779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc72685c6fa3c2f1529c6794b48513d514c77638b88d1027db7e76fc2f2d9e3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:56:15 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 15 Sep 2021 19:00:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Fri, 08 Oct 2021 17:29:07 GMT
ENV PSMDB_VERSION=4.4.9-10
# Fri, 08 Oct 2021 17:29:07 GMT
ENV OS_VER=el8
# Fri, 08 Oct 2021 17:29:07 GMT
ENV FULL_PERCONA_VERSION=4.4.9-10.el8
# Fri, 08 Oct 2021 17:29:08 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Oct 2021 17:29:38 GMT
RUN set -ex;     dnf install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         oniguruma         jq         dnf-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     dnf clean all;     dnf -y remove dnf-utils;     rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Oct 2021 17:29:39 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 08 Oct 2021 17:29:40 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Oct 2021 17:29:40 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Oct 2021 17:29:41 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Oct 2021 17:29:45 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Oct 2021 17:29:47 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Oct 2021 17:29:48 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 08 Oct 2021 17:29:49 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 08 Oct 2021 17:29:49 GMT
VOLUME [/data/db]
# Fri, 08 Oct 2021 17:29:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Oct 2021 17:29:49 GMT
EXPOSE 27017
# Fri, 08 Oct 2021 17:29:49 GMT
USER 1001
# Fri, 08 Oct 2021 17:29:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4a021af05ac4cdbe7625bc925b41c1bb50a7a385f4fc3dab431a07d712364d`  
		Last Modified: Wed, 15 Sep 2021 19:07:16 GMT  
		Size: 29.0 MB (28996777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c72bf3cbe7339a6cb91be4376ace8a0616f250d6ec146b8db7a3268db24aafa`  
		Last Modified: Fri, 08 Oct 2021 17:31:05 GMT  
		Size: 96.8 MB (96792513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de47aa321cf2aafebaa702288fe7ef722db505739af3981996de664430be6de`  
		Last Modified: Fri, 08 Oct 2021 17:30:53 GMT  
		Size: 1.5 KB (1541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fdc13b654cc3fa9b82a7186c28915fc4406e39174476148eadd5163876f816`  
		Last Modified: Fri, 08 Oct 2021 17:30:53 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c8102bf73d831abdec9820699daa8df3fe1c5cf481ff69aeba78144761b8fc`  
		Last Modified: Fri, 08 Oct 2021 17:30:51 GMT  
		Size: 10.6 KB (10573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6c9d2dbdd772da46a7e697fc45acf3fb379185682d88af7f58fddb3f351ddb`  
		Last Modified: Fri, 08 Oct 2021 17:30:51 GMT  
		Size: 914.5 KB (914540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe74822d9b9a15393ca341767582396dbd490386b7ecd04c5f8f12debb2e8c1`  
		Last Modified: Fri, 08 Oct 2021 17:30:52 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bcee84b935141816b3c773457065b8c301dc7a8ee3861f161c14bede5c2ef5`  
		Last Modified: Fri, 08 Oct 2021 17:30:50 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6b5c3585416016350db51917050dcb097da088d152f5764c51ddcf56f8a180`  
		Last Modified: Fri, 08 Oct 2021 17:30:51 GMT  
		Size: 4.6 KB (4556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
