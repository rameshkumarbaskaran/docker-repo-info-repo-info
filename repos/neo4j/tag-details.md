<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.28`](#neo4j4428)
-	[`neo4j:4.4.28-community`](#neo4j4428-community)
-	[`neo4j:4.4.28-enterprise`](#neo4j4428-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.14`](#neo4j514)
-	[`neo4j:5.14-bullseye`](#neo4j514-bullseye)
-	[`neo4j:5.14-community`](#neo4j514-community)
-	[`neo4j:5.14-community-bullseye`](#neo4j514-community-bullseye)
-	[`neo4j:5.14-community-ubi8`](#neo4j514-community-ubi8)
-	[`neo4j:5.14-enterprise`](#neo4j514-enterprise)
-	[`neo4j:5.14-enterprise-bullseye`](#neo4j514-enterprise-bullseye)
-	[`neo4j:5.14-enterprise-ubi8`](#neo4j514-enterprise-ubi8)
-	[`neo4j:5.14-ubi8`](#neo4j514-ubi8)
-	[`neo4j:5.14.0`](#neo4j5140)
-	[`neo4j:5.14.0-bullseye`](#neo4j5140-bullseye)
-	[`neo4j:5.14.0-community`](#neo4j5140-community)
-	[`neo4j:5.14.0-community-bullseye`](#neo4j5140-community-bullseye)
-	[`neo4j:5.14.0-community-ubi8`](#neo4j5140-community-ubi8)
-	[`neo4j:5.14.0-enterprise`](#neo4j5140-enterprise)
-	[`neo4j:5.14.0-enterprise-bullseye`](#neo4j5140-enterprise-bullseye)
-	[`neo4j:5.14.0-enterprise-ubi8`](#neo4j5140-enterprise-ubi8)
-	[`neo4j:5.14.0-ubi8`](#neo4j5140-ubi8)
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
$ docker pull neo4j@sha256:a80b48cb5cc8f60aa717eb22751a8570fad769c7812f9b42a84e3ade093b311b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:d460d328ce154268676eac9f671da96cb2352e65217a215ca58afabaa330ac3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297351980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d8d377e848aeaf61958658f94c584274c82d99e22a6dd99651be5ba96e6f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f00e23cf063836a6c39fe0baef42f7ade86d7a096548dcccb4620aa0e1a2a6a NEO4J_TARBALL=neo4j-community-4.4.28-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
# Wed, 29 Nov 2023 00:31:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:31:41 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 29 Nov 2023 00:32:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:32:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:32:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:32:08 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:32:08 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:32:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:32:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518dd9fa6f2e8b1dbe8b4179346513a40f007497640d3d3106e6c651e777e11e`  
		Last Modified: Wed, 29 Nov 2023 00:35:30 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed149c654f4ca8a095fbbc727edd786187d056a73e8e8dfd88f82c519af176b`  
		Last Modified: Wed, 29 Nov 2023 00:35:30 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080af8d4c72615dd5f5edc839623ec396d175a10b9af4e4fd62fc44d9e3186fb`  
		Last Modified: Wed, 29 Nov 2023 00:35:36 GMT  
		Size: 120.7 MB (120654200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3fc0d95b6fa0f32545cadaf2dc0a52fc5baa7318c4357b66f6e66b31ca3882e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292699848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1bc02b5d9b735494549b8f9bdd8a1eb2443ecfebf53028da53ec660808e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f00e23cf063836a6c39fe0baef42f7ade86d7a096548dcccb4620aa0e1a2a6a NEO4J_TARBALL=neo4j-community-4.4.28-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
# Tue, 28 Nov 2023 23:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:49:17 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Tue, 28 Nov 2023 23:49:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:49:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:49:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:49:44 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:49:44 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:49:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:49:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eae852627a07f974b52e0963f98ded118af4d207155168b1e9cf6ec98f95e6f`  
		Last Modified: Tue, 28 Nov 2023 23:53:17 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc14782865530c96cbf6d5cb32a314f61f3922dbb2ec36e38952f51fb6dce12`  
		Last Modified: Tue, 28 Nov 2023 23:53:17 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260a28fb8cdd92c92d1c3da5af70432fcb49e1967dd8077fb614569442780906`  
		Last Modified: Tue, 28 Nov 2023 23:53:22 GMT  
		Size: 120.6 MB (120620470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:a80b48cb5cc8f60aa717eb22751a8570fad769c7812f9b42a84e3ade093b311b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d460d328ce154268676eac9f671da96cb2352e65217a215ca58afabaa330ac3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297351980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d8d377e848aeaf61958658f94c584274c82d99e22a6dd99651be5ba96e6f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f00e23cf063836a6c39fe0baef42f7ade86d7a096548dcccb4620aa0e1a2a6a NEO4J_TARBALL=neo4j-community-4.4.28-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
# Wed, 29 Nov 2023 00:31:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:31:41 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 29 Nov 2023 00:32:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:32:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:32:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:32:08 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:32:08 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:32:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:32:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518dd9fa6f2e8b1dbe8b4179346513a40f007497640d3d3106e6c651e777e11e`  
		Last Modified: Wed, 29 Nov 2023 00:35:30 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed149c654f4ca8a095fbbc727edd786187d056a73e8e8dfd88f82c519af176b`  
		Last Modified: Wed, 29 Nov 2023 00:35:30 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080af8d4c72615dd5f5edc839623ec396d175a10b9af4e4fd62fc44d9e3186fb`  
		Last Modified: Wed, 29 Nov 2023 00:35:36 GMT  
		Size: 120.7 MB (120654200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3fc0d95b6fa0f32545cadaf2dc0a52fc5baa7318c4357b66f6e66b31ca3882e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292699848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1bc02b5d9b735494549b8f9bdd8a1eb2443ecfebf53028da53ec660808e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f00e23cf063836a6c39fe0baef42f7ade86d7a096548dcccb4620aa0e1a2a6a NEO4J_TARBALL=neo4j-community-4.4.28-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
# Tue, 28 Nov 2023 23:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:49:17 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Tue, 28 Nov 2023 23:49:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:49:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:49:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:49:44 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:49:44 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:49:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:49:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eae852627a07f974b52e0963f98ded118af4d207155168b1e9cf6ec98f95e6f`  
		Last Modified: Tue, 28 Nov 2023 23:53:17 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc14782865530c96cbf6d5cb32a314f61f3922dbb2ec36e38952f51fb6dce12`  
		Last Modified: Tue, 28 Nov 2023 23:53:17 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260a28fb8cdd92c92d1c3da5af70432fcb49e1967dd8077fb614569442780906`  
		Last Modified: Tue, 28 Nov 2023 23:53:22 GMT  
		Size: 120.6 MB (120620470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:dcab7cf84e003f7ee7dec3eb9b2405d095b4c41c58f591e517e44e6d339602fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:3295b38819cd0d2bae8628e0d19a96caf01ab969c1b161ac960ba32801d74e58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.9 MB (401907356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8bf36bd02457753255c25d761f15b00a2ec959d7cf18c3e418e4d645d4ce7f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:32:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=57dab47060e05c353c0c6741d9bbd0b8bc05677e5c5e16592ebdaf1ec90b1678 NEO4J_TARBALL=neo4j-enterprise-4.4.28-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:32:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
# Wed, 29 Nov 2023 00:32:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:32:15 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 29 Nov 2023 00:32:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:32:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:32:44 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:32:44 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:32:44 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:32:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:32:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76beb1752d1c21cf0fb1100accfa1bf63953b84b5ad4bb0897c086a94b0e5b13`  
		Last Modified: Wed, 29 Nov 2023 00:35:50 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c254ba5372a7dc8d2a2eb68251b451d31a29ebb4f92ddca8b6165dfa412a71b`  
		Last Modified: Wed, 29 Nov 2023 00:35:50 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906f7ed813be5b2c95a752ca3a32ac4a1b6edba5c701f4c06aa649b5cda082fe`  
		Last Modified: Wed, 29 Nov 2023 00:36:00 GMT  
		Size: 225.2 MB (225209573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f44c245d6d70f06de0ccba87905e64d3f985e15b84c0bcecf2382f86068111a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 MB (397252702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b57c6d5087f5b6502adb6d5923377017fd96695020c9a588c6d749929ae6dfd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:49:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=57dab47060e05c353c0c6741d9bbd0b8bc05677e5c5e16592ebdaf1ec90b1678 NEO4J_TARBALL=neo4j-enterprise-4.4.28-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
# Tue, 28 Nov 2023 23:49:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:49:51 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Tue, 28 Nov 2023 23:50:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:50:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:50:25 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:50:25 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:50:25 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:50:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:50:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a819cad5822961a62b3bf77159ba95d9c6009dea8803eeb13cfdb733141cbe`  
		Last Modified: Tue, 28 Nov 2023 23:53:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbef48f116a9fa6b395109ee354484acb5b699b450aa70b5c7defb8d04673665`  
		Last Modified: Tue, 28 Nov 2023 23:53:36 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ed0c775159251ab7e6cbaed7e0e078faef5aeaaec4aadca347098feb946402`  
		Last Modified: Tue, 28 Nov 2023 23:53:44 GMT  
		Size: 225.2 MB (225173322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.28`

```console
$ docker pull neo4j@sha256:a80b48cb5cc8f60aa717eb22751a8570fad769c7812f9b42a84e3ade093b311b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.28` - linux; amd64

```console
$ docker pull neo4j@sha256:d460d328ce154268676eac9f671da96cb2352e65217a215ca58afabaa330ac3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297351980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d8d377e848aeaf61958658f94c584274c82d99e22a6dd99651be5ba96e6f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f00e23cf063836a6c39fe0baef42f7ade86d7a096548dcccb4620aa0e1a2a6a NEO4J_TARBALL=neo4j-community-4.4.28-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
# Wed, 29 Nov 2023 00:31:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:31:41 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 29 Nov 2023 00:32:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:32:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:32:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:32:08 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:32:08 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:32:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:32:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518dd9fa6f2e8b1dbe8b4179346513a40f007497640d3d3106e6c651e777e11e`  
		Last Modified: Wed, 29 Nov 2023 00:35:30 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed149c654f4ca8a095fbbc727edd786187d056a73e8e8dfd88f82c519af176b`  
		Last Modified: Wed, 29 Nov 2023 00:35:30 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080af8d4c72615dd5f5edc839623ec396d175a10b9af4e4fd62fc44d9e3186fb`  
		Last Modified: Wed, 29 Nov 2023 00:35:36 GMT  
		Size: 120.7 MB (120654200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.28` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3fc0d95b6fa0f32545cadaf2dc0a52fc5baa7318c4357b66f6e66b31ca3882e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292699848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1bc02b5d9b735494549b8f9bdd8a1eb2443ecfebf53028da53ec660808e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f00e23cf063836a6c39fe0baef42f7ade86d7a096548dcccb4620aa0e1a2a6a NEO4J_TARBALL=neo4j-community-4.4.28-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
# Tue, 28 Nov 2023 23:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:49:17 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Tue, 28 Nov 2023 23:49:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:49:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:49:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:49:44 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:49:44 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:49:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:49:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eae852627a07f974b52e0963f98ded118af4d207155168b1e9cf6ec98f95e6f`  
		Last Modified: Tue, 28 Nov 2023 23:53:17 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc14782865530c96cbf6d5cb32a314f61f3922dbb2ec36e38952f51fb6dce12`  
		Last Modified: Tue, 28 Nov 2023 23:53:17 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260a28fb8cdd92c92d1c3da5af70432fcb49e1967dd8077fb614569442780906`  
		Last Modified: Tue, 28 Nov 2023 23:53:22 GMT  
		Size: 120.6 MB (120620470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.28-community`

```console
$ docker pull neo4j@sha256:a80b48cb5cc8f60aa717eb22751a8570fad769c7812f9b42a84e3ade093b311b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.28-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d460d328ce154268676eac9f671da96cb2352e65217a215ca58afabaa330ac3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297351980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d8d377e848aeaf61958658f94c584274c82d99e22a6dd99651be5ba96e6f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f00e23cf063836a6c39fe0baef42f7ade86d7a096548dcccb4620aa0e1a2a6a NEO4J_TARBALL=neo4j-community-4.4.28-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
# Wed, 29 Nov 2023 00:31:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:31:41 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 29 Nov 2023 00:32:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:32:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:32:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:32:08 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:32:08 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:32:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:32:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518dd9fa6f2e8b1dbe8b4179346513a40f007497640d3d3106e6c651e777e11e`  
		Last Modified: Wed, 29 Nov 2023 00:35:30 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed149c654f4ca8a095fbbc727edd786187d056a73e8e8dfd88f82c519af176b`  
		Last Modified: Wed, 29 Nov 2023 00:35:30 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080af8d4c72615dd5f5edc839623ec396d175a10b9af4e4fd62fc44d9e3186fb`  
		Last Modified: Wed, 29 Nov 2023 00:35:36 GMT  
		Size: 120.7 MB (120654200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.28-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3fc0d95b6fa0f32545cadaf2dc0a52fc5baa7318c4357b66f6e66b31ca3882e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292699848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1bc02b5d9b735494549b8f9bdd8a1eb2443ecfebf53028da53ec660808e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f00e23cf063836a6c39fe0baef42f7ade86d7a096548dcccb4620aa0e1a2a6a NEO4J_TARBALL=neo4j-community-4.4.28-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
# Tue, 28 Nov 2023 23:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:49:17 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Tue, 28 Nov 2023 23:49:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:49:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:49:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:49:44 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:49:44 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:49:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:49:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eae852627a07f974b52e0963f98ded118af4d207155168b1e9cf6ec98f95e6f`  
		Last Modified: Tue, 28 Nov 2023 23:53:17 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc14782865530c96cbf6d5cb32a314f61f3922dbb2ec36e38952f51fb6dce12`  
		Last Modified: Tue, 28 Nov 2023 23:53:17 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260a28fb8cdd92c92d1c3da5af70432fcb49e1967dd8077fb614569442780906`  
		Last Modified: Tue, 28 Nov 2023 23:53:22 GMT  
		Size: 120.6 MB (120620470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.28-enterprise`

```console
$ docker pull neo4j@sha256:dcab7cf84e003f7ee7dec3eb9b2405d095b4c41c58f591e517e44e6d339602fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.28-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:3295b38819cd0d2bae8628e0d19a96caf01ab969c1b161ac960ba32801d74e58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.9 MB (401907356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8bf36bd02457753255c25d761f15b00a2ec959d7cf18c3e418e4d645d4ce7f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:32:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=57dab47060e05c353c0c6741d9bbd0b8bc05677e5c5e16592ebdaf1ec90b1678 NEO4J_TARBALL=neo4j-enterprise-4.4.28-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:32:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
# Wed, 29 Nov 2023 00:32:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:32:15 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 29 Nov 2023 00:32:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:32:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:32:44 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:32:44 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:32:44 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:32:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:32:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76beb1752d1c21cf0fb1100accfa1bf63953b84b5ad4bb0897c086a94b0e5b13`  
		Last Modified: Wed, 29 Nov 2023 00:35:50 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c254ba5372a7dc8d2a2eb68251b451d31a29ebb4f92ddca8b6165dfa412a71b`  
		Last Modified: Wed, 29 Nov 2023 00:35:50 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906f7ed813be5b2c95a752ca3a32ac4a1b6edba5c701f4c06aa649b5cda082fe`  
		Last Modified: Wed, 29 Nov 2023 00:36:00 GMT  
		Size: 225.2 MB (225209573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.28-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f44c245d6d70f06de0ccba87905e64d3f985e15b84c0bcecf2382f86068111a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 MB (397252702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b57c6d5087f5b6502adb6d5923377017fd96695020c9a588c6d749929ae6dfd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:49:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=57dab47060e05c353c0c6741d9bbd0b8bc05677e5c5e16592ebdaf1ec90b1678 NEO4J_TARBALL=neo4j-enterprise-4.4.28-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
# Tue, 28 Nov 2023 23:49:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:49:51 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Tue, 28 Nov 2023 23:50:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.28-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:50:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:50:25 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:50:25 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:50:25 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:50:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:50:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a819cad5822961a62b3bf77159ba95d9c6009dea8803eeb13cfdb733141cbe`  
		Last Modified: Tue, 28 Nov 2023 23:53:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbef48f116a9fa6b395109ee354484acb5b699b450aa70b5c7defb8d04673665`  
		Last Modified: Tue, 28 Nov 2023 23:53:36 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ed0c775159251ab7e6cbaed7e0e078faef5aeaaec4aadca347098feb946402`  
		Last Modified: Tue, 28 Nov 2023 23:53:44 GMT  
		Size: 225.2 MB (225173322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:6d9dd4c546de66040da547c9d621565e96568df1d0f7d4c6729d5eedd8c25010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:92938ba56c77626700ae57f9388e6cd393f71c52cd043161f7ae32905d5e1836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347716900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f8a6b3e5a9cb9b1ec19db680b3d525c56373d15f873d0feebe4df64173c10e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:15 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:19 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657e623249a8a0ba5096c28fd871ede82a5d4f796d4d3d1c307353490e6f9be`  
		Last Modified: Wed, 29 Nov 2023 00:34:33 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdeaa75a57305e569d1eba89bb336be98a405cbbe34d6b142a979bef2d1d2aa`  
		Last Modified: Wed, 29 Nov 2023 00:34:39 GMT  
		Size: 111.8 MB (111777049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d343f4add7969bcc73569752ecbc224a44d9262e7258b2b7aadf4df8e95221f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343964879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b0b565198ad1f30a5b8383e92f40a8957f01b4ebefc4e7c2270c736b4ab856`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:48:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:48:45 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:48:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:48:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:48:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:48:49 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:48:49 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:48:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:48:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03f2f6d75cfeaa210d880db2b563a796c40f3301b40361db49b4512b91c39e`  
		Last Modified: Tue, 28 Nov 2023 23:52:24 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd412a983c2f43575453045e8bb564b835585461aeacdd9d1ee160a661bb62c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 111.8 MB (111777086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:f740da5906a33299028fbedad8d3259faf715a6060b7e154cc824b6db5341f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:bf45e46d60e3b4fd2341e6e41c3b973678ef6588d928597cc92930c1f0a20037
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564632304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65864587fc1dc8327a8e31be9425c505bd9990a1e64ea6dbc8f10aa27cf99d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:29:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:29:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:29:19 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:53 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:53 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76245e16042381f3c4159aba8a90bd93c09c7b30a0031fb44be8b3519affbb60`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f02f2de8d53823325d23d9b8641ee59227d00399fd530ec26e8fcc5cdd163`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e39cdc1269a852259679bbb642ce6767b47750a90fd1d5531ba0830013926`  
		Last Modified: Wed, 29 Nov 2023 00:34:13 GMT  
		Size: 388.3 MB (388327222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74e144d3a711e45a05d25728e6f343ed2fad0d2c2bfe8a8e6947b3c54fd35dd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562051672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80addc7a2143359179e479eb6211771bf38fb24d81421e4de4140bff4073186`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:58 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:47:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:47:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:47:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:47:29 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:47:29 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:47:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:47:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd1f97a3f585f5cc5329f27db8af7ce2dbfd521f6d3ea13537290c11553f6e`  
		Last Modified: Tue, 28 Nov 2023 23:51:48 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd9262c2eadd8fa9b9c8b1c4b04a49020e6cee44d1c6154244103ea986f1fe`  
		Last Modified: Tue, 28 Nov 2023 23:51:49 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba6863415d1d0ab1b8a248419e1f456b5a5d91635c2211a23e06cb81a0e1f06`  
		Last Modified: Tue, 28 Nov 2023 23:52:01 GMT  
		Size: 388.3 MB (388292463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:f740da5906a33299028fbedad8d3259faf715a6060b7e154cc824b6db5341f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:bf45e46d60e3b4fd2341e6e41c3b973678ef6588d928597cc92930c1f0a20037
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564632304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65864587fc1dc8327a8e31be9425c505bd9990a1e64ea6dbc8f10aa27cf99d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:29:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:29:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:29:19 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:53 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:53 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76245e16042381f3c4159aba8a90bd93c09c7b30a0031fb44be8b3519affbb60`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f02f2de8d53823325d23d9b8641ee59227d00399fd530ec26e8fcc5cdd163`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e39cdc1269a852259679bbb642ce6767b47750a90fd1d5531ba0830013926`  
		Last Modified: Wed, 29 Nov 2023 00:34:13 GMT  
		Size: 388.3 MB (388327222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74e144d3a711e45a05d25728e6f343ed2fad0d2c2bfe8a8e6947b3c54fd35dd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562051672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80addc7a2143359179e479eb6211771bf38fb24d81421e4de4140bff4073186`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:58 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:47:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:47:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:47:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:47:29 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:47:29 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:47:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:47:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd1f97a3f585f5cc5329f27db8af7ce2dbfd521f6d3ea13537290c11553f6e`  
		Last Modified: Tue, 28 Nov 2023 23:51:48 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd9262c2eadd8fa9b9c8b1c4b04a49020e6cee44d1c6154244103ea986f1fe`  
		Last Modified: Tue, 28 Nov 2023 23:51:49 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba6863415d1d0ab1b8a248419e1f456b5a5d91635c2211a23e06cb81a0e1f06`  
		Last Modified: Tue, 28 Nov 2023 23:52:01 GMT  
		Size: 388.3 MB (388292463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:33ecd809ebe1b853b14b13b42acb455da2df8d6a7358d67e5158b02a7897869b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:64cbe0846c70657413827abc7883af262da0ca71a457074cbc2bf98c1427237a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.3 MB (621334650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0c114e02209f07f68a4c8bd79bce57d6a4b0e8eeabb96795f04335dcfc61ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:23 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:35 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:35 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:35 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc46dbd3d903c733df2a02adb6bd155d978cc78b335626849b55feacd3f495d`  
		Last Modified: Wed, 29 Nov 2023 00:35:03 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aba93be461bc08be705707b639905c951a0c9783fca02748630375520caeb7`  
		Last Modified: Wed, 29 Nov 2023 00:35:17 GMT  
		Size: 385.4 MB (385394806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:21311e0ff534ce1a8fa64fc603c8b4467d5522dfe4c7c93ebd6a1a6fc1969272
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.6 MB (617582617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5149ac8326da12823732c4fa94b04726c6e6186b8d4a1d1db08f782f3c8540d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:49:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:49:00 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:49:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:49:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:49:12 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:49:12 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:49:12 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:49:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:49:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0744863a69d444cb47a3eacb4c1978916d877497ffdf3788e5efe06e6811bd0`  
		Last Modified: Tue, 28 Nov 2023 23:52:51 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624fb4ad33b0e532c3000929ac3f944011150441ef4ab381abe80951f356dc8c`  
		Last Modified: Tue, 28 Nov 2023 23:53:04 GMT  
		Size: 385.4 MB (385394832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:6d9dd4c546de66040da547c9d621565e96568df1d0f7d4c6729d5eedd8c25010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:92938ba56c77626700ae57f9388e6cd393f71c52cd043161f7ae32905d5e1836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347716900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f8a6b3e5a9cb9b1ec19db680b3d525c56373d15f873d0feebe4df64173c10e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:15 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:19 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657e623249a8a0ba5096c28fd871ede82a5d4f796d4d3d1c307353490e6f9be`  
		Last Modified: Wed, 29 Nov 2023 00:34:33 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdeaa75a57305e569d1eba89bb336be98a405cbbe34d6b142a979bef2d1d2aa`  
		Last Modified: Wed, 29 Nov 2023 00:34:39 GMT  
		Size: 111.8 MB (111777049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d343f4add7969bcc73569752ecbc224a44d9262e7258b2b7aadf4df8e95221f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343964879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b0b565198ad1f30a5b8383e92f40a8957f01b4ebefc4e7c2270c736b4ab856`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:48:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:48:45 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:48:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:48:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:48:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:48:49 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:48:49 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:48:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:48:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03f2f6d75cfeaa210d880db2b563a796c40f3301b40361db49b4512b91c39e`  
		Last Modified: Tue, 28 Nov 2023 23:52:24 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd412a983c2f43575453045e8bb564b835585461aeacdd9d1ee160a661bb62c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 111.8 MB (111777086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14-bullseye`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14-community`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14-community` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14-community-bullseye`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14-community-ubi8`

```console
$ docker pull neo4j@sha256:6d9dd4c546de66040da547c9d621565e96568df1d0f7d4c6729d5eedd8c25010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:92938ba56c77626700ae57f9388e6cd393f71c52cd043161f7ae32905d5e1836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347716900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f8a6b3e5a9cb9b1ec19db680b3d525c56373d15f873d0feebe4df64173c10e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:15 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:19 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657e623249a8a0ba5096c28fd871ede82a5d4f796d4d3d1c307353490e6f9be`  
		Last Modified: Wed, 29 Nov 2023 00:34:33 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdeaa75a57305e569d1eba89bb336be98a405cbbe34d6b142a979bef2d1d2aa`  
		Last Modified: Wed, 29 Nov 2023 00:34:39 GMT  
		Size: 111.8 MB (111777049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d343f4add7969bcc73569752ecbc224a44d9262e7258b2b7aadf4df8e95221f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343964879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b0b565198ad1f30a5b8383e92f40a8957f01b4ebefc4e7c2270c736b4ab856`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:48:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:48:45 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:48:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:48:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:48:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:48:49 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:48:49 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:48:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:48:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03f2f6d75cfeaa210d880db2b563a796c40f3301b40361db49b4512b91c39e`  
		Last Modified: Tue, 28 Nov 2023 23:52:24 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd412a983c2f43575453045e8bb564b835585461aeacdd9d1ee160a661bb62c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 111.8 MB (111777086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14-enterprise`

```console
$ docker pull neo4j@sha256:f740da5906a33299028fbedad8d3259faf715a6060b7e154cc824b6db5341f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:bf45e46d60e3b4fd2341e6e41c3b973678ef6588d928597cc92930c1f0a20037
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564632304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65864587fc1dc8327a8e31be9425c505bd9990a1e64ea6dbc8f10aa27cf99d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:29:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:29:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:29:19 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:53 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:53 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76245e16042381f3c4159aba8a90bd93c09c7b30a0031fb44be8b3519affbb60`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f02f2de8d53823325d23d9b8641ee59227d00399fd530ec26e8fcc5cdd163`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e39cdc1269a852259679bbb642ce6767b47750a90fd1d5531ba0830013926`  
		Last Modified: Wed, 29 Nov 2023 00:34:13 GMT  
		Size: 388.3 MB (388327222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74e144d3a711e45a05d25728e6f343ed2fad0d2c2bfe8a8e6947b3c54fd35dd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562051672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80addc7a2143359179e479eb6211771bf38fb24d81421e4de4140bff4073186`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:58 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:47:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:47:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:47:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:47:29 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:47:29 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:47:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:47:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd1f97a3f585f5cc5329f27db8af7ce2dbfd521f6d3ea13537290c11553f6e`  
		Last Modified: Tue, 28 Nov 2023 23:51:48 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd9262c2eadd8fa9b9c8b1c4b04a49020e6cee44d1c6154244103ea986f1fe`  
		Last Modified: Tue, 28 Nov 2023 23:51:49 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba6863415d1d0ab1b8a248419e1f456b5a5d91635c2211a23e06cb81a0e1f06`  
		Last Modified: Tue, 28 Nov 2023 23:52:01 GMT  
		Size: 388.3 MB (388292463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:f740da5906a33299028fbedad8d3259faf715a6060b7e154cc824b6db5341f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:bf45e46d60e3b4fd2341e6e41c3b973678ef6588d928597cc92930c1f0a20037
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564632304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65864587fc1dc8327a8e31be9425c505bd9990a1e64ea6dbc8f10aa27cf99d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:29:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:29:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:29:19 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:53 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:53 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76245e16042381f3c4159aba8a90bd93c09c7b30a0031fb44be8b3519affbb60`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f02f2de8d53823325d23d9b8641ee59227d00399fd530ec26e8fcc5cdd163`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e39cdc1269a852259679bbb642ce6767b47750a90fd1d5531ba0830013926`  
		Last Modified: Wed, 29 Nov 2023 00:34:13 GMT  
		Size: 388.3 MB (388327222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74e144d3a711e45a05d25728e6f343ed2fad0d2c2bfe8a8e6947b3c54fd35dd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562051672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80addc7a2143359179e479eb6211771bf38fb24d81421e4de4140bff4073186`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:58 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:47:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:47:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:47:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:47:29 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:47:29 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:47:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:47:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd1f97a3f585f5cc5329f27db8af7ce2dbfd521f6d3ea13537290c11553f6e`  
		Last Modified: Tue, 28 Nov 2023 23:51:48 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd9262c2eadd8fa9b9c8b1c4b04a49020e6cee44d1c6154244103ea986f1fe`  
		Last Modified: Tue, 28 Nov 2023 23:51:49 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba6863415d1d0ab1b8a248419e1f456b5a5d91635c2211a23e06cb81a0e1f06`  
		Last Modified: Tue, 28 Nov 2023 23:52:01 GMT  
		Size: 388.3 MB (388292463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:33ecd809ebe1b853b14b13b42acb455da2df8d6a7358d67e5158b02a7897869b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:64cbe0846c70657413827abc7883af262da0ca71a457074cbc2bf98c1427237a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.3 MB (621334650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0c114e02209f07f68a4c8bd79bce57d6a4b0e8eeabb96795f04335dcfc61ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:23 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:35 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:35 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:35 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc46dbd3d903c733df2a02adb6bd155d978cc78b335626849b55feacd3f495d`  
		Last Modified: Wed, 29 Nov 2023 00:35:03 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aba93be461bc08be705707b639905c951a0c9783fca02748630375520caeb7`  
		Last Modified: Wed, 29 Nov 2023 00:35:17 GMT  
		Size: 385.4 MB (385394806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:21311e0ff534ce1a8fa64fc603c8b4467d5522dfe4c7c93ebd6a1a6fc1969272
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.6 MB (617582617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5149ac8326da12823732c4fa94b04726c6e6186b8d4a1d1db08f782f3c8540d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:49:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:49:00 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:49:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:49:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:49:12 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:49:12 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:49:12 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:49:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:49:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0744863a69d444cb47a3eacb4c1978916d877497ffdf3788e5efe06e6811bd0`  
		Last Modified: Tue, 28 Nov 2023 23:52:51 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624fb4ad33b0e532c3000929ac3f944011150441ef4ab381abe80951f356dc8c`  
		Last Modified: Tue, 28 Nov 2023 23:53:04 GMT  
		Size: 385.4 MB (385394832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14-ubi8`

```console
$ docker pull neo4j@sha256:6d9dd4c546de66040da547c9d621565e96568df1d0f7d4c6729d5eedd8c25010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:92938ba56c77626700ae57f9388e6cd393f71c52cd043161f7ae32905d5e1836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347716900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f8a6b3e5a9cb9b1ec19db680b3d525c56373d15f873d0feebe4df64173c10e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:15 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:19 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657e623249a8a0ba5096c28fd871ede82a5d4f796d4d3d1c307353490e6f9be`  
		Last Modified: Wed, 29 Nov 2023 00:34:33 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdeaa75a57305e569d1eba89bb336be98a405cbbe34d6b142a979bef2d1d2aa`  
		Last Modified: Wed, 29 Nov 2023 00:34:39 GMT  
		Size: 111.8 MB (111777049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d343f4add7969bcc73569752ecbc224a44d9262e7258b2b7aadf4df8e95221f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343964879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b0b565198ad1f30a5b8383e92f40a8957f01b4ebefc4e7c2270c736b4ab856`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:48:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:48:45 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:48:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:48:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:48:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:48:49 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:48:49 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:48:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:48:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03f2f6d75cfeaa210d880db2b563a796c40f3301b40361db49b4512b91c39e`  
		Last Modified: Tue, 28 Nov 2023 23:52:24 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd412a983c2f43575453045e8bb564b835585461aeacdd9d1ee160a661bb62c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 111.8 MB (111777086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14.0`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14.0` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14.0-bullseye`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14.0-community`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14.0-community-bullseye`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14.0-community-ubi8`

```console
$ docker pull neo4j@sha256:6d9dd4c546de66040da547c9d621565e96568df1d0f7d4c6729d5eedd8c25010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:92938ba56c77626700ae57f9388e6cd393f71c52cd043161f7ae32905d5e1836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347716900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f8a6b3e5a9cb9b1ec19db680b3d525c56373d15f873d0feebe4df64173c10e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:15 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:19 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657e623249a8a0ba5096c28fd871ede82a5d4f796d4d3d1c307353490e6f9be`  
		Last Modified: Wed, 29 Nov 2023 00:34:33 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdeaa75a57305e569d1eba89bb336be98a405cbbe34d6b142a979bef2d1d2aa`  
		Last Modified: Wed, 29 Nov 2023 00:34:39 GMT  
		Size: 111.8 MB (111777049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d343f4add7969bcc73569752ecbc224a44d9262e7258b2b7aadf4df8e95221f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343964879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b0b565198ad1f30a5b8383e92f40a8957f01b4ebefc4e7c2270c736b4ab856`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:48:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:48:45 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:48:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:48:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:48:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:48:49 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:48:49 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:48:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:48:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03f2f6d75cfeaa210d880db2b563a796c40f3301b40361db49b4512b91c39e`  
		Last Modified: Tue, 28 Nov 2023 23:52:24 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd412a983c2f43575453045e8bb564b835585461aeacdd9d1ee160a661bb62c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 111.8 MB (111777086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14.0-enterprise`

```console
$ docker pull neo4j@sha256:f740da5906a33299028fbedad8d3259faf715a6060b7e154cc824b6db5341f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:bf45e46d60e3b4fd2341e6e41c3b973678ef6588d928597cc92930c1f0a20037
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564632304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65864587fc1dc8327a8e31be9425c505bd9990a1e64ea6dbc8f10aa27cf99d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:29:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:29:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:29:19 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:53 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:53 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76245e16042381f3c4159aba8a90bd93c09c7b30a0031fb44be8b3519affbb60`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f02f2de8d53823325d23d9b8641ee59227d00399fd530ec26e8fcc5cdd163`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e39cdc1269a852259679bbb642ce6767b47750a90fd1d5531ba0830013926`  
		Last Modified: Wed, 29 Nov 2023 00:34:13 GMT  
		Size: 388.3 MB (388327222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74e144d3a711e45a05d25728e6f343ed2fad0d2c2bfe8a8e6947b3c54fd35dd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562051672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80addc7a2143359179e479eb6211771bf38fb24d81421e4de4140bff4073186`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:58 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:47:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:47:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:47:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:47:29 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:47:29 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:47:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:47:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd1f97a3f585f5cc5329f27db8af7ce2dbfd521f6d3ea13537290c11553f6e`  
		Last Modified: Tue, 28 Nov 2023 23:51:48 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd9262c2eadd8fa9b9c8b1c4b04a49020e6cee44d1c6154244103ea986f1fe`  
		Last Modified: Tue, 28 Nov 2023 23:51:49 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba6863415d1d0ab1b8a248419e1f456b5a5d91635c2211a23e06cb81a0e1f06`  
		Last Modified: Tue, 28 Nov 2023 23:52:01 GMT  
		Size: 388.3 MB (388292463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:f740da5906a33299028fbedad8d3259faf715a6060b7e154cc824b6db5341f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:bf45e46d60e3b4fd2341e6e41c3b973678ef6588d928597cc92930c1f0a20037
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564632304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65864587fc1dc8327a8e31be9425c505bd9990a1e64ea6dbc8f10aa27cf99d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:29:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:29:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:29:19 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:53 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:53 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76245e16042381f3c4159aba8a90bd93c09c7b30a0031fb44be8b3519affbb60`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f02f2de8d53823325d23d9b8641ee59227d00399fd530ec26e8fcc5cdd163`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e39cdc1269a852259679bbb642ce6767b47750a90fd1d5531ba0830013926`  
		Last Modified: Wed, 29 Nov 2023 00:34:13 GMT  
		Size: 388.3 MB (388327222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74e144d3a711e45a05d25728e6f343ed2fad0d2c2bfe8a8e6947b3c54fd35dd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562051672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80addc7a2143359179e479eb6211771bf38fb24d81421e4de4140bff4073186`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:58 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:47:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:47:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:47:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:47:29 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:47:29 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:47:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:47:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd1f97a3f585f5cc5329f27db8af7ce2dbfd521f6d3ea13537290c11553f6e`  
		Last Modified: Tue, 28 Nov 2023 23:51:48 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd9262c2eadd8fa9b9c8b1c4b04a49020e6cee44d1c6154244103ea986f1fe`  
		Last Modified: Tue, 28 Nov 2023 23:51:49 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba6863415d1d0ab1b8a248419e1f456b5a5d91635c2211a23e06cb81a0e1f06`  
		Last Modified: Tue, 28 Nov 2023 23:52:01 GMT  
		Size: 388.3 MB (388292463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:33ecd809ebe1b853b14b13b42acb455da2df8d6a7358d67e5158b02a7897869b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:64cbe0846c70657413827abc7883af262da0ca71a457074cbc2bf98c1427237a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.3 MB (621334650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0c114e02209f07f68a4c8bd79bce57d6a4b0e8eeabb96795f04335dcfc61ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:23 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:35 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:35 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:35 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc46dbd3d903c733df2a02adb6bd155d978cc78b335626849b55feacd3f495d`  
		Last Modified: Wed, 29 Nov 2023 00:35:03 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aba93be461bc08be705707b639905c951a0c9783fca02748630375520caeb7`  
		Last Modified: Wed, 29 Nov 2023 00:35:17 GMT  
		Size: 385.4 MB (385394806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:21311e0ff534ce1a8fa64fc603c8b4467d5522dfe4c7c93ebd6a1a6fc1969272
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.6 MB (617582617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5149ac8326da12823732c4fa94b04726c6e6186b8d4a1d1db08f782f3c8540d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:49:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:49:00 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:49:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:49:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:49:12 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:49:12 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:49:12 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:49:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:49:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0744863a69d444cb47a3eacb4c1978916d877497ffdf3788e5efe06e6811bd0`  
		Last Modified: Tue, 28 Nov 2023 23:52:51 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624fb4ad33b0e532c3000929ac3f944011150441ef4ab381abe80951f356dc8c`  
		Last Modified: Tue, 28 Nov 2023 23:53:04 GMT  
		Size: 385.4 MB (385394832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.14.0-ubi8`

```console
$ docker pull neo4j@sha256:6d9dd4c546de66040da547c9d621565e96568df1d0f7d4c6729d5eedd8c25010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.14.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:92938ba56c77626700ae57f9388e6cd393f71c52cd043161f7ae32905d5e1836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347716900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f8a6b3e5a9cb9b1ec19db680b3d525c56373d15f873d0feebe4df64173c10e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:15 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:19 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657e623249a8a0ba5096c28fd871ede82a5d4f796d4d3d1c307353490e6f9be`  
		Last Modified: Wed, 29 Nov 2023 00:34:33 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdeaa75a57305e569d1eba89bb336be98a405cbbe34d6b142a979bef2d1d2aa`  
		Last Modified: Wed, 29 Nov 2023 00:34:39 GMT  
		Size: 111.8 MB (111777049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.14.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d343f4add7969bcc73569752ecbc224a44d9262e7258b2b7aadf4df8e95221f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343964879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b0b565198ad1f30a5b8383e92f40a8957f01b4ebefc4e7c2270c736b4ab856`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:48:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:48:45 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:48:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:48:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:48:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:48:49 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:48:49 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:48:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:48:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03f2f6d75cfeaa210d880db2b563a796c40f3301b40361db49b4512b91c39e`  
		Last Modified: Tue, 28 Nov 2023 23:52:24 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd412a983c2f43575453045e8bb564b835585461aeacdd9d1ee160a661bb62c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 111.8 MB (111777086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:6d9dd4c546de66040da547c9d621565e96568df1d0f7d4c6729d5eedd8c25010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:92938ba56c77626700ae57f9388e6cd393f71c52cd043161f7ae32905d5e1836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347716900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f8a6b3e5a9cb9b1ec19db680b3d525c56373d15f873d0feebe4df64173c10e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:15 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:19 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657e623249a8a0ba5096c28fd871ede82a5d4f796d4d3d1c307353490e6f9be`  
		Last Modified: Wed, 29 Nov 2023 00:34:33 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdeaa75a57305e569d1eba89bb336be98a405cbbe34d6b142a979bef2d1d2aa`  
		Last Modified: Wed, 29 Nov 2023 00:34:39 GMT  
		Size: 111.8 MB (111777049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d343f4add7969bcc73569752ecbc224a44d9262e7258b2b7aadf4df8e95221f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343964879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b0b565198ad1f30a5b8383e92f40a8957f01b4ebefc4e7c2270c736b4ab856`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:48:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:48:45 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:48:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:48:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:48:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:48:49 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:48:49 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:48:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:48:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03f2f6d75cfeaa210d880db2b563a796c40f3301b40361db49b4512b91c39e`  
		Last Modified: Tue, 28 Nov 2023 23:52:24 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd412a983c2f43575453045e8bb564b835585461aeacdd9d1ee160a661bb62c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 111.8 MB (111777086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:f740da5906a33299028fbedad8d3259faf715a6060b7e154cc824b6db5341f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:bf45e46d60e3b4fd2341e6e41c3b973678ef6588d928597cc92930c1f0a20037
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564632304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65864587fc1dc8327a8e31be9425c505bd9990a1e64ea6dbc8f10aa27cf99d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:29:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:29:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:29:19 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:53 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:53 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76245e16042381f3c4159aba8a90bd93c09c7b30a0031fb44be8b3519affbb60`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f02f2de8d53823325d23d9b8641ee59227d00399fd530ec26e8fcc5cdd163`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e39cdc1269a852259679bbb642ce6767b47750a90fd1d5531ba0830013926`  
		Last Modified: Wed, 29 Nov 2023 00:34:13 GMT  
		Size: 388.3 MB (388327222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74e144d3a711e45a05d25728e6f343ed2fad0d2c2bfe8a8e6947b3c54fd35dd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562051672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80addc7a2143359179e479eb6211771bf38fb24d81421e4de4140bff4073186`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:58 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:47:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:47:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:47:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:47:29 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:47:29 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:47:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:47:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd1f97a3f585f5cc5329f27db8af7ce2dbfd521f6d3ea13537290c11553f6e`  
		Last Modified: Tue, 28 Nov 2023 23:51:48 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd9262c2eadd8fa9b9c8b1c4b04a49020e6cee44d1c6154244103ea986f1fe`  
		Last Modified: Tue, 28 Nov 2023 23:51:49 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba6863415d1d0ab1b8a248419e1f456b5a5d91635c2211a23e06cb81a0e1f06`  
		Last Modified: Tue, 28 Nov 2023 23:52:01 GMT  
		Size: 388.3 MB (388292463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:f740da5906a33299028fbedad8d3259faf715a6060b7e154cc824b6db5341f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:bf45e46d60e3b4fd2341e6e41c3b973678ef6588d928597cc92930c1f0a20037
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564632304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65864587fc1dc8327a8e31be9425c505bd9990a1e64ea6dbc8f10aa27cf99d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:29:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:29:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:29:19 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:53 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:53 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76245e16042381f3c4159aba8a90bd93c09c7b30a0031fb44be8b3519affbb60`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f02f2de8d53823325d23d9b8641ee59227d00399fd530ec26e8fcc5cdd163`  
		Last Modified: Wed, 29 Nov 2023 00:33:58 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e39cdc1269a852259679bbb642ce6767b47750a90fd1d5531ba0830013926`  
		Last Modified: Wed, 29 Nov 2023 00:34:13 GMT  
		Size: 388.3 MB (388327222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74e144d3a711e45a05d25728e6f343ed2fad0d2c2bfe8a8e6947b3c54fd35dd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562051672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80addc7a2143359179e479eb6211771bf38fb24d81421e4de4140bff4073186`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:58 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:47:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:47:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:47:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:47:29 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:47:29 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:47:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:47:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd1f97a3f585f5cc5329f27db8af7ce2dbfd521f6d3ea13537290c11553f6e`  
		Last Modified: Tue, 28 Nov 2023 23:51:48 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd9262c2eadd8fa9b9c8b1c4b04a49020e6cee44d1c6154244103ea986f1fe`  
		Last Modified: Tue, 28 Nov 2023 23:51:49 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba6863415d1d0ab1b8a248419e1f456b5a5d91635c2211a23e06cb81a0e1f06`  
		Last Modified: Tue, 28 Nov 2023 23:52:01 GMT  
		Size: 388.3 MB (388292463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:33ecd809ebe1b853b14b13b42acb455da2df8d6a7358d67e5158b02a7897869b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:64cbe0846c70657413827abc7883af262da0ca71a457074cbc2bf98c1427237a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.3 MB (621334650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0c114e02209f07f68a4c8bd79bce57d6a4b0e8eeabb96795f04335dcfc61ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:23 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:35 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:35 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:35 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc46dbd3d903c733df2a02adb6bd155d978cc78b335626849b55feacd3f495d`  
		Last Modified: Wed, 29 Nov 2023 00:35:03 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aba93be461bc08be705707b639905c951a0c9783fca02748630375520caeb7`  
		Last Modified: Wed, 29 Nov 2023 00:35:17 GMT  
		Size: 385.4 MB (385394806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:21311e0ff534ce1a8fa64fc603c8b4467d5522dfe4c7c93ebd6a1a6fc1969272
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.6 MB (617582617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5149ac8326da12823732c4fa94b04726c6e6186b8d4a1d1db08f782f3c8540d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:49:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:49:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:49:00 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:49:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:49:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:49:12 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:49:12 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:49:12 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:49:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:49:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0744863a69d444cb47a3eacb4c1978916d877497ffdf3788e5efe06e6811bd0`  
		Last Modified: Tue, 28 Nov 2023 23:52:51 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624fb4ad33b0e532c3000929ac3f944011150441ef4ab381abe80951f356dc8c`  
		Last Modified: Tue, 28 Nov 2023 23:53:04 GMT  
		Size: 385.4 MB (385394832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:e83407f3910b027b7c91439c2bf812a84a277dfea8310874148e8b24e516d41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:5aa31aadb7f040f8803ccb7b0ead9a2d1e083a2f9218736a1bc4366e003c3a69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbacfd0af22c808f74feafb64d518e09b780121d407f1c46f8f5b68f2787d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:28:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Nov 2023 00:28:38 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:29:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 29 Nov 2023 00:29:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:29:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:29:09 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:29:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:29:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:29:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfceacc6ff0bac1e1f38eb74b5147714f8f8e95b31781665cd749daa636650e5`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0327908610b65c76d0aa08406366b92da34cc372224754536a7a215856c95fb`  
		Last Modified: Wed, 29 Nov 2023 00:33:16 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc072a3a3ddacd86ad791ec96fb62c8832ff0a69acc7bb97c62f96ef5b7bcca`  
		Last Modified: Wed, 29 Nov 2023 00:33:21 GMT  
		Size: 114.7 MB (114712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f23037073daead705db76cdacb4fd5784cfbadbb7016cbea052a6b5058475ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625b6cb44707cf837448a4f46f84d16c0c2925edc311d6e07a60c7c8a8bc05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:46:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:46:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 28 Nov 2023 23:46:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 28 Nov 2023 23:46:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:46:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:46:52 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:46:52 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:46:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5da089d9a839c05c798160cf1d4c26e642fcf08cc3a9d0ef4d3594a9be811`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9598a13c21e2cc0257447ff69ea0bde43ac949490c915618a567fa26c47ec`  
		Last Modified: Tue, 28 Nov 2023 23:51:07 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641807d671f900febacc03b4d1a3cab399a5474538b53e246bf51b9ccd20f53`  
		Last Modified: Tue, 28 Nov 2023 23:51:12 GMT  
		Size: 114.7 MB (114673999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:6d9dd4c546de66040da547c9d621565e96568df1d0f7d4c6729d5eedd8c25010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:92938ba56c77626700ae57f9388e6cd393f71c52cd043161f7ae32905d5e1836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347716900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f8a6b3e5a9cb9b1ec19db680b3d525c56373d15f873d0feebe4df64173c10e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 29 Nov 2023 00:31:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Wed, 29 Nov 2023 00:31:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Nov 2023 00:31:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Wed, 29 Nov 2023 00:31:15 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 29 Nov 2023 00:31:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 29 Nov 2023 00:31:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:31:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Nov 2023 00:31:19 GMT
VOLUME [/data /logs]
# Wed, 29 Nov 2023 00:31:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Nov 2023 00:31:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:31:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18026696efb9c03bec9f60a01b37bfc1598bb9e74a7211315c3866417bf4d22`  
		Last Modified: Wed, 29 Nov 2023 00:34:41 GMT  
		Size: 51.7 MB (51714751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657e623249a8a0ba5096c28fd871ede82a5d4f796d4d3d1c307353490e6f9be`  
		Last Modified: Wed, 29 Nov 2023 00:34:33 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdeaa75a57305e569d1eba89bb336be98a405cbbe34d6b142a979bef2d1d2aa`  
		Last Modified: Wed, 29 Nov 2023 00:34:39 GMT  
		Size: 111.8 MB (111777049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d343f4add7969bcc73569752ecbc224a44d9262e7258b2b7aadf4df8e95221f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343964879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b0b565198ad1f30a5b8383e92f40a8957f01b4ebefc4e7c2270c736b4ab856`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 28 Nov 2023 23:48:44 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Tue, 28 Nov 2023 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 28 Nov 2023 23:48:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Tue, 28 Nov 2023 23:48:45 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 28 Nov 2023 23:48:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 28 Nov 2023 23:48:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:48:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 28 Nov 2023 23:48:49 GMT
VOLUME [/data /logs]
# Tue, 28 Nov 2023 23:48:49 GMT
EXPOSE 7473 7474 7687
# Tue, 28 Nov 2023 23:48:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:48:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c637756d994412deb214f165bea6859a2d55c34312ed0c8962ad51fda176c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 50.8 MB (50813702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03f2f6d75cfeaa210d880db2b563a796c40f3301b40361db49b4512b91c39e`  
		Last Modified: Tue, 28 Nov 2023 23:52:24 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd412a983c2f43575453045e8bb564b835585461aeacdd9d1ee160a661bb62c`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 111.8 MB (111777086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
