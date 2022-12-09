## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:83ca269245f040232943592286e7571bde40751e73290489d657cf32d7b29d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:4ea502847e26beee2b5c47edc1581752e26dcafe47b1f1222e1d4933b99219a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432869753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9f83ddfd18e220f9c1df1c1bba91502212c1ab5fa9884c9f29e5a6276784cc`
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
# Fri, 09 Dec 2022 07:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 07:24:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Fri, 09 Dec 2022 07:24:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 07:24:28 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Fri, 09 Dec 2022 07:24:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 07:24:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 07:24:42 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 07:24:43 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 07:24:43 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 07:24:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 07:24:43 GMT
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
	-	`sha256:8e306e07ea3b58d1bb17833cb009a17b11f525413b51212b50f4cad9766a7446`  
		Last Modified: Fri, 09 Dec 2022 07:27:07 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c31c28f54c78bde862fd5399bfa609c84a57e321cc2dbf8b3ea478834b2a8bc`  
		Last Modified: Fri, 09 Dec 2022 07:27:07 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb9711d68ddc6a87e7849d94542ba7ec5ed728aff66bd5e496d6c47e33c6a63`  
		Last Modified: Fri, 09 Dec 2022 07:27:21 GMT  
		Size: 209.0 MB (209013614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:18d6289eba4991525677f122ab0d3eec3b57e9e5c00452bb31ca72e799fdf808
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430158080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485602c515591203d5f46c0966061d90e17c8aec5ed7a94fc61fd846060e30c0`
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
# Fri, 09 Dec 2022 06:04:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:04:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Fri, 09 Dec 2022 06:04:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:04:38 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Fri, 09 Dec 2022 06:04:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:04:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:04:56 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:04:56 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:04:56 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:04:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:04:57 GMT
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
	-	`sha256:f5d26ef527972959e82e9c8c5dadeeed2ce449840d705813c3bb65e26187c3d8`  
		Last Modified: Fri, 09 Dec 2022 06:06:15 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3098263ed95b81de5db6fdbde47099d8ee8603c6e4852db3a552ba58b91e66ee`  
		Last Modified: Fri, 09 Dec 2022 06:06:15 GMT  
		Size: 8.2 KB (8164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7080f7dc677d1ade020cb3417f0e9b6b7ac79456c207e0d41f69695ae2a9159a`  
		Last Modified: Fri, 09 Dec 2022 06:06:24 GMT  
		Size: 208.9 MB (208870505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
