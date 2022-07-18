## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:2c782fb8a75ac9133cc6d6d8938bbbfbc633a4927170a37e2674c91f43cf7e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9509c61962fe2a0b0108bbbdfa54113abf0803ba4804773eb259a564dbb1b8d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.5 MB (452467458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12108c3da840aed3439b94b46d992005f12a7a1c090bd1bede05a279036fa5c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Mon, 18 Jul 2022 19:33:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Jul 2022 19:33:31 GMT
COPY dir:8a7a1a18581d889adcfd1186d888a3c0783c2e9ca30258d92ae2f7ddfc431a7e in /opt/java/openjdk 
# Mon, 18 Jul 2022 19:33:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=747b2e71b273d8f0dd82cdb594aca02b87f03f445d2ee5eaba561c8ebd474bb0 NEO4J_TARBALL=neo4j-enterprise-4.4.9-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Jul 2022 19:33:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
# Mon, 18 Jul 2022 19:33:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 18 Jul 2022 19:33:34 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Mon, 18 Jul 2022 19:34:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 18 Jul 2022 19:34:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 19:34:06 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Jul 2022 19:34:06 GMT
VOLUME [/data /logs]
# Mon, 18 Jul 2022 19:34:06 GMT
EXPOSE 7473 7474 7687
# Mon, 18 Jul 2022 19:34:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Jul 2022 19:34:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301c27b952ac1335cb3ce07c0ac8557ec53361ae2213e344a692db860b0bcb83`  
		Last Modified: Mon, 18 Jul 2022 19:38:19 GMT  
		Size: 194.1 MB (194084239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c32ad33207a64c09eb5ea5b318a6a1258c293ff11b685d650d6e2daec69aa6`  
		Last Modified: Mon, 18 Jul 2022 19:38:03 GMT  
		Size: 3.9 KB (3854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd49f32ad01c249cf60866056a143446d860abceb6ee4347b9c1ad57d55cb6e`  
		Last Modified: Mon, 18 Jul 2022 19:38:03 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b784b446eed8f71355a03c4f2f08d5ab0c4290fdbb56fd0bcc04009566b7a2bf`  
		Last Modified: Mon, 18 Jul 2022 19:38:16 GMT  
		Size: 227.0 MB (227005142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:60dbd85ff54e6da3b245d03e65375f4fe9448b4795fd40da605aee27f45f7630
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.8 MB (447751976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc93bebfc92be94804b01e454101c753bdba7e2fa7ed993eb09f41a101c5e644`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Mon, 18 Jul 2022 18:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Jul 2022 18:51:11 GMT
COPY dir:6d7893b3ef4e7fadacd7bd0fc5d1c4de6ba46fcc57327ac0eab7c3d3c797493e in /opt/java/openjdk 
# Mon, 18 Jul 2022 18:51:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=747b2e71b273d8f0dd82cdb594aca02b87f03f445d2ee5eaba561c8ebd474bb0 NEO4J_TARBALL=neo4j-enterprise-4.4.9-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Jul 2022 18:51:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
# Mon, 18 Jul 2022 18:51:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 18 Jul 2022 18:51:15 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Mon, 18 Jul 2022 18:51:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 18 Jul 2022 18:51:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 18:51:38 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Jul 2022 18:51:39 GMT
VOLUME [/data /logs]
# Mon, 18 Jul 2022 18:51:40 GMT
EXPOSE 7473 7474 7687
# Mon, 18 Jul 2022 18:51:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Jul 2022 18:51:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9785e470015004852978bde18f43280b8784d3bce154a9eb78c2684a51a7d8`  
		Last Modified: Mon, 18 Jul 2022 18:54:31 GMT  
		Size: 190.8 MB (190824650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520af2ff7721a9a399c464c6e77113dd685a79a70adef91f23973eeb904ad6b2`  
		Last Modified: Mon, 18 Jul 2022 18:54:15 GMT  
		Size: 3.8 KB (3831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3b05ca6088fd1580135bbab2a47ab2927584cfe6121be50e3982191eb1726b`  
		Last Modified: Mon, 18 Jul 2022 18:54:15 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7343b2008aee1a5eda73d483d67ae4c763e3eef7fc2b9c08d99d443ae22ec3d`  
		Last Modified: Mon, 18 Jul 2022 18:54:32 GMT  
		Size: 226.9 MB (226861684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
