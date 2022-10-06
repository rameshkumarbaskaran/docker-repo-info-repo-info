## `neo4j:latest`

```console
$ docker pull neo4j@sha256:5ff678d279d428ddd6f6a7c7810310e91d7cc736a3b587dd98faf7f234cc3e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:1344ce62601a86f8c9a8f4f7305871ab051720460a72c20f2afb7fb909453def
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364653536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc240a92092bffd97d59687f2a111c0b3ecb9220b5bf23fe66bbf70dee9a1f55`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:34:29 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Wed, 05 Oct 2022 04:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 05 Oct 2022 04:25:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Wed, 05 Oct 2022 04:25:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 05 Oct 2022 04:25:05 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Wed, 05 Oct 2022 04:25:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:25:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:25:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Oct 2022 04:25:18 GMT
VOLUME [/data /logs]
# Wed, 05 Oct 2022 04:25:18 GMT
EXPOSE 7473 7474 7687
# Wed, 05 Oct 2022 04:25:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 04:25:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd943cda847b9f3402014ae85cb3f413d8a8197a5743326a30702a399bd52788`  
		Last Modified: Wed, 05 Oct 2022 01:48:04 GMT  
		Size: 198.1 MB (198124862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1330d3a02981b4aef7ae05c4a0d9e1f5f898998168090c81762a56310a8a753d`  
		Last Modified: Wed, 05 Oct 2022 04:30:38 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b73f556122d0352210097ad4edb45a89f02bd5f94fe288050d15af5a549aab7`  
		Last Modified: Wed, 05 Oct 2022 04:30:38 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9961b29c11c1a040b3ac66ccc7429adf17ab28a35d458b2b98a196eeef697fc4`  
		Last Modified: Wed, 05 Oct 2022 04:30:45 GMT  
		Size: 135.1 MB (135097102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c70d90d7265c20a245060235d93805f7f8fa67727ce142996892edde9dfc12a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359691107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb9a2c28b342a8c31e6c153314cd090b30babcf06fe543dbff7ed590e5fbfe9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Thu, 06 Oct 2022 04:10:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 06 Oct 2022 04:10:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Thu, 06 Oct 2022 04:10:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 06 Oct 2022 04:10:49 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Thu, 06 Oct 2022 04:11:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 04:11:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 04:11:02 GMT
WORKDIR /var/lib/neo4j
# Thu, 06 Oct 2022 04:11:03 GMT
VOLUME [/data /logs]
# Thu, 06 Oct 2022 04:11:04 GMT
EXPOSE 7473 7474 7687
# Thu, 06 Oct 2022 04:11:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 04:11:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a787024fd45ad869b464f1fe76a4cf09fda26077e5197ff4a5c924cb3e5cfab6`  
		Last Modified: Thu, 06 Oct 2022 04:14:28 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704636ce0269c958001dea680edfcfb4553c718e859454ea456343cd57380271`  
		Last Modified: Thu, 06 Oct 2022 04:14:28 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fd363331e26e0cc51a1b98185f63184d93d11e52d7e5f4fe77a799601a27c2`  
		Last Modified: Thu, 06 Oct 2022 04:14:38 GMT  
		Size: 134.7 MB (134748701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
