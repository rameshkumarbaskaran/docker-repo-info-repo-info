## `neo4j:latest`

```console
$ docker pull neo4j@sha256:31430902c1d2d28b8a49d55c9b926004ffded93a4772b99d6130b17edcf05cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:4b11a8b0c2cec8dfbdd3274371cbb4a9fe79f565e612902a6b51bd60535c4b10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364537737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc89d6f86cb9481affa84f327ca823b90e7a3bb4005624a4d22578a703add589`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:41:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Aug 2022 20:31:01 GMT
COPY dir:4ac06325a949f27c5b8adffe7355734c386bdf2f83321bf468ad13369e38083f in /opt/java/openjdk 
# Wed, 24 Aug 2022 20:31:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=869ecb89ce36fe457b4d4c4fcaa48fdf2f2d739c45323bd2c8ccdf09aa11abbf NEO4J_TARBALL=neo4j-community-4.4.10-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Aug 2022 20:31:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
# Wed, 24 Aug 2022 20:31:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 24 Aug 2022 20:31:04 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Wed, 24 Aug 2022 20:31:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 20:31:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 20:31:17 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Aug 2022 20:31:17 GMT
VOLUME [/data /logs]
# Wed, 24 Aug 2022 20:31:17 GMT
EXPOSE 7473 7474 7687
# Wed, 24 Aug 2022 20:31:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Aug 2022 20:31:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678de0068bf989d0a4913f5dece0aa034375ede2155af4c764d1584d108e37ba`  
		Last Modified: Wed, 24 Aug 2022 20:38:13 GMT  
		Size: 198.1 MB (198124721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168723be7915111d5e8075904fce394e596e3208e56924d8dccb41f25e6763f`  
		Last Modified: Wed, 24 Aug 2022 20:37:58 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46c733a9a1f212de7fd277080b0cfac03d638137e9378b9fea408a9941605fa`  
		Last Modified: Wed, 24 Aug 2022 20:37:57 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80623e2bc92f5adc51f72073c59271fe6f45914e62624510a6236438b13b090d`  
		Last Modified: Wed, 24 Aug 2022 20:38:05 GMT  
		Size: 135.0 MB (135020061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d620a2d74545a7e6d79e0daeaa09477cebc0c3d1f0d13d2ae7d108abbc271fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.6 MB (359616679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966431d1db10612e5bcfe082e73f6c3bcad507c746df7ed0602b14f1990389d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:32:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Aug 2022 04:32:44 GMT
COPY dir:e5bd61f4facd9326f475d46e6508e132d506189701c632d2ef4b1f956f5e2ab5 in /opt/java/openjdk 
# Tue, 23 Aug 2022 04:32:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=869ecb89ce36fe457b4d4c4fcaa48fdf2f2d739c45323bd2c8ccdf09aa11abbf NEO4J_TARBALL=neo4j-community-4.4.10-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 Aug 2022 04:32:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
# Tue, 23 Aug 2022 04:32:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 Aug 2022 04:32:48 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 23 Aug 2022 04:33:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:33:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 04:33:04 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 Aug 2022 04:33:05 GMT
VOLUME [/data /logs]
# Tue, 23 Aug 2022 04:33:06 GMT
EXPOSE 7473 7474 7687
# Tue, 23 Aug 2022 04:33:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 04:33:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1739fac7dfc2b6ca0ffb38b5bf8c72de0c913b4dcfc6025436f79f67d52c11ff`  
		Last Modified: Tue, 23 Aug 2022 04:37:28 GMT  
		Size: 194.9 MB (194869157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28f077711aa68114de401584d1738f902d5c29eaf04da3f376a538275fbe62`  
		Last Modified: Tue, 23 Aug 2022 04:37:11 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af004c5c9d30eee88713ae52b39368b734293ca5c0859254d5e64c70a2d277f9`  
		Last Modified: Tue, 23 Aug 2022 04:37:11 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0c8212e816c7edf85e4d36abc071d46824e6c958fd95c8ea5f641e8d3e7571`  
		Last Modified: Tue, 23 Aug 2022 04:37:20 GMT  
		Size: 134.7 MB (134672314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
