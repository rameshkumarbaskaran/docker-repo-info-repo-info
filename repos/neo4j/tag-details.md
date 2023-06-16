<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.21`](#neo4j4421)
-	[`neo4j:4.4.21-community`](#neo4j4421-community)
-	[`neo4j:4.4.21-enterprise`](#neo4j4421-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.9`](#neo4j59)
-	[`neo4j:5.9-community`](#neo4j59-community)
-	[`neo4j:5.9-enterprise`](#neo4j59-enterprise)
-	[`neo4j:5.9.0`](#neo4j590)
-	[`neo4j:5.9.0-community`](#neo4j590-community)
-	[`neo4j:5.9.0-enterprise`](#neo4j590-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:572153b597a340e7b8442217edb1d7525dd42ff6ba9096cadf9cbb28b14a9da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:af0b8351e10f2f66e853c6e959b54e1db780a9e19ab0860844c4769fc456385e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347524303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf473beffa6246d62d4c2569c194944c072628ba6fb73a92647faa1d868e2053`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:20:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:20:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:20:28 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:20:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:20:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:20:43 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:20:43 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:20:43 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:20:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:20:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa0a6975dfa29feaf803c94de20288cd29ca45546487f5eff385ae9655d1f45`  
		Last Modified: Fri, 16 Jun 2023 05:22:31 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3ea6e90d20daee9f17005dbb0cdd2dc10d6fc714bbf2fb166573233bda8c3`  
		Last Modified: Fri, 16 Jun 2023 05:22:31 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76b05814b2acdbff12372926c4d02f76b7c7d39192877d16cd4e9909377482`  
		Last Modified: Fri, 16 Jun 2023 05:22:38 GMT  
		Size: 117.5 MB (117544952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d61fdcd271341e03138b457b6691f86a85e370e690be995613c2f7711cba680
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342801857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aa2ad35dc11706be84886dbfc3211ccaede0b967ba53f6d320811b427adf75`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:42:21 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:44:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:44:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:44 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:44:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:53 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:53 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:53 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f561dc152f6d05a1820783d780247855889a7f67c10ad93e662c845bc4e04b7`  
		Last Modified: Fri, 16 Jun 2023 04:54:22 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d354935fa931e19a8f77a6c42fc6b00ded3220c90cb42cae42e6c5037216e7`  
		Last Modified: Fri, 16 Jun 2023 05:46:13 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb1d5b1ba3df14638b59a633b5694ee365f792344599f925786528df43a66d1`  
		Last Modified: Fri, 16 Jun 2023 05:46:14 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a259fe0e346454f8edb47ada3ba73f02bbdd9cb53d855ebe10fbf8cd621cc`  
		Last Modified: Fri, 16 Jun 2023 05:46:18 GMT  
		Size: 117.4 MB (117402245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:572153b597a340e7b8442217edb1d7525dd42ff6ba9096cadf9cbb28b14a9da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:af0b8351e10f2f66e853c6e959b54e1db780a9e19ab0860844c4769fc456385e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347524303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf473beffa6246d62d4c2569c194944c072628ba6fb73a92647faa1d868e2053`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:20:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:20:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:20:28 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:20:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:20:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:20:43 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:20:43 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:20:43 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:20:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:20:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa0a6975dfa29feaf803c94de20288cd29ca45546487f5eff385ae9655d1f45`  
		Last Modified: Fri, 16 Jun 2023 05:22:31 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3ea6e90d20daee9f17005dbb0cdd2dc10d6fc714bbf2fb166573233bda8c3`  
		Last Modified: Fri, 16 Jun 2023 05:22:31 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76b05814b2acdbff12372926c4d02f76b7c7d39192877d16cd4e9909377482`  
		Last Modified: Fri, 16 Jun 2023 05:22:38 GMT  
		Size: 117.5 MB (117544952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d61fdcd271341e03138b457b6691f86a85e370e690be995613c2f7711cba680
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342801857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aa2ad35dc11706be84886dbfc3211ccaede0b967ba53f6d320811b427adf75`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:42:21 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:44:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:44:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:44 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:44:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:53 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:53 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:53 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f561dc152f6d05a1820783d780247855889a7f67c10ad93e662c845bc4e04b7`  
		Last Modified: Fri, 16 Jun 2023 04:54:22 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d354935fa931e19a8f77a6c42fc6b00ded3220c90cb42cae42e6c5037216e7`  
		Last Modified: Fri, 16 Jun 2023 05:46:13 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb1d5b1ba3df14638b59a633b5694ee365f792344599f925786528df43a66d1`  
		Last Modified: Fri, 16 Jun 2023 05:46:14 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a259fe0e346454f8edb47ada3ba73f02bbdd9cb53d855ebe10fbf8cd621cc`  
		Last Modified: Fri, 16 Jun 2023 05:46:18 GMT  
		Size: 117.4 MB (117402245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:0d63991f54111dd5559781b27e8f531f8f7a7d5ab4da95fca1b5d714a789d0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b2d4ba995bad4c208c6ad081c8e5137476c2d2bc0f92bb11d96adb46582365c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.2 MB (447190355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490c4ccf128ba0bff6cf967e5982092d7d0d655fdb30cee6a9adadcf92d4d399`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:20:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:20:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:20:51 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:21:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:21:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:21:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:21:12 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:21:12 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:21:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:21:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3dc0ed80ba8f5d1aa930e6dbe28ab57080f5180217d2f9bcd3b20dbf36b6ee`  
		Last Modified: Fri, 16 Jun 2023 05:22:57 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75bf0033d4f598982374de4ef5149898b9caa3ffc816e567f074d455863886b`  
		Last Modified: Fri, 16 Jun 2023 05:22:57 GMT  
		Size: 8.7 KB (8704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ebd40e9a33f7c07fdad223d9a71432366eb5946da04b93c217d69f02a18a25`  
		Last Modified: Fri, 16 Jun 2023 05:23:06 GMT  
		Size: 217.2 MB (217211011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74d65cf0030354d706b1734879747cf59b1469b2a16a0899ad153f7d9cac04ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.5 MB (442467317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df61f3b1ca63129fd60412f8fec17ffef83cde8f5794566863814a8076dc8a1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:42:21 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:44:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:44:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:58 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:45:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:45:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:45:09 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:45:10 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:45:10 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:45:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:45:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f561dc152f6d05a1820783d780247855889a7f67c10ad93e662c845bc4e04b7`  
		Last Modified: Fri, 16 Jun 2023 04:54:22 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ea29dfb8fca6c499b2b739d2ec72cb9862867e581ed576a15f7eaaaa7a189d`  
		Last Modified: Fri, 16 Jun 2023 05:46:30 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc4b0a3c2b7a7d795de9f657a1d2170b6fcafe73b42fccb0a6444f3b9d05712`  
		Last Modified: Fri, 16 Jun 2023 05:46:30 GMT  
		Size: 8.7 KB (8705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc147fbf25fb68d2d9fb97feb42b226dddf4440311c8cec4b122a04d4ca80d0`  
		Last Modified: Fri, 16 Jun 2023 05:46:39 GMT  
		Size: 217.1 MB (217067707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.21`

```console
$ docker pull neo4j@sha256:572153b597a340e7b8442217edb1d7525dd42ff6ba9096cadf9cbb28b14a9da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.21` - linux; amd64

```console
$ docker pull neo4j@sha256:af0b8351e10f2f66e853c6e959b54e1db780a9e19ab0860844c4769fc456385e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347524303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf473beffa6246d62d4c2569c194944c072628ba6fb73a92647faa1d868e2053`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:20:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:20:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:20:28 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:20:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:20:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:20:43 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:20:43 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:20:43 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:20:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:20:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa0a6975dfa29feaf803c94de20288cd29ca45546487f5eff385ae9655d1f45`  
		Last Modified: Fri, 16 Jun 2023 05:22:31 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3ea6e90d20daee9f17005dbb0cdd2dc10d6fc714bbf2fb166573233bda8c3`  
		Last Modified: Fri, 16 Jun 2023 05:22:31 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76b05814b2acdbff12372926c4d02f76b7c7d39192877d16cd4e9909377482`  
		Last Modified: Fri, 16 Jun 2023 05:22:38 GMT  
		Size: 117.5 MB (117544952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.21` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d61fdcd271341e03138b457b6691f86a85e370e690be995613c2f7711cba680
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342801857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aa2ad35dc11706be84886dbfc3211ccaede0b967ba53f6d320811b427adf75`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:42:21 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:44:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:44:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:44 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:44:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:53 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:53 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:53 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f561dc152f6d05a1820783d780247855889a7f67c10ad93e662c845bc4e04b7`  
		Last Modified: Fri, 16 Jun 2023 04:54:22 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d354935fa931e19a8f77a6c42fc6b00ded3220c90cb42cae42e6c5037216e7`  
		Last Modified: Fri, 16 Jun 2023 05:46:13 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb1d5b1ba3df14638b59a633b5694ee365f792344599f925786528df43a66d1`  
		Last Modified: Fri, 16 Jun 2023 05:46:14 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a259fe0e346454f8edb47ada3ba73f02bbdd9cb53d855ebe10fbf8cd621cc`  
		Last Modified: Fri, 16 Jun 2023 05:46:18 GMT  
		Size: 117.4 MB (117402245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.21-community`

```console
$ docker pull neo4j@sha256:572153b597a340e7b8442217edb1d7525dd42ff6ba9096cadf9cbb28b14a9da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.21-community` - linux; amd64

```console
$ docker pull neo4j@sha256:af0b8351e10f2f66e853c6e959b54e1db780a9e19ab0860844c4769fc456385e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347524303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf473beffa6246d62d4c2569c194944c072628ba6fb73a92647faa1d868e2053`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:20:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:20:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:20:28 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:20:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:20:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:20:43 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:20:43 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:20:43 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:20:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:20:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa0a6975dfa29feaf803c94de20288cd29ca45546487f5eff385ae9655d1f45`  
		Last Modified: Fri, 16 Jun 2023 05:22:31 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3ea6e90d20daee9f17005dbb0cdd2dc10d6fc714bbf2fb166573233bda8c3`  
		Last Modified: Fri, 16 Jun 2023 05:22:31 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76b05814b2acdbff12372926c4d02f76b7c7d39192877d16cd4e9909377482`  
		Last Modified: Fri, 16 Jun 2023 05:22:38 GMT  
		Size: 117.5 MB (117544952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.21-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d61fdcd271341e03138b457b6691f86a85e370e690be995613c2f7711cba680
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342801857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aa2ad35dc11706be84886dbfc3211ccaede0b967ba53f6d320811b427adf75`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:42:21 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:44:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:44:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:44 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:44:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:53 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:53 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:53 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f561dc152f6d05a1820783d780247855889a7f67c10ad93e662c845bc4e04b7`  
		Last Modified: Fri, 16 Jun 2023 04:54:22 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d354935fa931e19a8f77a6c42fc6b00ded3220c90cb42cae42e6c5037216e7`  
		Last Modified: Fri, 16 Jun 2023 05:46:13 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb1d5b1ba3df14638b59a633b5694ee365f792344599f925786528df43a66d1`  
		Last Modified: Fri, 16 Jun 2023 05:46:14 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a259fe0e346454f8edb47ada3ba73f02bbdd9cb53d855ebe10fbf8cd621cc`  
		Last Modified: Fri, 16 Jun 2023 05:46:18 GMT  
		Size: 117.4 MB (117402245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.21-enterprise`

```console
$ docker pull neo4j@sha256:0d63991f54111dd5559781b27e8f531f8f7a7d5ab4da95fca1b5d714a789d0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.21-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b2d4ba995bad4c208c6ad081c8e5137476c2d2bc0f92bb11d96adb46582365c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.2 MB (447190355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490c4ccf128ba0bff6cf967e5982092d7d0d655fdb30cee6a9adadcf92d4d399`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:20:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:20:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:20:51 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:21:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:21:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:21:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:21:12 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:21:12 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:21:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:21:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3dc0ed80ba8f5d1aa930e6dbe28ab57080f5180217d2f9bcd3b20dbf36b6ee`  
		Last Modified: Fri, 16 Jun 2023 05:22:57 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75bf0033d4f598982374de4ef5149898b9caa3ffc816e567f074d455863886b`  
		Last Modified: Fri, 16 Jun 2023 05:22:57 GMT  
		Size: 8.7 KB (8704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ebd40e9a33f7c07fdad223d9a71432366eb5946da04b93c217d69f02a18a25`  
		Last Modified: Fri, 16 Jun 2023 05:23:06 GMT  
		Size: 217.2 MB (217211011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.21-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74d65cf0030354d706b1734879747cf59b1469b2a16a0899ad153f7d9cac04ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.5 MB (442467317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df61f3b1ca63129fd60412f8fec17ffef83cde8f5794566863814a8076dc8a1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:42:21 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:44:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Fri, 16 Jun 2023 05:44:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:58 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 16 Jun 2023 05:45:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:45:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:45:09 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:45:10 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:45:10 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:45:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:45:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f561dc152f6d05a1820783d780247855889a7f67c10ad93e662c845bc4e04b7`  
		Last Modified: Fri, 16 Jun 2023 04:54:22 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ea29dfb8fca6c499b2b739d2ec72cb9862867e581ed576a15f7eaaaa7a189d`  
		Last Modified: Fri, 16 Jun 2023 05:46:30 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc4b0a3c2b7a7d795de9f657a1d2170b6fcafe73b42fccb0a6444f3b9d05712`  
		Last Modified: Fri, 16 Jun 2023 05:46:30 GMT  
		Size: 8.7 KB (8705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc147fbf25fb68d2d9fb97feb42b226dddf4440311c8cec4b122a04d4ca80d0`  
		Last Modified: Fri, 16 Jun 2023 05:46:39 GMT  
		Size: 217.1 MB (217067707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:ca9c939fac3c770fc0e62663f48105cd89f88b13941ceb09157f6863e773e8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
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
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
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
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fbc31ac7d10747bef7f56165f4595170f12ba52e40d806cd67337b9f7e99ceb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4931ca0b07aebfca661bb4ad50991d0bbf9edc940e77d28cda3cbed9c57e1b72`
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
# Fri, 16 Jun 2023 05:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:44:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:44:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:18 GMT
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
	-	`sha256:3078201372ce04a1f09d98d7fbdc11e3b54b763c8a699d143f56477d54398550`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90b2ac4e02fc7bbf06ab59e56a14344899b72235ef544f80af862f5b6df811a`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6483f2806be0854a918f97fb2b7cf81daf78e069a46311b4a7905734517e05d3`  
		Last Modified: Fri, 16 Jun 2023 05:45:30 GMT  
		Size: 115.6 MB (115646264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:ca9c939fac3c770fc0e62663f48105cd89f88b13941ceb09157f6863e773e8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
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
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
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
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fbc31ac7d10747bef7f56165f4595170f12ba52e40d806cd67337b9f7e99ceb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4931ca0b07aebfca661bb4ad50991d0bbf9edc940e77d28cda3cbed9c57e1b72`
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
# Fri, 16 Jun 2023 05:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:44:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:44:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:18 GMT
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
	-	`sha256:3078201372ce04a1f09d98d7fbdc11e3b54b763c8a699d143f56477d54398550`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90b2ac4e02fc7bbf06ab59e56a14344899b72235ef544f80af862f5b6df811a`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6483f2806be0854a918f97fb2b7cf81daf78e069a46311b4a7905734517e05d3`  
		Last Modified: Fri, 16 Jun 2023 05:45:30 GMT  
		Size: 115.6 MB (115646264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:be98efd9aff8d0d249a83de6e99240bbc18a4947ce9250269d418796380f5d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

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

### `neo4j:5-enterprise` - linux; arm64 variant v8

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

## `neo4j:5.9`

```console
$ docker pull neo4j@sha256:ca9c939fac3c770fc0e62663f48105cd89f88b13941ceb09157f6863e773e8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
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
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
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
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fbc31ac7d10747bef7f56165f4595170f12ba52e40d806cd67337b9f7e99ceb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4931ca0b07aebfca661bb4ad50991d0bbf9edc940e77d28cda3cbed9c57e1b72`
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
# Fri, 16 Jun 2023 05:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:44:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:44:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:18 GMT
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
	-	`sha256:3078201372ce04a1f09d98d7fbdc11e3b54b763c8a699d143f56477d54398550`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90b2ac4e02fc7bbf06ab59e56a14344899b72235ef544f80af862f5b6df811a`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6483f2806be0854a918f97fb2b7cf81daf78e069a46311b4a7905734517e05d3`  
		Last Modified: Fri, 16 Jun 2023 05:45:30 GMT  
		Size: 115.6 MB (115646264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9-community`

```console
$ docker pull neo4j@sha256:ca9c939fac3c770fc0e62663f48105cd89f88b13941ceb09157f6863e773e8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
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
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
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
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fbc31ac7d10747bef7f56165f4595170f12ba52e40d806cd67337b9f7e99ceb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4931ca0b07aebfca661bb4ad50991d0bbf9edc940e77d28cda3cbed9c57e1b72`
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
# Fri, 16 Jun 2023 05:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:44:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:44:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:18 GMT
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
	-	`sha256:3078201372ce04a1f09d98d7fbdc11e3b54b763c8a699d143f56477d54398550`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90b2ac4e02fc7bbf06ab59e56a14344899b72235ef544f80af862f5b6df811a`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6483f2806be0854a918f97fb2b7cf81daf78e069a46311b4a7905734517e05d3`  
		Last Modified: Fri, 16 Jun 2023 05:45:30 GMT  
		Size: 115.6 MB (115646264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9-enterprise`

```console
$ docker pull neo4j@sha256:be98efd9aff8d0d249a83de6e99240bbc18a4947ce9250269d418796380f5d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9-enterprise` - linux; amd64

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

### `neo4j:5.9-enterprise` - linux; arm64 variant v8

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

## `neo4j:5.9.0`

```console
$ docker pull neo4j@sha256:ca9c939fac3c770fc0e62663f48105cd89f88b13941ceb09157f6863e773e8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9.0` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
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
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
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
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fbc31ac7d10747bef7f56165f4595170f12ba52e40d806cd67337b9f7e99ceb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4931ca0b07aebfca661bb4ad50991d0bbf9edc940e77d28cda3cbed9c57e1b72`
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
# Fri, 16 Jun 2023 05:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:44:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:44:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:18 GMT
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
	-	`sha256:3078201372ce04a1f09d98d7fbdc11e3b54b763c8a699d143f56477d54398550`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90b2ac4e02fc7bbf06ab59e56a14344899b72235ef544f80af862f5b6df811a`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6483f2806be0854a918f97fb2b7cf81daf78e069a46311b4a7905734517e05d3`  
		Last Modified: Fri, 16 Jun 2023 05:45:30 GMT  
		Size: 115.6 MB (115646264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9.0-community`

```console
$ docker pull neo4j@sha256:ca9c939fac3c770fc0e62663f48105cd89f88b13941ceb09157f6863e773e8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
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
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
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
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fbc31ac7d10747bef7f56165f4595170f12ba52e40d806cd67337b9f7e99ceb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4931ca0b07aebfca661bb4ad50991d0bbf9edc940e77d28cda3cbed9c57e1b72`
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
# Fri, 16 Jun 2023 05:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:44:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:44:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:18 GMT
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
	-	`sha256:3078201372ce04a1f09d98d7fbdc11e3b54b763c8a699d143f56477d54398550`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90b2ac4e02fc7bbf06ab59e56a14344899b72235ef544f80af862f5b6df811a`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6483f2806be0854a918f97fb2b7cf81daf78e069a46311b4a7905734517e05d3`  
		Last Modified: Fri, 16 Jun 2023 05:45:30 GMT  
		Size: 115.6 MB (115646264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9.0-enterprise`

```console
$ docker pull neo4j@sha256:be98efd9aff8d0d249a83de6e99240bbc18a4947ce9250269d418796380f5d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9.0-enterprise` - linux; amd64

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

### `neo4j:5.9.0-enterprise` - linux; arm64 variant v8

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

## `neo4j:community`

```console
$ docker pull neo4j@sha256:ca9c939fac3c770fc0e62663f48105cd89f88b13941ceb09157f6863e773e8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
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
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
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
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fbc31ac7d10747bef7f56165f4595170f12ba52e40d806cd67337b9f7e99ceb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4931ca0b07aebfca661bb4ad50991d0bbf9edc940e77d28cda3cbed9c57e1b72`
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
# Fri, 16 Jun 2023 05:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:44:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:44:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:18 GMT
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
	-	`sha256:3078201372ce04a1f09d98d7fbdc11e3b54b763c8a699d143f56477d54398550`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90b2ac4e02fc7bbf06ab59e56a14344899b72235ef544f80af862f5b6df811a`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6483f2806be0854a918f97fb2b7cf81daf78e069a46311b4a7905734517e05d3`  
		Last Modified: Fri, 16 Jun 2023 05:45:30 GMT  
		Size: 115.6 MB (115646264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:ca9c939fac3c770fc0e62663f48105cd89f88b13941ceb09157f6863e773e8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
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
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
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
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fbc31ac7d10747bef7f56165f4595170f12ba52e40d806cd67337b9f7e99ceb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4931ca0b07aebfca661bb4ad50991d0bbf9edc940e77d28cda3cbed9c57e1b72`
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
# Fri, 16 Jun 2023 05:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:44:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:44:01 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:44:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:44:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:44:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:44:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:44:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:44:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:44:18 GMT
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
	-	`sha256:3078201372ce04a1f09d98d7fbdc11e3b54b763c8a699d143f56477d54398550`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90b2ac4e02fc7bbf06ab59e56a14344899b72235ef544f80af862f5b6df811a`  
		Last Modified: Fri, 16 Jun 2023 05:45:25 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6483f2806be0854a918f97fb2b7cf81daf78e069a46311b4a7905734517e05d3`  
		Last Modified: Fri, 16 Jun 2023 05:45:30 GMT  
		Size: 115.6 MB (115646264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
