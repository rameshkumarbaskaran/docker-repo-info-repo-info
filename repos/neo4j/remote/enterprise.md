## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:be98efd9aff8d0d249a83de6e99240bbc18a4947ce9250269d418796380f5d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:631f6f6c38f7f4ec8c242c835170dd208889b6ff1d1974cd91c0befd909abd57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617745683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355d4b7934f264f871f69865b91102fe63a65413e2e8fd09238b57a3c35c3c1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:58 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:20:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:20:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:20:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:20:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:20:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeefc867edcf7d51cc01312e1d1db4f53976bc6bbc672ee592afe405e904eb4`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2c974f3c0a61eb19c39c57031e709c5175b072d83a0adad056aedeab6a702`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90970750e9471bcf7f345847d4ca2adec9d10d0f5f0df02b0c8d1cd0b4b0d5c3`  
		Last Modified: Fri, 16 Jun 2023 05:22:16 GMT  
		Size: 393.7 MB (393734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cfec950d9c31b4df89a939d4de7829983af3f81b2c7afe3c5446fecd02751e99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615092666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb00dc5565a54825adbb04844c0fd2a37198485fc9026fd237a4b7bd9763b61`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:47:00 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:44:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:21 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:44:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:40 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:40 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:40 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589855d0c7aebd4ca2b50aaf622d291cd44875676cdd56512b687b47b80c59ad`  
		Last Modified: Fri, 16 Jun 2023 04:57:17 GMT  
		Size: 191.4 MB (191387665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33435c570e9f3fcb5453b4d4520a476d438fe8d13a74356aebd1a12bc85e08c2`  
		Last Modified: Fri, 16 Jun 2023 05:45:48 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90f0276d98722fb9f100f91ea807eea4c2001db116637d5bd558bdaca492066`  
		Last Modified: Fri, 16 Jun 2023 05:45:48 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e3b28e73cca72045c5e9fab15d02e29629d102febc8b7cefd46577510d0ed`  
		Last Modified: Fri, 16 Jun 2023 05:46:01 GMT  
		Size: 393.6 MB (393628913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
