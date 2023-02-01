## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:9c17f0465668045e97cca06b20b98a4c32889cf449e51fdc4dab2f9bcd9e9c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b78362e1f11f8edd109c2729c31a4816830c9cb5a94aedfc18a4134fb06e43b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338568155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ca23e2a7605755e322d256315703c1db8f059c9b16bb984b065d8a4d99548c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Feb 2023 03:18:17 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Wed, 01 Feb 2023 03:54:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=aa985dd8298e2f82f744a0dc4693369aad26afff0338c14459fc3331e43ef143 NEO4J_TARBALL=neo4j-community-5.4.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 01 Feb 2023 03:54:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.4.0-unix.tar.gz
# Wed, 01 Feb 2023 03:54:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.4.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 01 Feb 2023 03:54:23 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 01 Feb 2023 03:54:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.4.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 03:54:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 03:54:35 GMT
WORKDIR /var/lib/neo4j
# Wed, 01 Feb 2023 03:54:35 GMT
VOLUME [/data /logs]
# Wed, 01 Feb 2023 03:54:36 GMT
EXPOSE 7473 7474 7687
# Wed, 01 Feb 2023 03:54:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 01 Feb 2023 03:54:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5222c39363e9ad4cf3befb9bb980d24da88c73d38324ec54e4613c745a424`  
		Last Modified: Wed, 01 Feb 2023 03:33:57 GMT  
		Size: 192.4 MB (192438216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74af1d46a83637c0ef9a65bcf1d6a51c2db69d85f12eee97ee2c202a3eeb91cc`  
		Last Modified: Wed, 01 Feb 2023 03:55:58 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b728bca9ce26168a174da813783d77ebf8b10da1c22a9206a32fbe45f90293e`  
		Last Modified: Wed, 01 Feb 2023 03:55:58 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a51226b2472eae83267ee4067cc3151e287a8ab0556145740f92fa1932e09c`  
		Last Modified: Wed, 01 Feb 2023 03:56:03 GMT  
		Size: 114.7 MB (114720760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bf1d85b1081fd556288f0c204756b4db616740b5c4e88badcf1d443ca4d298ed
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335896449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da0dd68954d57ef80e0675d9a718b3246fb314e948876f4fef7943b654cb1cf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 20:54:33 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Tue, 31 Jan 2023 21:57:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=aa985dd8298e2f82f744a0dc4693369aad26afff0338c14459fc3331e43ef143 NEO4J_TARBALL=neo4j-community-5.4.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Jan 2023 21:57:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.4.0-unix.tar.gz
# Tue, 31 Jan 2023 21:57:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.4.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Jan 2023 21:57:35 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 31 Jan 2023 21:57:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.4.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 21:57:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 21:57:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Jan 2023 21:57:50 GMT
VOLUME [/data /logs]
# Tue, 31 Jan 2023 21:57:50 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Jan 2023 21:57:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Jan 2023 21:57:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a105a97fdf20185e2d7c3fa185a80f146fc82f987de1e73befa061b450f1bf`  
		Last Modified: Tue, 31 Jan 2023 21:07:37 GMT  
		Size: 191.3 MB (191260408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a5c4e04f9bcf426624cdddd72be1ee3b881e3343b3b4fdba019406e3e19c4`  
		Last Modified: Tue, 31 Jan 2023 21:59:10 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b40a34bc69773588a218a7f59e57a44423c30b870271af697637e0b998a823`  
		Last Modified: Tue, 31 Jan 2023 21:59:10 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7e2b8dcc69dc7857585c0a42bb279013e506142b19e3dcb30ca055674272b`  
		Last Modified: Tue, 31 Jan 2023 21:59:15 GMT  
		Size: 114.6 MB (114578996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
