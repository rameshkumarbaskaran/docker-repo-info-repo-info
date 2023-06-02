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
-	[`neo4j:5.8`](#neo4j58)
-	[`neo4j:5.8-community`](#neo4j58-community)
-	[`neo4j:5.8-enterprise`](#neo4j58-enterprise)
-	[`neo4j:5.8.0`](#neo4j580)
-	[`neo4j:5.8.0-community`](#neo4j580-community)
-	[`neo4j:5.8.0-enterprise`](#neo4j580-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:ec1b72a26240baff16ad62708f142720d673d136047171a955c61ad54b97e7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:20b6f0d0a58d8594d750543a65580d2d4d155c25a3051d421782bcc1a8b88f36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347510643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaba5a05b527d2e856ff98357b27632c2d6ab5b8201285b8f7fb35e09895b2a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Wed, 24 May 2023 22:41:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 May 2023 22:41:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Wed, 24 May 2023 22:41:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 24 May 2023 22:41:42 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Wed, 24 May 2023 22:41:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:41:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 22:41:59 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 May 2023 22:41:59 GMT
VOLUME [/data /logs]
# Wed, 24 May 2023 22:41:59 GMT
EXPOSE 7473 7474 7687
# Wed, 24 May 2023 22:41:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 May 2023 22:41:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba548696136ebfdb3932d61038075a9a64e6780a26955fe651a38872acb0f7`  
		Last Modified: Wed, 24 May 2023 22:42:43 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd170bb4c60b8d0ce9ca4ba500cb0864c8623a81ed5bb3265ae15bd49c30b840`  
		Last Modified: Wed, 24 May 2023 22:42:43 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7804b912276a62123f534cf70ab78d5b564f996e7e9ee76a213df25b9741a6bd`  
		Last Modified: Wed, 24 May 2023 22:42:48 GMT  
		Size: 117.5 MB (117544967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4b37645e26dfc8aac6852a22685ae98ef638a2b562ccbb88a27e46ad71efcf1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342791699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ff0882b7e434afdf253834c48043986047cdcb1efae2c67da5675b583a5f4d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:13 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:13 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d74853288fb9d3db14568370550a2ecfed9ecea2d47eb2c8b3dc7104e543e`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0976adc224137844c0460002fcd029bd93300b5cd0ea684f85769bd1cb853`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267da01b61f5b481ce02f9ad2cfcf05186f68e008bfdc9bc7b653f183594a98`  
		Last Modified: Fri, 02 Jun 2023 01:46:44 GMT  
		Size: 117.4 MB (117402148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:ec1b72a26240baff16ad62708f142720d673d136047171a955c61ad54b97e7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:20b6f0d0a58d8594d750543a65580d2d4d155c25a3051d421782bcc1a8b88f36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347510643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaba5a05b527d2e856ff98357b27632c2d6ab5b8201285b8f7fb35e09895b2a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Wed, 24 May 2023 22:41:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 May 2023 22:41:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Wed, 24 May 2023 22:41:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 24 May 2023 22:41:42 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Wed, 24 May 2023 22:41:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:41:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 22:41:59 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 May 2023 22:41:59 GMT
VOLUME [/data /logs]
# Wed, 24 May 2023 22:41:59 GMT
EXPOSE 7473 7474 7687
# Wed, 24 May 2023 22:41:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 May 2023 22:41:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba548696136ebfdb3932d61038075a9a64e6780a26955fe651a38872acb0f7`  
		Last Modified: Wed, 24 May 2023 22:42:43 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd170bb4c60b8d0ce9ca4ba500cb0864c8623a81ed5bb3265ae15bd49c30b840`  
		Last Modified: Wed, 24 May 2023 22:42:43 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7804b912276a62123f534cf70ab78d5b564f996e7e9ee76a213df25b9741a6bd`  
		Last Modified: Wed, 24 May 2023 22:42:48 GMT  
		Size: 117.5 MB (117544967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4b37645e26dfc8aac6852a22685ae98ef638a2b562ccbb88a27e46ad71efcf1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342791699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ff0882b7e434afdf253834c48043986047cdcb1efae2c67da5675b583a5f4d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:13 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:13 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d74853288fb9d3db14568370550a2ecfed9ecea2d47eb2c8b3dc7104e543e`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0976adc224137844c0460002fcd029bd93300b5cd0ea684f85769bd1cb853`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267da01b61f5b481ce02f9ad2cfcf05186f68e008bfdc9bc7b653f183594a98`  
		Last Modified: Fri, 02 Jun 2023 01:46:44 GMT  
		Size: 117.4 MB (117402148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:7b5b654b2f44d6fee425f173e10854be7df0650ef2954f05babaef35b059a78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:cf9da4917af279535e6091bc745ee0d411ce52e24cc851242912124bcb137568
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.2 MB (447176734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddbe43efabfb5eba5c9d357342ceaff7ace5d43999944faa1a59f1aef5081d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Wed, 24 May 2023 22:42:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 24 May 2023 22:42:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Wed, 24 May 2023 22:42:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 24 May 2023 22:42:05 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Wed, 24 May 2023 22:42:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:42:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 22:42:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 May 2023 22:42:26 GMT
VOLUME [/data /logs]
# Wed, 24 May 2023 22:42:26 GMT
EXPOSE 7473 7474 7687
# Wed, 24 May 2023 22:42:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 May 2023 22:42:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64be358033d4783da255caab3d1f427fb3d2de28303aee9b7e8b80f3ad2f17e4`  
		Last Modified: Wed, 24 May 2023 22:43:00 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab3fceedd7c64038ce29d3067b2f23e5df7e93682d189f1bba4b1c3d7bb02ce`  
		Last Modified: Wed, 24 May 2023 22:43:00 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadeaddc13c08b1ab2190d645ba2c3797178204835c7da220399bed0eacfaf82`  
		Last Modified: Wed, 24 May 2023 22:43:09 GMT  
		Size: 217.2 MB (217211060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:dcc4d672b419d757c6306e5dec6183736a570538b426db2f2218d73a29fb4ea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.5 MB (442457305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff27e143becfe2604ca3962b963209ccc6245e7374343a7e4deec8da1bc5c568`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:17 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dfbd0d60b628088706570a5418eac35a21a37bac09c9c191bf016e33ddafc6`  
		Last Modified: Fri, 02 Jun 2023 01:46:56 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185a593214eaf66f24ba4304503486e7b38f41aee427196b1075c22e540533d3`  
		Last Modified: Fri, 02 Jun 2023 01:46:55 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068e7342b690ce5986d46141bf21ae24b1be0c005c3956a171848bb603ac5be`  
		Last Modified: Fri, 02 Jun 2023 01:47:03 GMT  
		Size: 217.1 MB (217067754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.21`

```console
$ docker pull neo4j@sha256:ec1b72a26240baff16ad62708f142720d673d136047171a955c61ad54b97e7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.21` - linux; amd64

```console
$ docker pull neo4j@sha256:20b6f0d0a58d8594d750543a65580d2d4d155c25a3051d421782bcc1a8b88f36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347510643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaba5a05b527d2e856ff98357b27632c2d6ab5b8201285b8f7fb35e09895b2a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Wed, 24 May 2023 22:41:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 May 2023 22:41:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Wed, 24 May 2023 22:41:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 24 May 2023 22:41:42 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Wed, 24 May 2023 22:41:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:41:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 22:41:59 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 May 2023 22:41:59 GMT
VOLUME [/data /logs]
# Wed, 24 May 2023 22:41:59 GMT
EXPOSE 7473 7474 7687
# Wed, 24 May 2023 22:41:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 May 2023 22:41:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba548696136ebfdb3932d61038075a9a64e6780a26955fe651a38872acb0f7`  
		Last Modified: Wed, 24 May 2023 22:42:43 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd170bb4c60b8d0ce9ca4ba500cb0864c8623a81ed5bb3265ae15bd49c30b840`  
		Last Modified: Wed, 24 May 2023 22:42:43 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7804b912276a62123f534cf70ab78d5b564f996e7e9ee76a213df25b9741a6bd`  
		Last Modified: Wed, 24 May 2023 22:42:48 GMT  
		Size: 117.5 MB (117544967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.21` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4b37645e26dfc8aac6852a22685ae98ef638a2b562ccbb88a27e46ad71efcf1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342791699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ff0882b7e434afdf253834c48043986047cdcb1efae2c67da5675b583a5f4d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:13 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:13 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d74853288fb9d3db14568370550a2ecfed9ecea2d47eb2c8b3dc7104e543e`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0976adc224137844c0460002fcd029bd93300b5cd0ea684f85769bd1cb853`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267da01b61f5b481ce02f9ad2cfcf05186f68e008bfdc9bc7b653f183594a98`  
		Last Modified: Fri, 02 Jun 2023 01:46:44 GMT  
		Size: 117.4 MB (117402148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.21-community`

```console
$ docker pull neo4j@sha256:ec1b72a26240baff16ad62708f142720d673d136047171a955c61ad54b97e7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.21-community` - linux; amd64

```console
$ docker pull neo4j@sha256:20b6f0d0a58d8594d750543a65580d2d4d155c25a3051d421782bcc1a8b88f36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347510643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaba5a05b527d2e856ff98357b27632c2d6ab5b8201285b8f7fb35e09895b2a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Wed, 24 May 2023 22:41:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 May 2023 22:41:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Wed, 24 May 2023 22:41:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 24 May 2023 22:41:42 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Wed, 24 May 2023 22:41:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:41:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 22:41:59 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 May 2023 22:41:59 GMT
VOLUME [/data /logs]
# Wed, 24 May 2023 22:41:59 GMT
EXPOSE 7473 7474 7687
# Wed, 24 May 2023 22:41:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 May 2023 22:41:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba548696136ebfdb3932d61038075a9a64e6780a26955fe651a38872acb0f7`  
		Last Modified: Wed, 24 May 2023 22:42:43 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd170bb4c60b8d0ce9ca4ba500cb0864c8623a81ed5bb3265ae15bd49c30b840`  
		Last Modified: Wed, 24 May 2023 22:42:43 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7804b912276a62123f534cf70ab78d5b564f996e7e9ee76a213df25b9741a6bd`  
		Last Modified: Wed, 24 May 2023 22:42:48 GMT  
		Size: 117.5 MB (117544967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.21-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4b37645e26dfc8aac6852a22685ae98ef638a2b562ccbb88a27e46ad71efcf1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342791699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ff0882b7e434afdf253834c48043986047cdcb1efae2c67da5675b583a5f4d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:13 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:13 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d74853288fb9d3db14568370550a2ecfed9ecea2d47eb2c8b3dc7104e543e`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0976adc224137844c0460002fcd029bd93300b5cd0ea684f85769bd1cb853`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267da01b61f5b481ce02f9ad2cfcf05186f68e008bfdc9bc7b653f183594a98`  
		Last Modified: Fri, 02 Jun 2023 01:46:44 GMT  
		Size: 117.4 MB (117402148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.21-enterprise`

```console
$ docker pull neo4j@sha256:7b5b654b2f44d6fee425f173e10854be7df0650ef2954f05babaef35b059a78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.21-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:cf9da4917af279535e6091bc745ee0d411ce52e24cc851242912124bcb137568
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.2 MB (447176734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddbe43efabfb5eba5c9d357342ceaff7ace5d43999944faa1a59f1aef5081d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Wed, 24 May 2023 22:42:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 24 May 2023 22:42:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Wed, 24 May 2023 22:42:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 24 May 2023 22:42:05 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Wed, 24 May 2023 22:42:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2023 22:42:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 22:42:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 May 2023 22:42:26 GMT
VOLUME [/data /logs]
# Wed, 24 May 2023 22:42:26 GMT
EXPOSE 7473 7474 7687
# Wed, 24 May 2023 22:42:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 May 2023 22:42:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64be358033d4783da255caab3d1f427fb3d2de28303aee9b7e8b80f3ad2f17e4`  
		Last Modified: Wed, 24 May 2023 22:43:00 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab3fceedd7c64038ce29d3067b2f23e5df7e93682d189f1bba4b1c3d7bb02ce`  
		Last Modified: Wed, 24 May 2023 22:43:00 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadeaddc13c08b1ab2190d645ba2c3797178204835c7da220399bed0eacfaf82`  
		Last Modified: Wed, 24 May 2023 22:43:09 GMT  
		Size: 217.2 MB (217211060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.21-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:dcc4d672b419d757c6306e5dec6183736a570538b426db2f2218d73a29fb4ea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.5 MB (442457305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff27e143becfe2604ca3962b963209ccc6245e7374343a7e4deec8da1bc5c568`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:17 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dfbd0d60b628088706570a5418eac35a21a37bac09c9c191bf016e33ddafc6`  
		Last Modified: Fri, 02 Jun 2023 01:46:56 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185a593214eaf66f24ba4304503486e7b38f41aee427196b1075c22e540533d3`  
		Last Modified: Fri, 02 Jun 2023 01:46:55 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068e7342b690ce5986d46141bf21ae24b1be0c005c3956a171848bb603ac5be`  
		Last Modified: Fri, 02 Jun 2023 01:47:03 GMT  
		Size: 217.1 MB (217067754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:c65cf103e222aece376c62fd0dd64b822fe8a7e1823befd62c9251521617b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:3fd77e59d9e06a7eecce321846f53832a76b7d1bae75a925881e7c2231efdb34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452f29a0e18f66142ce7a951e29d81204653f569ce56cdd78cd5a283798f0ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:21 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:22 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:22 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89510ac34046180f6d276611f00d911506456ea76e77a95e26c1520d73302b1`  
		Last Modified: Fri, 26 May 2023 23:04:02 GMT  
		Size: 8.8 KB (8764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb7c7da1886b79d0658640710a1ef554a326670aca43135cc5e9324ef48226`  
		Last Modified: Fri, 26 May 2023 23:04:07 GMT  
		Size: 114.7 MB (114688575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:c65cf103e222aece376c62fd0dd64b822fe8a7e1823befd62c9251521617b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3fd77e59d9e06a7eecce321846f53832a76b7d1bae75a925881e7c2231efdb34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452f29a0e18f66142ce7a951e29d81204653f569ce56cdd78cd5a283798f0ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:21 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:22 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:22 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89510ac34046180f6d276611f00d911506456ea76e77a95e26c1520d73302b1`  
		Last Modified: Fri, 26 May 2023 23:04:02 GMT  
		Size: 8.8 KB (8764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb7c7da1886b79d0658640710a1ef554a326670aca43135cc5e9324ef48226`  
		Last Modified: Fri, 26 May 2023 23:04:07 GMT  
		Size: 114.7 MB (114688575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:aa51a5c1e061c674f9c669ccb2fa162b8ae2b9c8a5974196be4d48831b154d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6660790a01e1e082b3be44ddf5787fb96d6bd2a7f147cd657296b1cd607a4677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a3841dea59ca9bc3979802d57aa57006353aea78c027b79dd3a8236b811944`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:27 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:44 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:44 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:44 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5011326b12928bcd6584016f6aea605e8a53b9a1d6ac9a647ce032b78f52fad`  
		Last Modified: Tue, 23 May 2023 04:20:50 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10b27eebe8bc8cd2ce03c7e8d5e4f7b605fa070eebb65ee877ad3d57c02cd0d`  
		Last Modified: Fri, 26 May 2023 23:04:28 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a93766d9299b80cc1ffea6a15bb21669c17960df5dd6e3772b0f1e8aa1e6207`  
		Last Modified: Fri, 26 May 2023 23:04:42 GMT  
		Size: 379.7 MB (379683026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cee38c97292f52ea37daabbecb008f2b4c49f428f95ea9f38caf94427362dd2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2121f2b76488aa36e163ff2bc0bcdf65a5a73a08d6ed8510bf4eac9c3237358`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:40 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:57 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:57 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:58 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac10763bf8b8833986f70a55f383df991114bfbe6839f9904f06468f0d0f80a8`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009719f6debaabbf1870471b661a8390e01b458827a6114d1027064a867d80`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183826f6c0789438a8b134ed5bd2d1249d148c71659c553e53bfc0a0c96db33d`  
		Last Modified: Fri, 02 Jun 2023 01:46:27 GMT  
		Size: 379.5 MB (379541395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8`

```console
$ docker pull neo4j@sha256:c65cf103e222aece376c62fd0dd64b822fe8a7e1823befd62c9251521617b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8` - linux; amd64

```console
$ docker pull neo4j@sha256:3fd77e59d9e06a7eecce321846f53832a76b7d1bae75a925881e7c2231efdb34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452f29a0e18f66142ce7a951e29d81204653f569ce56cdd78cd5a283798f0ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:21 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:22 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:22 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89510ac34046180f6d276611f00d911506456ea76e77a95e26c1520d73302b1`  
		Last Modified: Fri, 26 May 2023 23:04:02 GMT  
		Size: 8.8 KB (8764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb7c7da1886b79d0658640710a1ef554a326670aca43135cc5e9324ef48226`  
		Last Modified: Fri, 26 May 2023 23:04:07 GMT  
		Size: 114.7 MB (114688575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8-community`

```console
$ docker pull neo4j@sha256:c65cf103e222aece376c62fd0dd64b822fe8a7e1823befd62c9251521617b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3fd77e59d9e06a7eecce321846f53832a76b7d1bae75a925881e7c2231efdb34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452f29a0e18f66142ce7a951e29d81204653f569ce56cdd78cd5a283798f0ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:21 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:22 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:22 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89510ac34046180f6d276611f00d911506456ea76e77a95e26c1520d73302b1`  
		Last Modified: Fri, 26 May 2023 23:04:02 GMT  
		Size: 8.8 KB (8764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb7c7da1886b79d0658640710a1ef554a326670aca43135cc5e9324ef48226`  
		Last Modified: Fri, 26 May 2023 23:04:07 GMT  
		Size: 114.7 MB (114688575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8-enterprise`

```console
$ docker pull neo4j@sha256:aa51a5c1e061c674f9c669ccb2fa162b8ae2b9c8a5974196be4d48831b154d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6660790a01e1e082b3be44ddf5787fb96d6bd2a7f147cd657296b1cd607a4677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a3841dea59ca9bc3979802d57aa57006353aea78c027b79dd3a8236b811944`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:27 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:44 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:44 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:44 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5011326b12928bcd6584016f6aea605e8a53b9a1d6ac9a647ce032b78f52fad`  
		Last Modified: Tue, 23 May 2023 04:20:50 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10b27eebe8bc8cd2ce03c7e8d5e4f7b605fa070eebb65ee877ad3d57c02cd0d`  
		Last Modified: Fri, 26 May 2023 23:04:28 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a93766d9299b80cc1ffea6a15bb21669c17960df5dd6e3772b0f1e8aa1e6207`  
		Last Modified: Fri, 26 May 2023 23:04:42 GMT  
		Size: 379.7 MB (379683026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cee38c97292f52ea37daabbecb008f2b4c49f428f95ea9f38caf94427362dd2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2121f2b76488aa36e163ff2bc0bcdf65a5a73a08d6ed8510bf4eac9c3237358`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:40 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:57 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:57 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:58 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac10763bf8b8833986f70a55f383df991114bfbe6839f9904f06468f0d0f80a8`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009719f6debaabbf1870471b661a8390e01b458827a6114d1027064a867d80`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183826f6c0789438a8b134ed5bd2d1249d148c71659c553e53bfc0a0c96db33d`  
		Last Modified: Fri, 02 Jun 2023 01:46:27 GMT  
		Size: 379.5 MB (379541395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0`

```console
$ docker pull neo4j@sha256:c65cf103e222aece376c62fd0dd64b822fe8a7e1823befd62c9251521617b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0` - linux; amd64

```console
$ docker pull neo4j@sha256:3fd77e59d9e06a7eecce321846f53832a76b7d1bae75a925881e7c2231efdb34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452f29a0e18f66142ce7a951e29d81204653f569ce56cdd78cd5a283798f0ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:21 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:22 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:22 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89510ac34046180f6d276611f00d911506456ea76e77a95e26c1520d73302b1`  
		Last Modified: Fri, 26 May 2023 23:04:02 GMT  
		Size: 8.8 KB (8764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb7c7da1886b79d0658640710a1ef554a326670aca43135cc5e9324ef48226`  
		Last Modified: Fri, 26 May 2023 23:04:07 GMT  
		Size: 114.7 MB (114688575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0-community`

```console
$ docker pull neo4j@sha256:c65cf103e222aece376c62fd0dd64b822fe8a7e1823befd62c9251521617b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3fd77e59d9e06a7eecce321846f53832a76b7d1bae75a925881e7c2231efdb34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452f29a0e18f66142ce7a951e29d81204653f569ce56cdd78cd5a283798f0ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:21 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:22 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:22 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89510ac34046180f6d276611f00d911506456ea76e77a95e26c1520d73302b1`  
		Last Modified: Fri, 26 May 2023 23:04:02 GMT  
		Size: 8.8 KB (8764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb7c7da1886b79d0658640710a1ef554a326670aca43135cc5e9324ef48226`  
		Last Modified: Fri, 26 May 2023 23:04:07 GMT  
		Size: 114.7 MB (114688575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0-enterprise`

```console
$ docker pull neo4j@sha256:aa51a5c1e061c674f9c669ccb2fa162b8ae2b9c8a5974196be4d48831b154d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6660790a01e1e082b3be44ddf5787fb96d6bd2a7f147cd657296b1cd607a4677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a3841dea59ca9bc3979802d57aa57006353aea78c027b79dd3a8236b811944`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:27 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:44 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:44 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:44 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5011326b12928bcd6584016f6aea605e8a53b9a1d6ac9a647ce032b78f52fad`  
		Last Modified: Tue, 23 May 2023 04:20:50 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10b27eebe8bc8cd2ce03c7e8d5e4f7b605fa070eebb65ee877ad3d57c02cd0d`  
		Last Modified: Fri, 26 May 2023 23:04:28 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a93766d9299b80cc1ffea6a15bb21669c17960df5dd6e3772b0f1e8aa1e6207`  
		Last Modified: Fri, 26 May 2023 23:04:42 GMT  
		Size: 379.7 MB (379683026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cee38c97292f52ea37daabbecb008f2b4c49f428f95ea9f38caf94427362dd2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2121f2b76488aa36e163ff2bc0bcdf65a5a73a08d6ed8510bf4eac9c3237358`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:40 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:57 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:57 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:58 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac10763bf8b8833986f70a55f383df991114bfbe6839f9904f06468f0d0f80a8`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009719f6debaabbf1870471b661a8390e01b458827a6114d1027064a867d80`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183826f6c0789438a8b134ed5bd2d1249d148c71659c553e53bfc0a0c96db33d`  
		Last Modified: Fri, 02 Jun 2023 01:46:27 GMT  
		Size: 379.5 MB (379541395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:c65cf103e222aece376c62fd0dd64b822fe8a7e1823befd62c9251521617b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:3fd77e59d9e06a7eecce321846f53832a76b7d1bae75a925881e7c2231efdb34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452f29a0e18f66142ce7a951e29d81204653f569ce56cdd78cd5a283798f0ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:21 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:22 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:22 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89510ac34046180f6d276611f00d911506456ea76e77a95e26c1520d73302b1`  
		Last Modified: Fri, 26 May 2023 23:04:02 GMT  
		Size: 8.8 KB (8764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb7c7da1886b79d0658640710a1ef554a326670aca43135cc5e9324ef48226`  
		Last Modified: Fri, 26 May 2023 23:04:07 GMT  
		Size: 114.7 MB (114688575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:aa51a5c1e061c674f9c669ccb2fa162b8ae2b9c8a5974196be4d48831b154d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6660790a01e1e082b3be44ddf5787fb96d6bd2a7f147cd657296b1cd607a4677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a3841dea59ca9bc3979802d57aa57006353aea78c027b79dd3a8236b811944`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:27 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:44 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:44 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:44 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5011326b12928bcd6584016f6aea605e8a53b9a1d6ac9a647ce032b78f52fad`  
		Last Modified: Tue, 23 May 2023 04:20:50 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10b27eebe8bc8cd2ce03c7e8d5e4f7b605fa070eebb65ee877ad3d57c02cd0d`  
		Last Modified: Fri, 26 May 2023 23:04:28 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a93766d9299b80cc1ffea6a15bb21669c17960df5dd6e3772b0f1e8aa1e6207`  
		Last Modified: Fri, 26 May 2023 23:04:42 GMT  
		Size: 379.7 MB (379683026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cee38c97292f52ea37daabbecb008f2b4c49f428f95ea9f38caf94427362dd2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2121f2b76488aa36e163ff2bc0bcdf65a5a73a08d6ed8510bf4eac9c3237358`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:40 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:57 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:57 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:58 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac10763bf8b8833986f70a55f383df991114bfbe6839f9904f06468f0d0f80a8`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009719f6debaabbf1870471b661a8390e01b458827a6114d1027064a867d80`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183826f6c0789438a8b134ed5bd2d1249d148c71659c553e53bfc0a0c96db33d`  
		Last Modified: Fri, 02 Jun 2023 01:46:27 GMT  
		Size: 379.5 MB (379541395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:c65cf103e222aece376c62fd0dd64b822fe8a7e1823befd62c9251521617b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:3fd77e59d9e06a7eecce321846f53832a76b7d1bae75a925881e7c2231efdb34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452f29a0e18f66142ce7a951e29d81204653f569ce56cdd78cd5a283798f0ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 26 May 2023 23:03:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 26 May 2023 23:03:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 26 May 2023 23:03:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 May 2023 23:03:21 GMT
WORKDIR /var/lib/neo4j
# Fri, 26 May 2023 23:03:22 GMT
VOLUME [/data /logs]
# Fri, 26 May 2023 23:03:22 GMT
EXPOSE 7473 7474 7687
# Fri, 26 May 2023 23:03:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 26 May 2023 23:03:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89510ac34046180f6d276611f00d911506456ea76e77a95e26c1520d73302b1`  
		Last Modified: Fri, 26 May 2023 23:04:02 GMT  
		Size: 8.8 KB (8764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb7c7da1886b79d0658640710a1ef554a326670aca43135cc5e9324ef48226`  
		Last Modified: Fri, 26 May 2023 23:04:07 GMT  
		Size: 114.7 MB (114688575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
