<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.26`](#neo4j4426)
-	[`neo4j:4.4.26-community`](#neo4j4426-community)
-	[`neo4j:4.4.26-enterprise`](#neo4j4426-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.13`](#neo4j513)
-	[`neo4j:5.13-bullseye`](#neo4j513-bullseye)
-	[`neo4j:5.13-community`](#neo4j513-community)
-	[`neo4j:5.13-community-bullseye`](#neo4j513-community-bullseye)
-	[`neo4j:5.13-community-ubi8`](#neo4j513-community-ubi8)
-	[`neo4j:5.13-enterprise`](#neo4j513-enterprise)
-	[`neo4j:5.13-enterprise-bullseye`](#neo4j513-enterprise-bullseye)
-	[`neo4j:5.13-enterprise-ubi8`](#neo4j513-enterprise-ubi8)
-	[`neo4j:5.13-ubi8`](#neo4j513-ubi8)
-	[`neo4j:5.13.0`](#neo4j5130)
-	[`neo4j:5.13.0-bullseye`](#neo4j5130-bullseye)
-	[`neo4j:5.13.0-community`](#neo4j5130-community)
-	[`neo4j:5.13.0-community-bullseye`](#neo4j5130-community-bullseye)
-	[`neo4j:5.13.0-community-ubi8`](#neo4j5130-community-ubi8)
-	[`neo4j:5.13.0-enterprise`](#neo4j5130-enterprise)
-	[`neo4j:5.13.0-enterprise-bullseye`](#neo4j5130-enterprise-bullseye)
-	[`neo4j:5.13.0-enterprise-ubi8`](#neo4j5130-enterprise-ubi8)
-	[`neo4j:5.13.0-ubi8`](#neo4j5130-ubi8)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi8`](#neo4jcommunity-ubi8)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi8`](#neo4jenterprise-ubi8)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi8`](#neo4jubi8)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:4a39363e00e9d0d50b6dc007d055a3478b4ee10de2d226cb18b02d32d35ed67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:feaad7079ddee4352f5e01910f2eabec7406443824aaf901d56a6e6478e7634c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299042263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1a18b1ec7905f1272671d5fbec951af9948b5c9c79044dec0e5be43b2c7d72`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:44:34 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:10:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:10:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:10:22 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:10:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:10:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:34 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:34 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:34 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d89b17d02bb9e5579de05867f933086bcfc34a57e222c6f42c9296ba7309dd9`  
		Last Modified: Tue, 31 Oct 2023 01:07:48 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7110efc03247deb4131c788a6944fa11e9795c94f5e87fa2801ac6178455f7`  
		Last Modified: Tue, 31 Oct 2023 03:13:46 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb49211512d9dcd0314d89bb594edadc830bd51e8a9ee451e0028f0ec42d20b2`  
		Last Modified: Tue, 31 Oct 2023 03:13:46 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8995977898580c62038d127178382e7e71762584a17f396b37354db6423248d6`  
		Last Modified: Tue, 31 Oct 2023 03:13:52 GMT  
		Size: 122.3 MB (122344563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1bbe9d2d21f8a73c2865760d911239d4e087d52988a98349084d5f5e6523858
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294314597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de24c709dba0bfd6378bd21fe0fbd3848a6c8976a55de74f45c860db09af911`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:58:29 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:55:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:55:56 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:56:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:56:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:56:06 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:56:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:56:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:56:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:56:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1574a555514b1c133c3be600625ef18feb9a4fe8cac6b809f10df06a43b9ed`  
		Last Modified: Tue, 31 Oct 2023 01:18:17 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342e344e2135bcc4898aaabfa5b64ee14a672dcf8ea9f5e813b7366e805a9ca`  
		Last Modified: Tue, 31 Oct 2023 03:59:00 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6de0b35d239e34a39d1789c6d90151821c5b6f8fc5e75a42dd42912709b257`  
		Last Modified: Tue, 31 Oct 2023 03:59:00 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15ba4d0122ed19f29d8b13036453e6a4609c4de8c4cf05ce841464b16d02960`  
		Last Modified: Tue, 31 Oct 2023 03:59:07 GMT  
		Size: 122.2 MB (122235377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:4a39363e00e9d0d50b6dc007d055a3478b4ee10de2d226cb18b02d32d35ed67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:feaad7079ddee4352f5e01910f2eabec7406443824aaf901d56a6e6478e7634c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299042263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1a18b1ec7905f1272671d5fbec951af9948b5c9c79044dec0e5be43b2c7d72`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:44:34 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:10:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:10:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:10:22 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:10:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:10:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:34 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:34 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:34 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d89b17d02bb9e5579de05867f933086bcfc34a57e222c6f42c9296ba7309dd9`  
		Last Modified: Tue, 31 Oct 2023 01:07:48 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7110efc03247deb4131c788a6944fa11e9795c94f5e87fa2801ac6178455f7`  
		Last Modified: Tue, 31 Oct 2023 03:13:46 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb49211512d9dcd0314d89bb594edadc830bd51e8a9ee451e0028f0ec42d20b2`  
		Last Modified: Tue, 31 Oct 2023 03:13:46 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8995977898580c62038d127178382e7e71762584a17f396b37354db6423248d6`  
		Last Modified: Tue, 31 Oct 2023 03:13:52 GMT  
		Size: 122.3 MB (122344563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1bbe9d2d21f8a73c2865760d911239d4e087d52988a98349084d5f5e6523858
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294314597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de24c709dba0bfd6378bd21fe0fbd3848a6c8976a55de74f45c860db09af911`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:58:29 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:55:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:55:56 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:56:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:56:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:56:06 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:56:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:56:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:56:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:56:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1574a555514b1c133c3be600625ef18feb9a4fe8cac6b809f10df06a43b9ed`  
		Last Modified: Tue, 31 Oct 2023 01:18:17 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342e344e2135bcc4898aaabfa5b64ee14a672dcf8ea9f5e813b7366e805a9ca`  
		Last Modified: Tue, 31 Oct 2023 03:59:00 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6de0b35d239e34a39d1789c6d90151821c5b6f8fc5e75a42dd42912709b257`  
		Last Modified: Tue, 31 Oct 2023 03:59:00 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15ba4d0122ed19f29d8b13036453e6a4609c4de8c4cf05ce841464b16d02960`  
		Last Modified: Tue, 31 Oct 2023 03:59:07 GMT  
		Size: 122.2 MB (122235377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:b304ce805c57b859bc0694659c3edc2d1f23722261bd0c9392f7d2a73c271381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d26ef2880fd5616147b38e4aae700bef4058ce270d6cab6eb6c330b9699a614e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 MB (405731727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71593cda6218df5f30da5d917bf6c6048c4fb3c4fe043f3974b46e3a4bb31925`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:44:34 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:10:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5059157293dee431cd78ad350b077792a481526b3994f5f043529d7145005914 NEO4J_TARBALL=neo4j-enterprise-4.4.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:10:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:10:39 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:10:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:10:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:54 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:54 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d89b17d02bb9e5579de05867f933086bcfc34a57e222c6f42c9296ba7309dd9`  
		Last Modified: Tue, 31 Oct 2023 01:07:48 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d7e44686b148935237faf51c76919f946734a5a0e171ac8766a3e2e94345c`  
		Last Modified: Tue, 31 Oct 2023 03:14:06 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdaad29b663cff3890606955e89ed3c09f13e6a1a79b76e55e327e03ec390e2`  
		Last Modified: Tue, 31 Oct 2023 03:14:06 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa248dba3334b54c67f92049b8b52563bbc4d97cc9b69c4e36facaa6de2af047`  
		Last Modified: Tue, 31 Oct 2023 03:14:18 GMT  
		Size: 229.0 MB (229034025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6489e20b0683d0178e730444457fc2b782dc285515dd0a34ed5c41f54b4c1e57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.0 MB (401007147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050eeb054ff0c84c4210124ff819cd4362e05e34c71fc777fc7cbc0908f10569`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:58:29 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:56:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5059157293dee431cd78ad350b077792a481526b3994f5f043529d7145005914 NEO4J_TARBALL=neo4j-enterprise-4.4.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:56:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:56:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:56:09 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:56:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:56:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:56:22 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:56:22 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:56:22 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:56:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:56:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1574a555514b1c133c3be600625ef18feb9a4fe8cac6b809f10df06a43b9ed`  
		Last Modified: Tue, 31 Oct 2023 01:18:17 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228587ed37569c1e297435442f080e58359b006e558e9da95f6d5d45a2da430c`  
		Last Modified: Tue, 31 Oct 2023 03:59:19 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c465047f7a2b5e757357c45bb25d0367c32889c3b6169dfefdcc612171016f21`  
		Last Modified: Tue, 31 Oct 2023 03:59:19 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d8abef50d81020edbe341750aac21ce70f2b696ad0e87b52418b7e4b2b6116`  
		Last Modified: Tue, 31 Oct 2023 03:59:28 GMT  
		Size: 228.9 MB (228927924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.26`

```console
$ docker pull neo4j@sha256:4a39363e00e9d0d50b6dc007d055a3478b4ee10de2d226cb18b02d32d35ed67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.26` - linux; amd64

```console
$ docker pull neo4j@sha256:feaad7079ddee4352f5e01910f2eabec7406443824aaf901d56a6e6478e7634c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299042263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1a18b1ec7905f1272671d5fbec951af9948b5c9c79044dec0e5be43b2c7d72`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:44:34 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:10:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:10:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:10:22 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:10:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:10:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:34 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:34 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:34 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d89b17d02bb9e5579de05867f933086bcfc34a57e222c6f42c9296ba7309dd9`  
		Last Modified: Tue, 31 Oct 2023 01:07:48 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7110efc03247deb4131c788a6944fa11e9795c94f5e87fa2801ac6178455f7`  
		Last Modified: Tue, 31 Oct 2023 03:13:46 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb49211512d9dcd0314d89bb594edadc830bd51e8a9ee451e0028f0ec42d20b2`  
		Last Modified: Tue, 31 Oct 2023 03:13:46 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8995977898580c62038d127178382e7e71762584a17f396b37354db6423248d6`  
		Last Modified: Tue, 31 Oct 2023 03:13:52 GMT  
		Size: 122.3 MB (122344563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.26` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1bbe9d2d21f8a73c2865760d911239d4e087d52988a98349084d5f5e6523858
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294314597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de24c709dba0bfd6378bd21fe0fbd3848a6c8976a55de74f45c860db09af911`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:58:29 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:55:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:55:56 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:56:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:56:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:56:06 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:56:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:56:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:56:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:56:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1574a555514b1c133c3be600625ef18feb9a4fe8cac6b809f10df06a43b9ed`  
		Last Modified: Tue, 31 Oct 2023 01:18:17 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342e344e2135bcc4898aaabfa5b64ee14a672dcf8ea9f5e813b7366e805a9ca`  
		Last Modified: Tue, 31 Oct 2023 03:59:00 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6de0b35d239e34a39d1789c6d90151821c5b6f8fc5e75a42dd42912709b257`  
		Last Modified: Tue, 31 Oct 2023 03:59:00 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15ba4d0122ed19f29d8b13036453e6a4609c4de8c4cf05ce841464b16d02960`  
		Last Modified: Tue, 31 Oct 2023 03:59:07 GMT  
		Size: 122.2 MB (122235377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.26-community`

```console
$ docker pull neo4j@sha256:4a39363e00e9d0d50b6dc007d055a3478b4ee10de2d226cb18b02d32d35ed67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.26-community` - linux; amd64

```console
$ docker pull neo4j@sha256:feaad7079ddee4352f5e01910f2eabec7406443824aaf901d56a6e6478e7634c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299042263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1a18b1ec7905f1272671d5fbec951af9948b5c9c79044dec0e5be43b2c7d72`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:44:34 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:10:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:10:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:10:22 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:10:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:10:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:34 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:34 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:34 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d89b17d02bb9e5579de05867f933086bcfc34a57e222c6f42c9296ba7309dd9`  
		Last Modified: Tue, 31 Oct 2023 01:07:48 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7110efc03247deb4131c788a6944fa11e9795c94f5e87fa2801ac6178455f7`  
		Last Modified: Tue, 31 Oct 2023 03:13:46 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb49211512d9dcd0314d89bb594edadc830bd51e8a9ee451e0028f0ec42d20b2`  
		Last Modified: Tue, 31 Oct 2023 03:13:46 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8995977898580c62038d127178382e7e71762584a17f396b37354db6423248d6`  
		Last Modified: Tue, 31 Oct 2023 03:13:52 GMT  
		Size: 122.3 MB (122344563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.26-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1bbe9d2d21f8a73c2865760d911239d4e087d52988a98349084d5f5e6523858
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294314597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de24c709dba0bfd6378bd21fe0fbd3848a6c8976a55de74f45c860db09af911`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:58:29 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:55:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:55:56 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:56:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:56:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:56:06 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:56:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:56:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:56:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:56:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1574a555514b1c133c3be600625ef18feb9a4fe8cac6b809f10df06a43b9ed`  
		Last Modified: Tue, 31 Oct 2023 01:18:17 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342e344e2135bcc4898aaabfa5b64ee14a672dcf8ea9f5e813b7366e805a9ca`  
		Last Modified: Tue, 31 Oct 2023 03:59:00 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6de0b35d239e34a39d1789c6d90151821c5b6f8fc5e75a42dd42912709b257`  
		Last Modified: Tue, 31 Oct 2023 03:59:00 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15ba4d0122ed19f29d8b13036453e6a4609c4de8c4cf05ce841464b16d02960`  
		Last Modified: Tue, 31 Oct 2023 03:59:07 GMT  
		Size: 122.2 MB (122235377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.26-enterprise`

```console
$ docker pull neo4j@sha256:b304ce805c57b859bc0694659c3edc2d1f23722261bd0c9392f7d2a73c271381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.26-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d26ef2880fd5616147b38e4aae700bef4058ce270d6cab6eb6c330b9699a614e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 MB (405731727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71593cda6218df5f30da5d917bf6c6048c4fb3c4fe043f3974b46e3a4bb31925`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:44:34 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:10:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5059157293dee431cd78ad350b077792a481526b3994f5f043529d7145005914 NEO4J_TARBALL=neo4j-enterprise-4.4.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:10:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:10:39 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:10:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:10:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:54 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:54 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d89b17d02bb9e5579de05867f933086bcfc34a57e222c6f42c9296ba7309dd9`  
		Last Modified: Tue, 31 Oct 2023 01:07:48 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d7e44686b148935237faf51c76919f946734a5a0e171ac8766a3e2e94345c`  
		Last Modified: Tue, 31 Oct 2023 03:14:06 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdaad29b663cff3890606955e89ed3c09f13e6a1a79b76e55e327e03ec390e2`  
		Last Modified: Tue, 31 Oct 2023 03:14:06 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa248dba3334b54c67f92049b8b52563bbc4d97cc9b69c4e36facaa6de2af047`  
		Last Modified: Tue, 31 Oct 2023 03:14:18 GMT  
		Size: 229.0 MB (229034025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.26-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6489e20b0683d0178e730444457fc2b782dc285515dd0a34ed5c41f54b4c1e57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.0 MB (401007147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050eeb054ff0c84c4210124ff819cd4362e05e34c71fc777fc7cbc0908f10569`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:58:29 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:56:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5059157293dee431cd78ad350b077792a481526b3994f5f043529d7145005914 NEO4J_TARBALL=neo4j-enterprise-4.4.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:56:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
# Tue, 31 Oct 2023 03:56:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:56:09 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Tue, 31 Oct 2023 03:56:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:56:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:56:22 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:56:22 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:56:22 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:56:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:56:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1574a555514b1c133c3be600625ef18feb9a4fe8cac6b809f10df06a43b9ed`  
		Last Modified: Tue, 31 Oct 2023 01:18:17 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228587ed37569c1e297435442f080e58359b006e558e9da95f6d5d45a2da430c`  
		Last Modified: Tue, 31 Oct 2023 03:59:19 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c465047f7a2b5e757357c45bb25d0367c32889c3b6169dfefdcc612171016f21`  
		Last Modified: Tue, 31 Oct 2023 03:59:19 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d8abef50d81020edbe341750aac21ce70f2b696ad0e87b52418b7e4b2b6116`  
		Last Modified: Tue, 31 Oct 2023 03:59:28 GMT  
		Size: 228.9 MB (228927924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:cada68dcf9da0d3c9834a302fe09b7c40e594674eee89b81457efa9e0183424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7f529f9b883e7508d4d1a47443425886646969b67110faca226ecd6e3d7db0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303285075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0876e68b678eab976554606ae27aabd58cc4db13da7af5ec730f198d334d1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:58 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:02 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:03 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc8bfe48d470191a4f525a0d0a2b2d2df8cf58b607493f4fe27287d41a7e8a`  
		Last Modified: Tue, 31 Oct 2023 03:12:42 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f61cdc434df46bf9943e942b815c6121c056d9a469e1d1ff9b88d8c8ac6b080`  
		Last Modified: Tue, 31 Oct 2023 03:12:49 GMT  
		Size: 112.6 MB (112571528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e852f99034810f3853e7fbd42ccb0207c3cfc7ea9a1cbc9458f169446970d2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e56eb5ed513792f1a3c4c10172712d2e63f8c1737aa35adea5df8ed058dbe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:33 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:37 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:37 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4cf921619b8aac5f90d22a4751c47aee713ce6ccc841fd7091823360a9953`  
		Last Modified: Tue, 31 Oct 2023 03:58:03 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c30cb8efdf63af7a59c1dc194fc2f186fe59528309cacb4525b7ca4b18ea5`  
		Last Modified: Tue, 31 Oct 2023 03:58:08 GMT  
		Size: 112.6 MB (112571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:35c52292ec27c3941af1880f26e290416d9b785f8f825c88d01f67570dcba653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:62936367ed505f6765327f032edf5649fb06f4917bd62070b9fc43e4b1b7b492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d74a8c87c0f9a8d132d97fc735a709ec957f155ded65a6d1a54866aa956548`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:09:13 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:42 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:42 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc00dbc7af82a77fe12a3507eb1040e25ed6e988a29b5a80fc80f194a9fa01`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351db915d11ed606393043dbc9d3c5ed13334a147f8bb002433937f3037f5597`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b777d0f507083d0781390ce9c58bb98c6787acf7e564e9dbcfe0155c71f6ec`  
		Last Modified: Tue, 31 Oct 2023 03:12:22 GMT  
		Size: 387.8 MB (387788650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cec1c1dd661339776919cb113065a2a4b95f2b5c6db6bfc3e06447188eaf512e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f6e69b89dfa1ec3a2cda5a0e40fb196766c34213096dba80a37902c3d1b62f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:55:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68619d9958b93e93d5f977966ee4da3fc270f45ddbceef9844fb4a5d7477d98a`  
		Last Modified: Tue, 31 Oct 2023 03:57:27 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0fc3d1d5c65a349135f68daa643bf7cbcc3cabfb0c765a0a735036a1fd58fa`  
		Last Modified: Tue, 31 Oct 2023 03:57:28 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45fe7f10b172a3e850dceba2c2648bda38b2d9fbf366fbadc85063c90cfc1d4`  
		Last Modified: Tue, 31 Oct 2023 03:57:41 GMT  
		Size: 387.7 MB (387680001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:35c52292ec27c3941af1880f26e290416d9b785f8f825c88d01f67570dcba653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:62936367ed505f6765327f032edf5649fb06f4917bd62070b9fc43e4b1b7b492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d74a8c87c0f9a8d132d97fc735a709ec957f155ded65a6d1a54866aa956548`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:09:13 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:42 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:42 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc00dbc7af82a77fe12a3507eb1040e25ed6e988a29b5a80fc80f194a9fa01`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351db915d11ed606393043dbc9d3c5ed13334a147f8bb002433937f3037f5597`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b777d0f507083d0781390ce9c58bb98c6787acf7e564e9dbcfe0155c71f6ec`  
		Last Modified: Tue, 31 Oct 2023 03:12:22 GMT  
		Size: 387.8 MB (387788650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cec1c1dd661339776919cb113065a2a4b95f2b5c6db6bfc3e06447188eaf512e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f6e69b89dfa1ec3a2cda5a0e40fb196766c34213096dba80a37902c3d1b62f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:55:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68619d9958b93e93d5f977966ee4da3fc270f45ddbceef9844fb4a5d7477d98a`  
		Last Modified: Tue, 31 Oct 2023 03:57:27 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0fc3d1d5c65a349135f68daa643bf7cbcc3cabfb0c765a0a735036a1fd58fa`  
		Last Modified: Tue, 31 Oct 2023 03:57:28 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45fe7f10b172a3e850dceba2c2648bda38b2d9fbf366fbadc85063c90cfc1d4`  
		Last Modified: Tue, 31 Oct 2023 03:57:41 GMT  
		Size: 387.7 MB (387680001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:fbf58db74d5fb993cd188808ae3a966f0119c4eefce3295fff49abc51fec549d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a613d5196615fb0090ada8c126151e663bcf6bea31edf2a83570949d49352059
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574691704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f814c463a4165096f3b6f1fa1836fa16bc3f13ec33011a9d49ecef17805155`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:10:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:10:07 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:17 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:17 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:18 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9719156c8861c63c0f3d35884d03cdbfac1b86e31fff24c5c94c7c0baba3c`  
		Last Modified: Tue, 31 Oct 2023 03:13:15 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b5411e7bd3bb3e8f212dc4a7abbd40cc839cfe7e6a4d0e179570c3ae9f11f8`  
		Last Modified: Tue, 31 Oct 2023 03:13:33 GMT  
		Size: 384.0 MB (383978163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cbf81ff37755b9cb2196cfe822cb0671bc97bd69bb3cbfff84ad1114cdde5301
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.9 MB (571875278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433d59458c2f432f8c0153903d7ff89b6367a36b3088dd0e23fde154581c1bb9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:51 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:51 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:51 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9270bb2ee329178be9827cb8f5438ef26e8f5a4a6a5f87bfa19cf97b258ebf64`  
		Last Modified: Tue, 31 Oct 2023 03:58:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1ebb2e92c7a0041a3eb8cf0052ed6c07948d47d0e86a3b4d99d799e7d9df2`  
		Last Modified: Tue, 31 Oct 2023 03:58:48 GMT  
		Size: 384.0 MB (383978199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:cada68dcf9da0d3c9834a302fe09b7c40e594674eee89b81457efa9e0183424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7f529f9b883e7508d4d1a47443425886646969b67110faca226ecd6e3d7db0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303285075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0876e68b678eab976554606ae27aabd58cc4db13da7af5ec730f198d334d1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:58 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:02 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:03 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc8bfe48d470191a4f525a0d0a2b2d2df8cf58b607493f4fe27287d41a7e8a`  
		Last Modified: Tue, 31 Oct 2023 03:12:42 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f61cdc434df46bf9943e942b815c6121c056d9a469e1d1ff9b88d8c8ac6b080`  
		Last Modified: Tue, 31 Oct 2023 03:12:49 GMT  
		Size: 112.6 MB (112571528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e852f99034810f3853e7fbd42ccb0207c3cfc7ea9a1cbc9458f169446970d2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e56eb5ed513792f1a3c4c10172712d2e63f8c1737aa35adea5df8ed058dbe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:33 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:37 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:37 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4cf921619b8aac5f90d22a4751c47aee713ce6ccc841fd7091823360a9953`  
		Last Modified: Tue, 31 Oct 2023 03:58:03 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c30cb8efdf63af7a59c1dc194fc2f186fe59528309cacb4525b7ca4b18ea5`  
		Last Modified: Tue, 31 Oct 2023 03:58:08 GMT  
		Size: 112.6 MB (112571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-bullseye`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-community`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-community-bullseye`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-community-ubi8`

```console
$ docker pull neo4j@sha256:cada68dcf9da0d3c9834a302fe09b7c40e594674eee89b81457efa9e0183424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7f529f9b883e7508d4d1a47443425886646969b67110faca226ecd6e3d7db0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303285075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0876e68b678eab976554606ae27aabd58cc4db13da7af5ec730f198d334d1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:58 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:02 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:03 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc8bfe48d470191a4f525a0d0a2b2d2df8cf58b607493f4fe27287d41a7e8a`  
		Last Modified: Tue, 31 Oct 2023 03:12:42 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f61cdc434df46bf9943e942b815c6121c056d9a469e1d1ff9b88d8c8ac6b080`  
		Last Modified: Tue, 31 Oct 2023 03:12:49 GMT  
		Size: 112.6 MB (112571528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e852f99034810f3853e7fbd42ccb0207c3cfc7ea9a1cbc9458f169446970d2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e56eb5ed513792f1a3c4c10172712d2e63f8c1737aa35adea5df8ed058dbe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:33 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:37 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:37 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4cf921619b8aac5f90d22a4751c47aee713ce6ccc841fd7091823360a9953`  
		Last Modified: Tue, 31 Oct 2023 03:58:03 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c30cb8efdf63af7a59c1dc194fc2f186fe59528309cacb4525b7ca4b18ea5`  
		Last Modified: Tue, 31 Oct 2023 03:58:08 GMT  
		Size: 112.6 MB (112571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-enterprise`

```console
$ docker pull neo4j@sha256:35c52292ec27c3941af1880f26e290416d9b785f8f825c88d01f67570dcba653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:62936367ed505f6765327f032edf5649fb06f4917bd62070b9fc43e4b1b7b492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d74a8c87c0f9a8d132d97fc735a709ec957f155ded65a6d1a54866aa956548`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:09:13 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:42 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:42 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc00dbc7af82a77fe12a3507eb1040e25ed6e988a29b5a80fc80f194a9fa01`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351db915d11ed606393043dbc9d3c5ed13334a147f8bb002433937f3037f5597`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b777d0f507083d0781390ce9c58bb98c6787acf7e564e9dbcfe0155c71f6ec`  
		Last Modified: Tue, 31 Oct 2023 03:12:22 GMT  
		Size: 387.8 MB (387788650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cec1c1dd661339776919cb113065a2a4b95f2b5c6db6bfc3e06447188eaf512e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f6e69b89dfa1ec3a2cda5a0e40fb196766c34213096dba80a37902c3d1b62f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:55:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68619d9958b93e93d5f977966ee4da3fc270f45ddbceef9844fb4a5d7477d98a`  
		Last Modified: Tue, 31 Oct 2023 03:57:27 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0fc3d1d5c65a349135f68daa643bf7cbcc3cabfb0c765a0a735036a1fd58fa`  
		Last Modified: Tue, 31 Oct 2023 03:57:28 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45fe7f10b172a3e850dceba2c2648bda38b2d9fbf366fbadc85063c90cfc1d4`  
		Last Modified: Tue, 31 Oct 2023 03:57:41 GMT  
		Size: 387.7 MB (387680001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:35c52292ec27c3941af1880f26e290416d9b785f8f825c88d01f67570dcba653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:62936367ed505f6765327f032edf5649fb06f4917bd62070b9fc43e4b1b7b492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d74a8c87c0f9a8d132d97fc735a709ec957f155ded65a6d1a54866aa956548`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:09:13 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:42 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:42 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc00dbc7af82a77fe12a3507eb1040e25ed6e988a29b5a80fc80f194a9fa01`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351db915d11ed606393043dbc9d3c5ed13334a147f8bb002433937f3037f5597`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b777d0f507083d0781390ce9c58bb98c6787acf7e564e9dbcfe0155c71f6ec`  
		Last Modified: Tue, 31 Oct 2023 03:12:22 GMT  
		Size: 387.8 MB (387788650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cec1c1dd661339776919cb113065a2a4b95f2b5c6db6bfc3e06447188eaf512e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f6e69b89dfa1ec3a2cda5a0e40fb196766c34213096dba80a37902c3d1b62f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:55:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68619d9958b93e93d5f977966ee4da3fc270f45ddbceef9844fb4a5d7477d98a`  
		Last Modified: Tue, 31 Oct 2023 03:57:27 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0fc3d1d5c65a349135f68daa643bf7cbcc3cabfb0c765a0a735036a1fd58fa`  
		Last Modified: Tue, 31 Oct 2023 03:57:28 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45fe7f10b172a3e850dceba2c2648bda38b2d9fbf366fbadc85063c90cfc1d4`  
		Last Modified: Tue, 31 Oct 2023 03:57:41 GMT  
		Size: 387.7 MB (387680001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:fbf58db74d5fb993cd188808ae3a966f0119c4eefce3295fff49abc51fec549d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a613d5196615fb0090ada8c126151e663bcf6bea31edf2a83570949d49352059
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574691704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f814c463a4165096f3b6f1fa1836fa16bc3f13ec33011a9d49ecef17805155`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:10:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:10:07 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:17 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:17 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:18 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9719156c8861c63c0f3d35884d03cdbfac1b86e31fff24c5c94c7c0baba3c`  
		Last Modified: Tue, 31 Oct 2023 03:13:15 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b5411e7bd3bb3e8f212dc4a7abbd40cc839cfe7e6a4d0e179570c3ae9f11f8`  
		Last Modified: Tue, 31 Oct 2023 03:13:33 GMT  
		Size: 384.0 MB (383978163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cbf81ff37755b9cb2196cfe822cb0671bc97bd69bb3cbfff84ad1114cdde5301
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.9 MB (571875278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433d59458c2f432f8c0153903d7ff89b6367a36b3088dd0e23fde154581c1bb9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:51 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:51 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:51 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9270bb2ee329178be9827cb8f5438ef26e8f5a4a6a5f87bfa19cf97b258ebf64`  
		Last Modified: Tue, 31 Oct 2023 03:58:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1ebb2e92c7a0041a3eb8cf0052ed6c07948d47d0e86a3b4d99d799e7d9df2`  
		Last Modified: Tue, 31 Oct 2023 03:58:48 GMT  
		Size: 384.0 MB (383978199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-ubi8`

```console
$ docker pull neo4j@sha256:cada68dcf9da0d3c9834a302fe09b7c40e594674eee89b81457efa9e0183424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7f529f9b883e7508d4d1a47443425886646969b67110faca226ecd6e3d7db0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303285075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0876e68b678eab976554606ae27aabd58cc4db13da7af5ec730f198d334d1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:58 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:02 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:03 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc8bfe48d470191a4f525a0d0a2b2d2df8cf58b607493f4fe27287d41a7e8a`  
		Last Modified: Tue, 31 Oct 2023 03:12:42 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f61cdc434df46bf9943e942b815c6121c056d9a469e1d1ff9b88d8c8ac6b080`  
		Last Modified: Tue, 31 Oct 2023 03:12:49 GMT  
		Size: 112.6 MB (112571528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e852f99034810f3853e7fbd42ccb0207c3cfc7ea9a1cbc9458f169446970d2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e56eb5ed513792f1a3c4c10172712d2e63f8c1737aa35adea5df8ed058dbe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:33 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:37 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:37 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4cf921619b8aac5f90d22a4751c47aee713ce6ccc841fd7091823360a9953`  
		Last Modified: Tue, 31 Oct 2023 03:58:03 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c30cb8efdf63af7a59c1dc194fc2f186fe59528309cacb4525b7ca4b18ea5`  
		Last Modified: Tue, 31 Oct 2023 03:58:08 GMT  
		Size: 112.6 MB (112571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-bullseye`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-community`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-community-bullseye`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-community-ubi8`

```console
$ docker pull neo4j@sha256:cada68dcf9da0d3c9834a302fe09b7c40e594674eee89b81457efa9e0183424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7f529f9b883e7508d4d1a47443425886646969b67110faca226ecd6e3d7db0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303285075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0876e68b678eab976554606ae27aabd58cc4db13da7af5ec730f198d334d1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:58 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:02 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:03 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc8bfe48d470191a4f525a0d0a2b2d2df8cf58b607493f4fe27287d41a7e8a`  
		Last Modified: Tue, 31 Oct 2023 03:12:42 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f61cdc434df46bf9943e942b815c6121c056d9a469e1d1ff9b88d8c8ac6b080`  
		Last Modified: Tue, 31 Oct 2023 03:12:49 GMT  
		Size: 112.6 MB (112571528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e852f99034810f3853e7fbd42ccb0207c3cfc7ea9a1cbc9458f169446970d2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e56eb5ed513792f1a3c4c10172712d2e63f8c1737aa35adea5df8ed058dbe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:33 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:37 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:37 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4cf921619b8aac5f90d22a4751c47aee713ce6ccc841fd7091823360a9953`  
		Last Modified: Tue, 31 Oct 2023 03:58:03 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c30cb8efdf63af7a59c1dc194fc2f186fe59528309cacb4525b7ca4b18ea5`  
		Last Modified: Tue, 31 Oct 2023 03:58:08 GMT  
		Size: 112.6 MB (112571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-enterprise`

```console
$ docker pull neo4j@sha256:35c52292ec27c3941af1880f26e290416d9b785f8f825c88d01f67570dcba653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:62936367ed505f6765327f032edf5649fb06f4917bd62070b9fc43e4b1b7b492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d74a8c87c0f9a8d132d97fc735a709ec957f155ded65a6d1a54866aa956548`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:09:13 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:42 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:42 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc00dbc7af82a77fe12a3507eb1040e25ed6e988a29b5a80fc80f194a9fa01`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351db915d11ed606393043dbc9d3c5ed13334a147f8bb002433937f3037f5597`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b777d0f507083d0781390ce9c58bb98c6787acf7e564e9dbcfe0155c71f6ec`  
		Last Modified: Tue, 31 Oct 2023 03:12:22 GMT  
		Size: 387.8 MB (387788650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cec1c1dd661339776919cb113065a2a4b95f2b5c6db6bfc3e06447188eaf512e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f6e69b89dfa1ec3a2cda5a0e40fb196766c34213096dba80a37902c3d1b62f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:55:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68619d9958b93e93d5f977966ee4da3fc270f45ddbceef9844fb4a5d7477d98a`  
		Last Modified: Tue, 31 Oct 2023 03:57:27 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0fc3d1d5c65a349135f68daa643bf7cbcc3cabfb0c765a0a735036a1fd58fa`  
		Last Modified: Tue, 31 Oct 2023 03:57:28 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45fe7f10b172a3e850dceba2c2648bda38b2d9fbf366fbadc85063c90cfc1d4`  
		Last Modified: Tue, 31 Oct 2023 03:57:41 GMT  
		Size: 387.7 MB (387680001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:35c52292ec27c3941af1880f26e290416d9b785f8f825c88d01f67570dcba653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:62936367ed505f6765327f032edf5649fb06f4917bd62070b9fc43e4b1b7b492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d74a8c87c0f9a8d132d97fc735a709ec957f155ded65a6d1a54866aa956548`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:09:13 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:42 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:42 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc00dbc7af82a77fe12a3507eb1040e25ed6e988a29b5a80fc80f194a9fa01`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351db915d11ed606393043dbc9d3c5ed13334a147f8bb002433937f3037f5597`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b777d0f507083d0781390ce9c58bb98c6787acf7e564e9dbcfe0155c71f6ec`  
		Last Modified: Tue, 31 Oct 2023 03:12:22 GMT  
		Size: 387.8 MB (387788650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cec1c1dd661339776919cb113065a2a4b95f2b5c6db6bfc3e06447188eaf512e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f6e69b89dfa1ec3a2cda5a0e40fb196766c34213096dba80a37902c3d1b62f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:55:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68619d9958b93e93d5f977966ee4da3fc270f45ddbceef9844fb4a5d7477d98a`  
		Last Modified: Tue, 31 Oct 2023 03:57:27 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0fc3d1d5c65a349135f68daa643bf7cbcc3cabfb0c765a0a735036a1fd58fa`  
		Last Modified: Tue, 31 Oct 2023 03:57:28 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45fe7f10b172a3e850dceba2c2648bda38b2d9fbf366fbadc85063c90cfc1d4`  
		Last Modified: Tue, 31 Oct 2023 03:57:41 GMT  
		Size: 387.7 MB (387680001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:fbf58db74d5fb993cd188808ae3a966f0119c4eefce3295fff49abc51fec549d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a613d5196615fb0090ada8c126151e663bcf6bea31edf2a83570949d49352059
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574691704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f814c463a4165096f3b6f1fa1836fa16bc3f13ec33011a9d49ecef17805155`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:10:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:10:07 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:17 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:17 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:18 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9719156c8861c63c0f3d35884d03cdbfac1b86e31fff24c5c94c7c0baba3c`  
		Last Modified: Tue, 31 Oct 2023 03:13:15 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b5411e7bd3bb3e8f212dc4a7abbd40cc839cfe7e6a4d0e179570c3ae9f11f8`  
		Last Modified: Tue, 31 Oct 2023 03:13:33 GMT  
		Size: 384.0 MB (383978163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cbf81ff37755b9cb2196cfe822cb0671bc97bd69bb3cbfff84ad1114cdde5301
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.9 MB (571875278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433d59458c2f432f8c0153903d7ff89b6367a36b3088dd0e23fde154581c1bb9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:51 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:51 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:51 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9270bb2ee329178be9827cb8f5438ef26e8f5a4a6a5f87bfa19cf97b258ebf64`  
		Last Modified: Tue, 31 Oct 2023 03:58:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1ebb2e92c7a0041a3eb8cf0052ed6c07948d47d0e86a3b4d99d799e7d9df2`  
		Last Modified: Tue, 31 Oct 2023 03:58:48 GMT  
		Size: 384.0 MB (383978199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-ubi8`

```console
$ docker pull neo4j@sha256:cada68dcf9da0d3c9834a302fe09b7c40e594674eee89b81457efa9e0183424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7f529f9b883e7508d4d1a47443425886646969b67110faca226ecd6e3d7db0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303285075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0876e68b678eab976554606ae27aabd58cc4db13da7af5ec730f198d334d1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:58 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:02 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:03 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc8bfe48d470191a4f525a0d0a2b2d2df8cf58b607493f4fe27287d41a7e8a`  
		Last Modified: Tue, 31 Oct 2023 03:12:42 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f61cdc434df46bf9943e942b815c6121c056d9a469e1d1ff9b88d8c8ac6b080`  
		Last Modified: Tue, 31 Oct 2023 03:12:49 GMT  
		Size: 112.6 MB (112571528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e852f99034810f3853e7fbd42ccb0207c3cfc7ea9a1cbc9458f169446970d2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e56eb5ed513792f1a3c4c10172712d2e63f8c1737aa35adea5df8ed058dbe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:33 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:37 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:37 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4cf921619b8aac5f90d22a4751c47aee713ce6ccc841fd7091823360a9953`  
		Last Modified: Tue, 31 Oct 2023 03:58:03 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c30cb8efdf63af7a59c1dc194fc2f186fe59528309cacb4525b7ca4b18ea5`  
		Last Modified: Tue, 31 Oct 2023 03:58:08 GMT  
		Size: 112.6 MB (112571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:cada68dcf9da0d3c9834a302fe09b7c40e594674eee89b81457efa9e0183424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7f529f9b883e7508d4d1a47443425886646969b67110faca226ecd6e3d7db0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303285075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0876e68b678eab976554606ae27aabd58cc4db13da7af5ec730f198d334d1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:58 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:02 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:03 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc8bfe48d470191a4f525a0d0a2b2d2df8cf58b607493f4fe27287d41a7e8a`  
		Last Modified: Tue, 31 Oct 2023 03:12:42 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f61cdc434df46bf9943e942b815c6121c056d9a469e1d1ff9b88d8c8ac6b080`  
		Last Modified: Tue, 31 Oct 2023 03:12:49 GMT  
		Size: 112.6 MB (112571528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e852f99034810f3853e7fbd42ccb0207c3cfc7ea9a1cbc9458f169446970d2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e56eb5ed513792f1a3c4c10172712d2e63f8c1737aa35adea5df8ed058dbe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:33 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:37 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:37 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4cf921619b8aac5f90d22a4751c47aee713ce6ccc841fd7091823360a9953`  
		Last Modified: Tue, 31 Oct 2023 03:58:03 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c30cb8efdf63af7a59c1dc194fc2f186fe59528309cacb4525b7ca4b18ea5`  
		Last Modified: Tue, 31 Oct 2023 03:58:08 GMT  
		Size: 112.6 MB (112571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:35c52292ec27c3941af1880f26e290416d9b785f8f825c88d01f67570dcba653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:62936367ed505f6765327f032edf5649fb06f4917bd62070b9fc43e4b1b7b492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d74a8c87c0f9a8d132d97fc735a709ec957f155ded65a6d1a54866aa956548`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:09:13 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:42 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:42 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc00dbc7af82a77fe12a3507eb1040e25ed6e988a29b5a80fc80f194a9fa01`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351db915d11ed606393043dbc9d3c5ed13334a147f8bb002433937f3037f5597`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b777d0f507083d0781390ce9c58bb98c6787acf7e564e9dbcfe0155c71f6ec`  
		Last Modified: Tue, 31 Oct 2023 03:12:22 GMT  
		Size: 387.8 MB (387788650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cec1c1dd661339776919cb113065a2a4b95f2b5c6db6bfc3e06447188eaf512e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f6e69b89dfa1ec3a2cda5a0e40fb196766c34213096dba80a37902c3d1b62f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:55:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68619d9958b93e93d5f977966ee4da3fc270f45ddbceef9844fb4a5d7477d98a`  
		Last Modified: Tue, 31 Oct 2023 03:57:27 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0fc3d1d5c65a349135f68daa643bf7cbcc3cabfb0c765a0a735036a1fd58fa`  
		Last Modified: Tue, 31 Oct 2023 03:57:28 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45fe7f10b172a3e850dceba2c2648bda38b2d9fbf366fbadc85063c90cfc1d4`  
		Last Modified: Tue, 31 Oct 2023 03:57:41 GMT  
		Size: 387.7 MB (387680001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:35c52292ec27c3941af1880f26e290416d9b785f8f825c88d01f67570dcba653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:62936367ed505f6765327f032edf5649fb06f4917bd62070b9fc43e4b1b7b492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d74a8c87c0f9a8d132d97fc735a709ec957f155ded65a6d1a54866aa956548`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:09:13 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:42 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:42 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc00dbc7af82a77fe12a3507eb1040e25ed6e988a29b5a80fc80f194a9fa01`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351db915d11ed606393043dbc9d3c5ed13334a147f8bb002433937f3037f5597`  
		Last Modified: Tue, 31 Oct 2023 03:12:04 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b777d0f507083d0781390ce9c58bb98c6787acf7e564e9dbcfe0155c71f6ec`  
		Last Modified: Tue, 31 Oct 2023 03:12:22 GMT  
		Size: 387.8 MB (387788650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cec1c1dd661339776919cb113065a2a4b95f2b5c6db6bfc3e06447188eaf512e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f6e69b89dfa1ec3a2cda5a0e40fb196766c34213096dba80a37902c3d1b62f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:55:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:06 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68619d9958b93e93d5f977966ee4da3fc270f45ddbceef9844fb4a5d7477d98a`  
		Last Modified: Tue, 31 Oct 2023 03:57:27 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0fc3d1d5c65a349135f68daa643bf7cbcc3cabfb0c765a0a735036a1fd58fa`  
		Last Modified: Tue, 31 Oct 2023 03:57:28 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45fe7f10b172a3e850dceba2c2648bda38b2d9fbf366fbadc85063c90cfc1d4`  
		Last Modified: Tue, 31 Oct 2023 03:57:41 GMT  
		Size: 387.7 MB (387680001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:fbf58db74d5fb993cd188808ae3a966f0119c4eefce3295fff49abc51fec549d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a613d5196615fb0090ada8c126151e663bcf6bea31edf2a83570949d49352059
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574691704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f814c463a4165096f3b6f1fa1836fa16bc3f13ec33011a9d49ecef17805155`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:10:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:10:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:10:07 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:17 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:17 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:18 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9719156c8861c63c0f3d35884d03cdbfac1b86e31fff24c5c94c7c0baba3c`  
		Last Modified: Tue, 31 Oct 2023 03:13:15 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b5411e7bd3bb3e8f212dc4a7abbd40cc839cfe7e6a4d0e179570c3ae9f11f8`  
		Last Modified: Tue, 31 Oct 2023 03:13:33 GMT  
		Size: 384.0 MB (383978163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cbf81ff37755b9cb2196cfe822cb0671bc97bd69bb3cbfff84ad1114cdde5301
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.9 MB (571875278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433d59458c2f432f8c0153903d7ff89b6367a36b3088dd0e23fde154581c1bb9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:51 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:51 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:51 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9270bb2ee329178be9827cb8f5438ef26e8f5a4a6a5f87bfa19cf97b258ebf64`  
		Last Modified: Tue, 31 Oct 2023 03:58:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1ebb2e92c7a0041a3eb8cf0052ed6c07948d47d0e86a3b4d99d799e7d9df2`  
		Last Modified: Tue, 31 Oct 2023 03:58:48 GMT  
		Size: 384.0 MB (383978199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:a41a24815b24614ce7a5b90e88bf3eaf805671d9bbecab0c63b212ba7512542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:a6598d270082477c7d175d5a8f55627979600bb01490363fb9a1d05f781b5879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa4298bbaf95264701cab2f5369a08de53626d316d1e549ca74abf108a5350`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:46 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:08:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:08:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:08:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:09:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:09:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:09:05 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:09:06 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72499bec9571df5cb3ce7a10136ddb85ab01039855a43f2508008801023e27f`  
		Last Modified: Tue, 31 Oct 2023 01:13:13 GMT  
		Size: 144.9 MB (144873985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15996f185c3a038eb1130b7961393ee5a6f7208f5730d42b767cc5e184803e71`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41321735b175e6a1d0adddbb25d79e589cc76a71a423458a6683b5858d86d2ae`  
		Last Modified: Tue, 31 Oct 2023 03:11:22 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3397d94c5909fcd1a494226e018e64fc4a4a9ef5b805afca661e82792015eb09`  
		Last Modified: Tue, 31 Oct 2023 03:11:28 GMT  
		Size: 116.4 MB (116381818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bce776803960935d2f7576209274d8e7432978f778199dbf5420e3397b1af940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b916634f00c34bcfa899515456288a8b2328157832bd5b151970b9cc31c09f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:35 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:54:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:54:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:54:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 31 Oct 2023 03:54:32 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:54:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:54:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:54:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:54:44 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:54:44 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:54:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:54:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4583de8d1521212ce513b072cfa351e0ebdf445da8d233b8cf23c98fd894c9`  
		Last Modified: Tue, 31 Oct 2023 01:23:17 GMT  
		Size: 143.7 MB (143681740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568cd1b97e7b6b339d207cd1142a5c12bc84513b4306873ab1921a0b89eb9986`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 3.9 KB (3899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b7cb6dfddfb02151c5585f3984b4ed78639bae3484308d87b0263326cd69cb`  
		Last Modified: Tue, 31 Oct 2023 03:56:48 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c945b7fe70750dd9b20abafe7b15c1fa9b965ead74a523fa59a97754d2114a99`  
		Last Modified: Tue, 31 Oct 2023 03:56:54 GMT  
		Size: 116.3 MB (116275119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:cada68dcf9da0d3c9834a302fe09b7c40e594674eee89b81457efa9e0183424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7f529f9b883e7508d4d1a47443425886646969b67110faca226ecd6e3d7db0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303285075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0876e68b678eab976554606ae27aabd58cc4db13da7af5ec730f198d334d1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:58 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:02 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:03 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc8bfe48d470191a4f525a0d0a2b2d2df8cf58b607493f4fe27287d41a7e8a`  
		Last Modified: Tue, 31 Oct 2023 03:12:42 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f61cdc434df46bf9943e942b815c6121c056d9a469e1d1ff9b88d8c8ac6b080`  
		Last Modified: Tue, 31 Oct 2023 03:12:49 GMT  
		Size: 112.6 MB (112571528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e852f99034810f3853e7fbd42ccb0207c3cfc7ea9a1cbc9458f169446970d2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e56eb5ed513792f1a3c4c10172712d2e63f8c1737aa35adea5df8ed058dbe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:33 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:37 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:37 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4cf921619b8aac5f90d22a4751c47aee713ce6ccc841fd7091823360a9953`  
		Last Modified: Tue, 31 Oct 2023 03:58:03 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c30cb8efdf63af7a59c1dc194fc2f186fe59528309cacb4525b7ca4b18ea5`  
		Last Modified: Tue, 31 Oct 2023 03:58:08 GMT  
		Size: 112.6 MB (112571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
