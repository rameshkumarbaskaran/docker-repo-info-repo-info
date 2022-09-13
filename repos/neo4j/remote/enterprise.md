## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:53544639ee1fa746724b266a99779e2e4a7f7d81b14ea8a4eccb05487ec5d4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9321b1f2ab8808b449b317c0da9628a1ee70fe1429155c94679ad7904eea1409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.4 MB (461385036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff3ea0e6dd19cbcb2f0c0a760321ae7dcd32cbc83cb1d38041434afa54c5f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2d62050d2297db74344d3369b6ba1a7e7ae17e71f688f61f4b88c56b08e49969 NEO4J_TARBALL=neo4j-enterprise-4.4.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:19:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:19:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:19:07 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:29 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:29 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f1ead2d0e9e5e1baab7b62a2a27183133fe152824c5ec52c4a9aceda821813`  
		Last Modified: Tue, 13 Sep 2022 06:25:07 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62c4f491f69d7d8cb4ba9ab853e12f4a1d71a4ca56fbe29fb0cf55044187c42`  
		Last Modified: Tue, 13 Sep 2022 06:25:06 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ae8c3b58ef782ea410f33fe07a9de62b5decf1b567df1d9dd900df41629c9`  
		Last Modified: Tue, 13 Sep 2022 06:25:17 GMT  
		Size: 231.8 MB (231844559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:66600f0286e3b0db2f3202d951a44f27fee4bf748065d9fe2be37d7a704b68a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.6 MB (456634844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0418c71f1e407183fa23de34f33ce02f9fead82c8b83cc9d8151b08180370568`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2d62050d2297db74344d3369b6ba1a7e7ae17e71f688f61f4b88c56b08e49969 NEO4J_TARBALL=neo4j-enterprise-4.4.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:59:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:59:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:59:03 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:59:04 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:59:05 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:59:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:59:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b477b03c5968111a707b851d433689c5b3338eace827767d8a4db9151fa36bd4`  
		Last Modified: Tue, 13 Sep 2022 07:02:23 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0c756f2b19b39d7782c220796457bde5dcb5f6251ae3b63cc2170f2cf283ab`  
		Last Modified: Tue, 13 Sep 2022 07:02:23 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800af0660e6941177b5634cef2c8c2438ea31ee1364c5812dc649874f70ddcf7`  
		Last Modified: Tue, 13 Sep 2022 07:02:37 GMT  
		Size: 231.7 MB (231701331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
