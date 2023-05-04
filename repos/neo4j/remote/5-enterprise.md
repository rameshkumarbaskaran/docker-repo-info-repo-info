## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:57d229fe09a56fbae744d670317cb3ade55286f0c0bab7ffae10fcdd77a8a75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0687fdd5019587391c59f3314890c9cbbe74a3bd524a2a96e58438dcad9f001e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.1 MB (604135637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694627db54d52024a8099962173868fd6c657fbf6019c7117ddaced0c1fc5216`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Thu, 04 May 2023 15:21:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ed2a757d3d52b0dd5d37566118e333c4a32568d8b551d47edb62222b37f9486a NEO4J_TARBALL=neo4j-enterprise-5.7.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.7.0-unix.tar.gz
# Thu, 04 May 2023 15:21:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:30 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 15:21:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:21:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:21:47 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:21:47 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:21:47 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:21:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:21:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caeccbe2fe34e37aaed755e800bde512ec96ba67658c499a0e625394b96a2984`  
		Last Modified: Thu, 04 May 2023 15:22:56 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc13bab5e10767fcc54cfe4c2bf6ecab3322895818d219dbbba59881e98b6ba`  
		Last Modified: Thu, 04 May 2023 15:22:57 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abc134aa75fb964857995fcac583e0b5accb36dc421ccf44723e53025c36fff`  
		Last Modified: Thu, 04 May 2023 15:23:11 GMT  
		Size: 380.1 MB (380139109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:94abe8120c5430ab066aea1692491fa9d4ecf8d504a807510d5498a1562eadfa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.4 MB (601449266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d30c05a208e81fc92ba79e35c04df9af40e8950da321169bfa87bf06e621d7d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Thu, 04 May 2023 12:05:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ed2a757d3d52b0dd5d37566118e333c4a32568d8b551d47edb62222b37f9486a NEO4J_TARBALL=neo4j-enterprise-5.7.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:05:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.7.0-unix.tar.gz
# Thu, 04 May 2023 12:05:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:05:07 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 12:05:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:25 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:25 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73a1fc72b29e2bb1ea0dd76ad5507ef446c37ba2ec53af00c078d2f158d3424`  
		Last Modified: Thu, 04 May 2023 12:06:33 GMT  
		Size: 3.9 KB (3891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b19eaac8bbe54d4c8bc4102e86c17dbff7bea7fa395db92ddd87c0dd8ae40c`  
		Last Modified: Thu, 04 May 2023 12:06:33 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa3fe131fde0ce072e7b87753cf16cd5d86a83e95ebe1ea85581e4b7cf01a8f`  
		Last Modified: Thu, 04 May 2023 12:06:45 GMT  
		Size: 380.0 MB (379996227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
