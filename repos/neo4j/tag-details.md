<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.19`](#neo4j4419)
-	[`neo4j:4.4.19-community`](#neo4j4419-community)
-	[`neo4j:4.4.19-enterprise`](#neo4j4419-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.7`](#neo4j57)
-	[`neo4j:5.7-community`](#neo4j57-community)
-	[`neo4j:5.7-enterprise`](#neo4j57-enterprise)
-	[`neo4j:5.7.0`](#neo4j570)
-	[`neo4j:5.7.0-community`](#neo4j570-community)
-	[`neo4j:5.7.0-enterprise`](#neo4j570-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:885b09ffbc75f69659eb5a2e6d69f160376c02e59f6f9524abb52ba1669d3199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:23cee9a73e7421c0ae60d2e41673365a55eca428a86161beacbc00b47ccb009d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349626050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470c60e4b112ac4a0c0744a8493c2a8118d8b3703bfdd2a37b82c8cb32d5d7d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Thu, 04 May 2023 15:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Thu, 04 May 2023 15:21:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:50 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 15:22:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:22:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:22:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:22:00 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:22:00 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:22:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:22:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419348188128285663b652d2c0f3279b6ee12edd0ab96e81b83fa8ad2f38d041`  
		Last Modified: Thu, 04 May 2023 15:23:23 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816b5dbbd24f755d469dba32500f6f1db4fee3210f71633d7b12d0d892951bb2`  
		Last Modified: Thu, 04 May 2023 15:23:23 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686fb79d4ef1d8392a5102bf7d24b4e83df0d394f88d9a4e87716c98272b0abc`  
		Last Modified: Thu, 04 May 2023 15:23:29 GMT  
		Size: 119.7 MB (119660597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f785d0cdb940c0d3af0870ca1e978a96cda87b7b4ab383e90c78ad60d8a92a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344907362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34d7e3d74bf44fafe1c31aa74bcca972894e24e9894854be6561210fee47536`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Thu, 04 May 2023 12:05:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:05:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Thu, 04 May 2023 12:05:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:05:30 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 12:05:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:39 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:39 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:40 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b87eea2caf98f51733ab05c70e2390e47ba43561b4d5e64ce1f035adb4d5b`  
		Last Modified: Thu, 04 May 2023 12:06:56 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1297f0820ec77dc87fca58cb3c7d1452001027792bf525bfa87191b9540b93c`  
		Last Modified: Thu, 04 May 2023 12:06:56 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a718454e9752be9cb18bdd6adabffd967c492a2a835f258eb859c09a9708aff6`  
		Last Modified: Thu, 04 May 2023 12:07:01 GMT  
		Size: 119.5 MB (119517959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:885b09ffbc75f69659eb5a2e6d69f160376c02e59f6f9524abb52ba1669d3199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:23cee9a73e7421c0ae60d2e41673365a55eca428a86161beacbc00b47ccb009d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349626050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470c60e4b112ac4a0c0744a8493c2a8118d8b3703bfdd2a37b82c8cb32d5d7d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Thu, 04 May 2023 15:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Thu, 04 May 2023 15:21:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:50 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 15:22:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:22:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:22:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:22:00 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:22:00 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:22:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:22:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419348188128285663b652d2c0f3279b6ee12edd0ab96e81b83fa8ad2f38d041`  
		Last Modified: Thu, 04 May 2023 15:23:23 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816b5dbbd24f755d469dba32500f6f1db4fee3210f71633d7b12d0d892951bb2`  
		Last Modified: Thu, 04 May 2023 15:23:23 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686fb79d4ef1d8392a5102bf7d24b4e83df0d394f88d9a4e87716c98272b0abc`  
		Last Modified: Thu, 04 May 2023 15:23:29 GMT  
		Size: 119.7 MB (119660597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f785d0cdb940c0d3af0870ca1e978a96cda87b7b4ab383e90c78ad60d8a92a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344907362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34d7e3d74bf44fafe1c31aa74bcca972894e24e9894854be6561210fee47536`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Thu, 04 May 2023 12:05:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:05:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Thu, 04 May 2023 12:05:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:05:30 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 12:05:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:39 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:39 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:40 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b87eea2caf98f51733ab05c70e2390e47ba43561b4d5e64ce1f035adb4d5b`  
		Last Modified: Thu, 04 May 2023 12:06:56 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1297f0820ec77dc87fca58cb3c7d1452001027792bf525bfa87191b9540b93c`  
		Last Modified: Thu, 04 May 2023 12:06:56 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a718454e9752be9cb18bdd6adabffd967c492a2a835f258eb859c09a9708aff6`  
		Last Modified: Thu, 04 May 2023 12:07:01 GMT  
		Size: 119.5 MB (119517959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:dd14f33c06af694bdd25784f99ccf68456f06565868e0bc1cea891589cdbcf36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b58f6df940e05cdfadd3505feaac823f749508cc25ee70b181c2acf9f99361e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.4 MB (446393720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9214b32f60fac3e8ce8ec5b19cb09ca26a53d008bb9c675805c8e5e4fd4208`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Thu, 04 May 2023 15:22:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9ecf2706abff535c4ac9e902ca36257ab23af96be3386ea54f0ec17dcb7cf8e NEO4J_TARBALL=neo4j-enterprise-4.4.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:22:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
# Thu, 04 May 2023 15:22:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:22:04 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 15:22:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:22:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:22:17 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:22:17 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:22:17 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:22:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:22:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1a494e5bb9094f48f72d5d76b2ab9747adb25ffba906268ff6038c22b44104`  
		Last Modified: Thu, 04 May 2023 15:23:40 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d50da69828b3ab49529949f4a8c7ad0921e488571b086cb61ec95de2a8b4c`  
		Last Modified: Thu, 04 May 2023 15:23:40 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc554372fb8f615971184f20338533437a1b9fde98fa1e07cc56eec2f2bd720`  
		Last Modified: Thu, 04 May 2023 15:23:49 GMT  
		Size: 216.4 MB (216428271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:65eb92cf8d5ab246fe228d11dd3102c436ae8217847439db489ecc9291a86611
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.7 MB (441675410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4360bfabdd1eb2c0428c3a518d33db00eabdab6dfe5a0c124470923fe72302df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Thu, 04 May 2023 12:05:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9ecf2706abff535c4ac9e902ca36257ab23af96be3386ea54f0ec17dcb7cf8e NEO4J_TARBALL=neo4j-enterprise-4.4.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:05:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
# Thu, 04 May 2023 12:05:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:05:43 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 12:05:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:56 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:56 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:56 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6afc98d2829f19f6050c43e8f70813fbb02303cf8c4fa0969c7c2aa1e3978`  
		Last Modified: Thu, 04 May 2023 12:07:13 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a2a66cd05153c19d51918da9fc8e1a6790f7f43b934e51022f6a8a76fd1247`  
		Last Modified: Thu, 04 May 2023 12:07:13 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bdbb9ab3ee1ad3e4c95ec756618fd425be6f9293237d84d540b7a92154e2ea`  
		Last Modified: Thu, 04 May 2023 12:07:21 GMT  
		Size: 216.3 MB (216286011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.19`

```console
$ docker pull neo4j@sha256:885b09ffbc75f69659eb5a2e6d69f160376c02e59f6f9524abb52ba1669d3199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.19` - linux; amd64

```console
$ docker pull neo4j@sha256:23cee9a73e7421c0ae60d2e41673365a55eca428a86161beacbc00b47ccb009d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349626050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470c60e4b112ac4a0c0744a8493c2a8118d8b3703bfdd2a37b82c8cb32d5d7d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Thu, 04 May 2023 15:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Thu, 04 May 2023 15:21:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:50 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 15:22:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:22:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:22:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:22:00 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:22:00 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:22:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:22:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419348188128285663b652d2c0f3279b6ee12edd0ab96e81b83fa8ad2f38d041`  
		Last Modified: Thu, 04 May 2023 15:23:23 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816b5dbbd24f755d469dba32500f6f1db4fee3210f71633d7b12d0d892951bb2`  
		Last Modified: Thu, 04 May 2023 15:23:23 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686fb79d4ef1d8392a5102bf7d24b4e83df0d394f88d9a4e87716c98272b0abc`  
		Last Modified: Thu, 04 May 2023 15:23:29 GMT  
		Size: 119.7 MB (119660597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.19` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f785d0cdb940c0d3af0870ca1e978a96cda87b7b4ab383e90c78ad60d8a92a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344907362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34d7e3d74bf44fafe1c31aa74bcca972894e24e9894854be6561210fee47536`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Thu, 04 May 2023 12:05:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:05:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Thu, 04 May 2023 12:05:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:05:30 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 12:05:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:39 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:39 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:40 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b87eea2caf98f51733ab05c70e2390e47ba43561b4d5e64ce1f035adb4d5b`  
		Last Modified: Thu, 04 May 2023 12:06:56 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1297f0820ec77dc87fca58cb3c7d1452001027792bf525bfa87191b9540b93c`  
		Last Modified: Thu, 04 May 2023 12:06:56 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a718454e9752be9cb18bdd6adabffd967c492a2a835f258eb859c09a9708aff6`  
		Last Modified: Thu, 04 May 2023 12:07:01 GMT  
		Size: 119.5 MB (119517959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.19-community`

```console
$ docker pull neo4j@sha256:885b09ffbc75f69659eb5a2e6d69f160376c02e59f6f9524abb52ba1669d3199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.19-community` - linux; amd64

```console
$ docker pull neo4j@sha256:23cee9a73e7421c0ae60d2e41673365a55eca428a86161beacbc00b47ccb009d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349626050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470c60e4b112ac4a0c0744a8493c2a8118d8b3703bfdd2a37b82c8cb32d5d7d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Thu, 04 May 2023 15:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Thu, 04 May 2023 15:21:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:50 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 15:22:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:22:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:22:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:22:00 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:22:00 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:22:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:22:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419348188128285663b652d2c0f3279b6ee12edd0ab96e81b83fa8ad2f38d041`  
		Last Modified: Thu, 04 May 2023 15:23:23 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816b5dbbd24f755d469dba32500f6f1db4fee3210f71633d7b12d0d892951bb2`  
		Last Modified: Thu, 04 May 2023 15:23:23 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686fb79d4ef1d8392a5102bf7d24b4e83df0d394f88d9a4e87716c98272b0abc`  
		Last Modified: Thu, 04 May 2023 15:23:29 GMT  
		Size: 119.7 MB (119660597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.19-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f785d0cdb940c0d3af0870ca1e978a96cda87b7b4ab383e90c78ad60d8a92a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344907362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34d7e3d74bf44fafe1c31aa74bcca972894e24e9894854be6561210fee47536`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Thu, 04 May 2023 12:05:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:05:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Thu, 04 May 2023 12:05:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:05:30 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 12:05:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:39 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:39 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:40 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b87eea2caf98f51733ab05c70e2390e47ba43561b4d5e64ce1f035adb4d5b`  
		Last Modified: Thu, 04 May 2023 12:06:56 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1297f0820ec77dc87fca58cb3c7d1452001027792bf525bfa87191b9540b93c`  
		Last Modified: Thu, 04 May 2023 12:06:56 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a718454e9752be9cb18bdd6adabffd967c492a2a835f258eb859c09a9708aff6`  
		Last Modified: Thu, 04 May 2023 12:07:01 GMT  
		Size: 119.5 MB (119517959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.19-enterprise`

```console
$ docker pull neo4j@sha256:dd14f33c06af694bdd25784f99ccf68456f06565868e0bc1cea891589cdbcf36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.19-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b58f6df940e05cdfadd3505feaac823f749508cc25ee70b181c2acf9f99361e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.4 MB (446393720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9214b32f60fac3e8ce8ec5b19cb09ca26a53d008bb9c675805c8e5e4fd4208`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Thu, 04 May 2023 15:22:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9ecf2706abff535c4ac9e902ca36257ab23af96be3386ea54f0ec17dcb7cf8e NEO4J_TARBALL=neo4j-enterprise-4.4.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:22:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
# Thu, 04 May 2023 15:22:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:22:04 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 15:22:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:22:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:22:17 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:22:17 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:22:17 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:22:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:22:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1a494e5bb9094f48f72d5d76b2ab9747adb25ffba906268ff6038c22b44104`  
		Last Modified: Thu, 04 May 2023 15:23:40 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d50da69828b3ab49529949f4a8c7ad0921e488571b086cb61ec95de2a8b4c`  
		Last Modified: Thu, 04 May 2023 15:23:40 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc554372fb8f615971184f20338533437a1b9fde98fa1e07cc56eec2f2bd720`  
		Last Modified: Thu, 04 May 2023 15:23:49 GMT  
		Size: 216.4 MB (216428271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.19-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:65eb92cf8d5ab246fe228d11dd3102c436ae8217847439db489ecc9291a86611
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.7 MB (441675410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4360bfabdd1eb2c0428c3a518d33db00eabdab6dfe5a0c124470923fe72302df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Thu, 04 May 2023 12:05:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9ecf2706abff535c4ac9e902ca36257ab23af96be3386ea54f0ec17dcb7cf8e NEO4J_TARBALL=neo4j-enterprise-4.4.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:05:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
# Thu, 04 May 2023 12:05:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:05:43 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Thu, 04 May 2023 12:05:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:56 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:56 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:56 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6afc98d2829f19f6050c43e8f70813fbb02303cf8c4fa0969c7c2aa1e3978`  
		Last Modified: Thu, 04 May 2023 12:07:13 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a2a66cd05153c19d51918da9fc8e1a6790f7f43b934e51022f6a8a76fd1247`  
		Last Modified: Thu, 04 May 2023 12:07:13 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bdbb9ab3ee1ad3e4c95ec756618fd425be6f9293237d84d540b7a92154e2ea`  
		Last Modified: Thu, 04 May 2023 12:07:21 GMT  
		Size: 216.3 MB (216286011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:b479b35be2a92d2a6e1733be95f880e0d426807bba01ad7f59f754190db8bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:9ae58e94484dc656875403f50bdd71491cdffdd3ff0c444ad17e3f6798df21b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339670141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c085cd5b6d7e70b080914e77965b3fb19a7e74513579b83575ee980c220f7c2`
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
# Thu, 04 May 2023 15:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 15:21:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:14 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 15:21:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:21:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:21:25 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:21:25 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:21:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:21:25 GMT
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
	-	`sha256:1ee472bf81628b9d551dbeeda93e67610217cf88190ccdbb6f8b3041d2ba6aa8`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c6bab2805d41e3ba5a24b44369c8be22145520c07d310e1fbbaa658f2e49a4`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f75f5c05e0ccd7a8834357c841736baa038f5ee2aedfbf043b8ae3d39dd12`  
		Last Modified: Thu, 04 May 2023 15:22:37 GMT  
		Size: 115.7 MB (115673613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7aa4ae79e62f700964a424d6166309162ad421ea7241cdfef8782cb7b5abf210
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336981794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6c0929c126c1a2abcd1b5af1ca7420955f76624ac87ea1d5e06f14b84b271`
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
# Thu, 04 May 2023 12:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:04:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 12:04:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:04:48 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 12:05:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:01 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:01 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:02 GMT
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
	-	`sha256:c93a8328b0b62b333b941f4f72d41fbe9f1cb67c1bdfd42ef100aa881314e839`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3ce690ce0b7d3890d98ff9ccdded5c33f4227911f17a5595392105e27326e3`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b6be57bf03bc40983fbb0f78148f99a9c9fc273d643783cc2d9a6ed968b1a`  
		Last Modified: Thu, 04 May 2023 12:06:14 GMT  
		Size: 115.5 MB (115528758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:b479b35be2a92d2a6e1733be95f880e0d426807bba01ad7f59f754190db8bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9ae58e94484dc656875403f50bdd71491cdffdd3ff0c444ad17e3f6798df21b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339670141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c085cd5b6d7e70b080914e77965b3fb19a7e74513579b83575ee980c220f7c2`
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
# Thu, 04 May 2023 15:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 15:21:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:14 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 15:21:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:21:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:21:25 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:21:25 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:21:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:21:25 GMT
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
	-	`sha256:1ee472bf81628b9d551dbeeda93e67610217cf88190ccdbb6f8b3041d2ba6aa8`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c6bab2805d41e3ba5a24b44369c8be22145520c07d310e1fbbaa658f2e49a4`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f75f5c05e0ccd7a8834357c841736baa038f5ee2aedfbf043b8ae3d39dd12`  
		Last Modified: Thu, 04 May 2023 15:22:37 GMT  
		Size: 115.7 MB (115673613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7aa4ae79e62f700964a424d6166309162ad421ea7241cdfef8782cb7b5abf210
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336981794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6c0929c126c1a2abcd1b5af1ca7420955f76624ac87ea1d5e06f14b84b271`
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
# Thu, 04 May 2023 12:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:04:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 12:04:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:04:48 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 12:05:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:01 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:01 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:02 GMT
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
	-	`sha256:c93a8328b0b62b333b941f4f72d41fbe9f1cb67c1bdfd42ef100aa881314e839`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3ce690ce0b7d3890d98ff9ccdded5c33f4227911f17a5595392105e27326e3`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b6be57bf03bc40983fbb0f78148f99a9c9fc273d643783cc2d9a6ed968b1a`  
		Last Modified: Thu, 04 May 2023 12:06:14 GMT  
		Size: 115.5 MB (115528758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `neo4j:5.7`

```console
$ docker pull neo4j@sha256:b479b35be2a92d2a6e1733be95f880e0d426807bba01ad7f59f754190db8bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.7` - linux; amd64

```console
$ docker pull neo4j@sha256:9ae58e94484dc656875403f50bdd71491cdffdd3ff0c444ad17e3f6798df21b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339670141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c085cd5b6d7e70b080914e77965b3fb19a7e74513579b83575ee980c220f7c2`
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
# Thu, 04 May 2023 15:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 15:21:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:14 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 15:21:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:21:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:21:25 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:21:25 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:21:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:21:25 GMT
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
	-	`sha256:1ee472bf81628b9d551dbeeda93e67610217cf88190ccdbb6f8b3041d2ba6aa8`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c6bab2805d41e3ba5a24b44369c8be22145520c07d310e1fbbaa658f2e49a4`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f75f5c05e0ccd7a8834357c841736baa038f5ee2aedfbf043b8ae3d39dd12`  
		Last Modified: Thu, 04 May 2023 15:22:37 GMT  
		Size: 115.7 MB (115673613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.7` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7aa4ae79e62f700964a424d6166309162ad421ea7241cdfef8782cb7b5abf210
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336981794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6c0929c126c1a2abcd1b5af1ca7420955f76624ac87ea1d5e06f14b84b271`
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
# Thu, 04 May 2023 12:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:04:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 12:04:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:04:48 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 12:05:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:01 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:01 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:02 GMT
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
	-	`sha256:c93a8328b0b62b333b941f4f72d41fbe9f1cb67c1bdfd42ef100aa881314e839`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3ce690ce0b7d3890d98ff9ccdded5c33f4227911f17a5595392105e27326e3`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b6be57bf03bc40983fbb0f78148f99a9c9fc273d643783cc2d9a6ed968b1a`  
		Last Modified: Thu, 04 May 2023 12:06:14 GMT  
		Size: 115.5 MB (115528758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.7-community`

```console
$ docker pull neo4j@sha256:b479b35be2a92d2a6e1733be95f880e0d426807bba01ad7f59f754190db8bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.7-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9ae58e94484dc656875403f50bdd71491cdffdd3ff0c444ad17e3f6798df21b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339670141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c085cd5b6d7e70b080914e77965b3fb19a7e74513579b83575ee980c220f7c2`
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
# Thu, 04 May 2023 15:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 15:21:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:14 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 15:21:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:21:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:21:25 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:21:25 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:21:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:21:25 GMT
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
	-	`sha256:1ee472bf81628b9d551dbeeda93e67610217cf88190ccdbb6f8b3041d2ba6aa8`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c6bab2805d41e3ba5a24b44369c8be22145520c07d310e1fbbaa658f2e49a4`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f75f5c05e0ccd7a8834357c841736baa038f5ee2aedfbf043b8ae3d39dd12`  
		Last Modified: Thu, 04 May 2023 15:22:37 GMT  
		Size: 115.7 MB (115673613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.7-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7aa4ae79e62f700964a424d6166309162ad421ea7241cdfef8782cb7b5abf210
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336981794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6c0929c126c1a2abcd1b5af1ca7420955f76624ac87ea1d5e06f14b84b271`
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
# Thu, 04 May 2023 12:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:04:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 12:04:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:04:48 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 12:05:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:01 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:01 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:02 GMT
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
	-	`sha256:c93a8328b0b62b333b941f4f72d41fbe9f1cb67c1bdfd42ef100aa881314e839`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3ce690ce0b7d3890d98ff9ccdded5c33f4227911f17a5595392105e27326e3`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b6be57bf03bc40983fbb0f78148f99a9c9fc273d643783cc2d9a6ed968b1a`  
		Last Modified: Thu, 04 May 2023 12:06:14 GMT  
		Size: 115.5 MB (115528758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.7-enterprise`

```console
$ docker pull neo4j@sha256:57d229fe09a56fbae744d670317cb3ade55286f0c0bab7ffae10fcdd77a8a75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.7-enterprise` - linux; amd64

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

### `neo4j:5.7-enterprise` - linux; arm64 variant v8

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

## `neo4j:5.7.0`

```console
$ docker pull neo4j@sha256:b479b35be2a92d2a6e1733be95f880e0d426807bba01ad7f59f754190db8bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.7.0` - linux; amd64

```console
$ docker pull neo4j@sha256:9ae58e94484dc656875403f50bdd71491cdffdd3ff0c444ad17e3f6798df21b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339670141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c085cd5b6d7e70b080914e77965b3fb19a7e74513579b83575ee980c220f7c2`
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
# Thu, 04 May 2023 15:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 15:21:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:14 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 15:21:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:21:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:21:25 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:21:25 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:21:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:21:25 GMT
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
	-	`sha256:1ee472bf81628b9d551dbeeda93e67610217cf88190ccdbb6f8b3041d2ba6aa8`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c6bab2805d41e3ba5a24b44369c8be22145520c07d310e1fbbaa658f2e49a4`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f75f5c05e0ccd7a8834357c841736baa038f5ee2aedfbf043b8ae3d39dd12`  
		Last Modified: Thu, 04 May 2023 15:22:37 GMT  
		Size: 115.7 MB (115673613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.7.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7aa4ae79e62f700964a424d6166309162ad421ea7241cdfef8782cb7b5abf210
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336981794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6c0929c126c1a2abcd1b5af1ca7420955f76624ac87ea1d5e06f14b84b271`
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
# Thu, 04 May 2023 12:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:04:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 12:04:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:04:48 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 12:05:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:01 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:01 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:02 GMT
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
	-	`sha256:c93a8328b0b62b333b941f4f72d41fbe9f1cb67c1bdfd42ef100aa881314e839`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3ce690ce0b7d3890d98ff9ccdded5c33f4227911f17a5595392105e27326e3`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b6be57bf03bc40983fbb0f78148f99a9c9fc273d643783cc2d9a6ed968b1a`  
		Last Modified: Thu, 04 May 2023 12:06:14 GMT  
		Size: 115.5 MB (115528758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.7.0-community`

```console
$ docker pull neo4j@sha256:b479b35be2a92d2a6e1733be95f880e0d426807bba01ad7f59f754190db8bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.7.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9ae58e94484dc656875403f50bdd71491cdffdd3ff0c444ad17e3f6798df21b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339670141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c085cd5b6d7e70b080914e77965b3fb19a7e74513579b83575ee980c220f7c2`
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
# Thu, 04 May 2023 15:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 15:21:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:14 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 15:21:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:21:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:21:25 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:21:25 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:21:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:21:25 GMT
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
	-	`sha256:1ee472bf81628b9d551dbeeda93e67610217cf88190ccdbb6f8b3041d2ba6aa8`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c6bab2805d41e3ba5a24b44369c8be22145520c07d310e1fbbaa658f2e49a4`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f75f5c05e0ccd7a8834357c841736baa038f5ee2aedfbf043b8ae3d39dd12`  
		Last Modified: Thu, 04 May 2023 15:22:37 GMT  
		Size: 115.7 MB (115673613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.7.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7aa4ae79e62f700964a424d6166309162ad421ea7241cdfef8782cb7b5abf210
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336981794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6c0929c126c1a2abcd1b5af1ca7420955f76624ac87ea1d5e06f14b84b271`
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
# Thu, 04 May 2023 12:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:04:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 12:04:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:04:48 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 12:05:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:01 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:01 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:02 GMT
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
	-	`sha256:c93a8328b0b62b333b941f4f72d41fbe9f1cb67c1bdfd42ef100aa881314e839`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3ce690ce0b7d3890d98ff9ccdded5c33f4227911f17a5595392105e27326e3`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b6be57bf03bc40983fbb0f78148f99a9c9fc273d643783cc2d9a6ed968b1a`  
		Last Modified: Thu, 04 May 2023 12:06:14 GMT  
		Size: 115.5 MB (115528758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.7.0-enterprise`

```console
$ docker pull neo4j@sha256:57d229fe09a56fbae744d670317cb3ade55286f0c0bab7ffae10fcdd77a8a75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.7.0-enterprise` - linux; amd64

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

### `neo4j:5.7.0-enterprise` - linux; arm64 variant v8

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

## `neo4j:community`

```console
$ docker pull neo4j@sha256:b479b35be2a92d2a6e1733be95f880e0d426807bba01ad7f59f754190db8bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:9ae58e94484dc656875403f50bdd71491cdffdd3ff0c444ad17e3f6798df21b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339670141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c085cd5b6d7e70b080914e77965b3fb19a7e74513579b83575ee980c220f7c2`
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
# Thu, 04 May 2023 15:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 15:21:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:14 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 15:21:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:21:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:21:25 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:21:25 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:21:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:21:25 GMT
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
	-	`sha256:1ee472bf81628b9d551dbeeda93e67610217cf88190ccdbb6f8b3041d2ba6aa8`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c6bab2805d41e3ba5a24b44369c8be22145520c07d310e1fbbaa658f2e49a4`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f75f5c05e0ccd7a8834357c841736baa038f5ee2aedfbf043b8ae3d39dd12`  
		Last Modified: Thu, 04 May 2023 15:22:37 GMT  
		Size: 115.7 MB (115673613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7aa4ae79e62f700964a424d6166309162ad421ea7241cdfef8782cb7b5abf210
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336981794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6c0929c126c1a2abcd1b5af1ca7420955f76624ac87ea1d5e06f14b84b271`
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
# Thu, 04 May 2023 12:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:04:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 12:04:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:04:48 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 12:05:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:01 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:01 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:02 GMT
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
	-	`sha256:c93a8328b0b62b333b941f4f72d41fbe9f1cb67c1bdfd42ef100aa881314e839`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3ce690ce0b7d3890d98ff9ccdded5c33f4227911f17a5595392105e27326e3`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b6be57bf03bc40983fbb0f78148f99a9c9fc273d643783cc2d9a6ed968b1a`  
		Last Modified: Thu, 04 May 2023 12:06:14 GMT  
		Size: 115.5 MB (115528758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:57d229fe09a56fbae744d670317cb3ade55286f0c0bab7ffae10fcdd77a8a75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

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

### `neo4j:enterprise` - linux; arm64 variant v8

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

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:b479b35be2a92d2a6e1733be95f880e0d426807bba01ad7f59f754190db8bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:9ae58e94484dc656875403f50bdd71491cdffdd3ff0c444ad17e3f6798df21b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339670141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c085cd5b6d7e70b080914e77965b3fb19a7e74513579b83575ee980c220f7c2`
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
# Thu, 04 May 2023 15:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 15:21:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 15:21:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 15:21:14 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 15:21:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:21:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 15:21:25 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 15:21:25 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 15:21:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 15:21:25 GMT
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
	-	`sha256:1ee472bf81628b9d551dbeeda93e67610217cf88190ccdbb6f8b3041d2ba6aa8`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c6bab2805d41e3ba5a24b44369c8be22145520c07d310e1fbbaa658f2e49a4`  
		Last Modified: Thu, 04 May 2023 15:22:31 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f75f5c05e0ccd7a8834357c841736baa038f5ee2aedfbf043b8ae3d39dd12`  
		Last Modified: Thu, 04 May 2023 15:22:37 GMT  
		Size: 115.7 MB (115673613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7aa4ae79e62f700964a424d6166309162ad421ea7241cdfef8782cb7b5abf210
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336981794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6c0929c126c1a2abcd1b5af1ca7420955f76624ac87ea1d5e06f14b84b271`
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
# Thu, 04 May 2023 12:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 May 2023 12:04:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Thu, 04 May 2023 12:04:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 04 May 2023 12:04:48 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Thu, 04 May 2023 12:05:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:05:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:05:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 May 2023 12:05:01 GMT
VOLUME [/data /logs]
# Thu, 04 May 2023 12:05:01 GMT
EXPOSE 7473 7474 7687
# Thu, 04 May 2023 12:05:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 May 2023 12:05:02 GMT
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
	-	`sha256:c93a8328b0b62b333b941f4f72d41fbe9f1cb67c1bdfd42ef100aa881314e839`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3ce690ce0b7d3890d98ff9ccdded5c33f4227911f17a5595392105e27326e3`  
		Last Modified: Thu, 04 May 2023 12:06:09 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b6be57bf03bc40983fbb0f78148f99a9c9fc273d643783cc2d9a6ed968b1a`  
		Last Modified: Thu, 04 May 2023 12:06:14 GMT  
		Size: 115.5 MB (115528758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
