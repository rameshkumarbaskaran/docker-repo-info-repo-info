## `neo4j:latest`

```console
$ docker pull neo4j@sha256:7fc91f2c16cf52dadb125b320c9a547d2d7a9565b6b96e6639b374025d5f56c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:eb626e4b6c5956c190e864ec7ea2d2d3c1975cfbc3bef446130e8320c78f3049
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336774731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0393f054dc7f833476289501bc72fe55784c0b99914fc06f47260e236a2b46b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:49:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 06:42:08 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Fri, 09 Dec 2022 07:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 07:24:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Fri, 09 Dec 2022 07:24:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 07:24:10 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Fri, 09 Dec 2022 07:24:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 07:24:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 07:24:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 07:24:23 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 07:24:23 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 07:24:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 07:24:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72b40014e8ed7c4beca3427f678152536843fa5317d5c90ba564c8f93f170d1`  
		Last Modified: Fri, 09 Dec 2022 06:57:07 GMT  
		Size: 192.4 MB (192431264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f953c3133dea11ad4119388794c08351dc59d033b148b1e21dd2540c8a259d2e`  
		Last Modified: Fri, 09 Dec 2022 07:26:43 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3dc3a881de5b61d1b4a16220ccfbd608609af9e93c1e40aad4f5ff4213887d2`  
		Last Modified: Fri, 09 Dec 2022 07:26:43 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39a521fdef67208223f07ba77bd966d4ecaaeb47832a52d59e091d0d8d405db`  
		Last Modified: Fri, 09 Dec 2022 07:26:50 GMT  
		Size: 112.9 MB (112918594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:66a86b47786f9ece3d499c8112d71916663da0dd2229f0ccbfb4652f628d2168
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3924171754e99a92127c8f1fafed34be8fc1c81da16500dc3be5e1e37431dde`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 05:08:26 GMT
COPY dir:533cfee1c12b6052cd1297ebc89704c8b7da6e8016c06b0e341bcec0d4934dde in /opt/java/openjdk 
# Fri, 09 Dec 2022 06:04:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:04:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Fri, 09 Dec 2022 06:04:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:04:23 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Fri, 09 Dec 2022 06:04:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:04:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:04:33 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:04:33 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:04:33 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:04:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:04:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252cfa205e433a4c57ba726668ab09a5be5ab3251c8c31999a816013f05f5e54`  
		Last Modified: Fri, 09 Dec 2022 05:21:35 GMT  
		Size: 191.2 MB (191215205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4438ae9db4dc6039bc424a68c980ce15d81123c7217b787cc8f1555cd3ee9900`  
		Last Modified: Fri, 09 Dec 2022 06:05:52 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadab086183024cd7601e4f6521c502a33abac72a24df0c10394c3ada6195c0`  
		Last Modified: Fri, 09 Dec 2022 06:05:52 GMT  
		Size: 8.2 KB (8163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391d1c9dfc0b8451b1db0a957e1c30e888bd8adb73a3d600c11e261847e08805`  
		Last Modified: Fri, 09 Dec 2022 06:05:57 GMT  
		Size: 112.8 MB (112775836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
