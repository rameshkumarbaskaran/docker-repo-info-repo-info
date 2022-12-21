<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.3`](#neo4j43)
-	[`neo4j:4.3-community`](#neo4j43-community)
-	[`neo4j:4.3-enterprise`](#neo4j43-enterprise)
-	[`neo4j:4.3.22`](#neo4j4322)
-	[`neo4j:4.3.22-community`](#neo4j4322-community)
-	[`neo4j:4.3.22-enterprise`](#neo4j4322-enterprise)
-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.15`](#neo4j4415)
-	[`neo4j:4.4.15-community`](#neo4j4415-community)
-	[`neo4j:4.4.15-enterprise`](#neo4j4415-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.2`](#neo4j52)
-	[`neo4j:5.2-enterprise`](#neo4j52-enterprise)
-	[`neo4j:5.2.0`](#neo4j520)
-	[`neo4j:5.2.0-community`](#neo4j520-community)
-	[`neo4j:5.2.0-enterprise`](#neo4j520-enterprise)
-	[`neo4j:5.3`](#neo4j53)
-	[`neo4j:5.3-enterprise`](#neo4j53-enterprise)
-	[`neo4j:5.3.0`](#neo4j530)
-	[`neo4j:5.3.0-community`](#neo4j530-community)
-	[`neo4j:5.3.0-enterprise`](#neo4j530-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.3`

```console
$ docker pull neo4j@sha256:3254c510e3964349f2dd31b05960997414a42bd50a1ef6a2284fef251e5eb1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3` - linux; amd64

```console
$ docker pull neo4j@sha256:7b7fd5b24aaa97eea2f35bfb40d63497285e10794291a99ee3a8877e5d11c258
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360395581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54974f0419a4ee10fb3ff4d5c1ea589e8928fec45627b18b276cf38cc52762b1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:55:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb4f97266d8057fbf15012235106a7241c66cc27475187eb6a6d3cdc9298e534 NEO4J_TARBALL=neo4j-community-4.3.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:55:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
# Wed, 21 Dec 2022 11:55:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:55:20 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Wed, 21 Dec 2022 11:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:55:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:55:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:55:37 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:55:37 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957f6332e51a5dfc3a81ad0e26f805c8ae872c4016ae3a4cb0c0e208b555ce13`  
		Last Modified: Wed, 21 Dec 2022 11:58:34 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0be55406d04748a9265b652006a15d5b420d85436111c92915f6d4789a9d61b`  
		Last Modified: Wed, 21 Dec 2022 11:58:34 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309a95613972df65ff648a11554c7524bfbfa85648e8abefd1f20ab8d8860701`  
		Last Modified: Wed, 21 Dec 2022 11:58:42 GMT  
		Size: 130.5 MB (130532592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-community`

```console
$ docker pull neo4j@sha256:3254c510e3964349f2dd31b05960997414a42bd50a1ef6a2284fef251e5eb1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-community` - linux; amd64

```console
$ docker pull neo4j@sha256:7b7fd5b24aaa97eea2f35bfb40d63497285e10794291a99ee3a8877e5d11c258
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360395581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54974f0419a4ee10fb3ff4d5c1ea589e8928fec45627b18b276cf38cc52762b1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:55:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb4f97266d8057fbf15012235106a7241c66cc27475187eb6a6d3cdc9298e534 NEO4J_TARBALL=neo4j-community-4.3.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:55:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
# Wed, 21 Dec 2022 11:55:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:55:20 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Wed, 21 Dec 2022 11:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:55:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:55:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:55:37 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:55:37 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957f6332e51a5dfc3a81ad0e26f805c8ae872c4016ae3a4cb0c0e208b555ce13`  
		Last Modified: Wed, 21 Dec 2022 11:58:34 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0be55406d04748a9265b652006a15d5b420d85436111c92915f6d4789a9d61b`  
		Last Modified: Wed, 21 Dec 2022 11:58:34 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309a95613972df65ff648a11554c7524bfbfa85648e8abefd1f20ab8d8860701`  
		Last Modified: Wed, 21 Dec 2022 11:58:42 GMT  
		Size: 130.5 MB (130532592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-enterprise`

```console
$ docker pull neo4j@sha256:ad7e7cf5ae8acee2fe295212efe800c3f6fdc525e1a3ffeb0d2a7b72ee914c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:4a067a11ae9903745d1b8ccc5f489dc1481882815a984e37768171c129435fc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 MB (390898840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c2eb637cb9a97a9254365f294437d10b00e647bb5481ec7f069e45f91710ba`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:55:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=eac8dab9669ad128ae65fabfac982087eaebb6b3bc011e688d33eb379ed92629 NEO4J_TARBALL=neo4j-enterprise-4.3.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:55:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
# Wed, 21 Dec 2022 11:55:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:55:44 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Wed, 21 Dec 2022 11:56:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:56:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:56:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:56:02 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:56:02 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:56:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:56:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904a828face08638e6917a40735402923d3ceca95c88b0ca85a96fd4edc6f72`  
		Last Modified: Wed, 21 Dec 2022 11:58:54 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fde765240b1a7ffed25c1cd955399958eccbcac0e54fd9241a67874626a24e`  
		Last Modified: Wed, 21 Dec 2022 11:58:54 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e949f67dea6139b19746646161ba930dc871178194d26afbe7c7384376e6f884`  
		Last Modified: Wed, 21 Dec 2022 11:59:02 GMT  
		Size: 161.0 MB (161035859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.22`

```console
$ docker pull neo4j@sha256:3254c510e3964349f2dd31b05960997414a42bd50a1ef6a2284fef251e5eb1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.22` - linux; amd64

```console
$ docker pull neo4j@sha256:7b7fd5b24aaa97eea2f35bfb40d63497285e10794291a99ee3a8877e5d11c258
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360395581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54974f0419a4ee10fb3ff4d5c1ea589e8928fec45627b18b276cf38cc52762b1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:55:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb4f97266d8057fbf15012235106a7241c66cc27475187eb6a6d3cdc9298e534 NEO4J_TARBALL=neo4j-community-4.3.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:55:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
# Wed, 21 Dec 2022 11:55:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:55:20 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Wed, 21 Dec 2022 11:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:55:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:55:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:55:37 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:55:37 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957f6332e51a5dfc3a81ad0e26f805c8ae872c4016ae3a4cb0c0e208b555ce13`  
		Last Modified: Wed, 21 Dec 2022 11:58:34 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0be55406d04748a9265b652006a15d5b420d85436111c92915f6d4789a9d61b`  
		Last Modified: Wed, 21 Dec 2022 11:58:34 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309a95613972df65ff648a11554c7524bfbfa85648e8abefd1f20ab8d8860701`  
		Last Modified: Wed, 21 Dec 2022 11:58:42 GMT  
		Size: 130.5 MB (130532592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.22-community`

```console
$ docker pull neo4j@sha256:3254c510e3964349f2dd31b05960997414a42bd50a1ef6a2284fef251e5eb1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.22-community` - linux; amd64

```console
$ docker pull neo4j@sha256:7b7fd5b24aaa97eea2f35bfb40d63497285e10794291a99ee3a8877e5d11c258
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360395581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54974f0419a4ee10fb3ff4d5c1ea589e8928fec45627b18b276cf38cc52762b1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:55:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb4f97266d8057fbf15012235106a7241c66cc27475187eb6a6d3cdc9298e534 NEO4J_TARBALL=neo4j-community-4.3.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:55:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
# Wed, 21 Dec 2022 11:55:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:55:20 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Wed, 21 Dec 2022 11:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:55:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:55:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:55:37 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:55:37 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957f6332e51a5dfc3a81ad0e26f805c8ae872c4016ae3a4cb0c0e208b555ce13`  
		Last Modified: Wed, 21 Dec 2022 11:58:34 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0be55406d04748a9265b652006a15d5b420d85436111c92915f6d4789a9d61b`  
		Last Modified: Wed, 21 Dec 2022 11:58:34 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309a95613972df65ff648a11554c7524bfbfa85648e8abefd1f20ab8d8860701`  
		Last Modified: Wed, 21 Dec 2022 11:58:42 GMT  
		Size: 130.5 MB (130532592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.22-enterprise`

```console
$ docker pull neo4j@sha256:ad7e7cf5ae8acee2fe295212efe800c3f6fdc525e1a3ffeb0d2a7b72ee914c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.22-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:4a067a11ae9903745d1b8ccc5f489dc1481882815a984e37768171c129435fc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 MB (390898840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c2eb637cb9a97a9254365f294437d10b00e647bb5481ec7f069e45f91710ba`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:55:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=eac8dab9669ad128ae65fabfac982087eaebb6b3bc011e688d33eb379ed92629 NEO4J_TARBALL=neo4j-enterprise-4.3.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:55:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
# Wed, 21 Dec 2022 11:55:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:55:44 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Wed, 21 Dec 2022 11:56:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:56:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:56:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:56:02 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:56:02 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:56:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:56:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904a828face08638e6917a40735402923d3ceca95c88b0ca85a96fd4edc6f72`  
		Last Modified: Wed, 21 Dec 2022 11:58:54 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fde765240b1a7ffed25c1cd955399958eccbcac0e54fd9241a67874626a24e`  
		Last Modified: Wed, 21 Dec 2022 11:58:54 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e949f67dea6139b19746646161ba930dc871178194d26afbe7c7384376e6f884`  
		Last Modified: Wed, 21 Dec 2022 11:59:02 GMT  
		Size: 161.0 MB (161035859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:b7c68e2d094f8ed986316fd719c849d16726c2e078fc7c4e6d10e9dc6d7910ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:8f41afc36817b80873ddbf439195bea8306e1d07b9b15cacc7fe3db63c2f6ba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365280701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a1c54200cadb166a13ca5ff49aad8675a505e2f1ec9eab62adea2263a3394`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:54:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:54:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Wed, 21 Dec 2022 11:54:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:54:28 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Wed, 21 Dec 2022 11:54:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:54:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:54:45 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:54:45 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:54:45 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:54:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:54:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea29a925d6d469af60c170c243ae635b2b44f24f708f8ec26d1ceb8fed83b0`  
		Last Modified: Wed, 21 Dec 2022 11:57:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f25799ab7bd6bd9cce3191f98c20fd7bf1d2143f5976cb9fb813f0ba6f80d`  
		Last Modified: Wed, 21 Dec 2022 11:57:56 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d939b3dc311402c3d2bc29edecea34d5d395e87dc626eec65a2194060193a7b3`  
		Last Modified: Wed, 21 Dec 2022 11:58:03 GMT  
		Size: 135.4 MB (135417178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0b8463a7237f648a135381fe814b747fe90beb9b9f159190ccef082b54bc90ec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360552059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4251b853f2a32a447e7657725de68a4c57b42c13309b55cb974ae4e3ebb00003`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 05:04:05 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Fri, 09 Dec 2022 06:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:05:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Fri, 09 Dec 2022 06:05:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:05:02 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 09 Dec 2022 06:05:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:05:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:05:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:05:12 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:05:12 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:05:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:05:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44bbb0380eb6b5cd1051003f5ce31baf496a9113c5e9927f76bcf714c433145`  
		Last Modified: Fri, 09 Dec 2022 05:18:38 GMT  
		Size: 195.2 MB (195203372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddf1b63ee1021fb4d42c559adb38c1d219199899fd8bcf7038761056f945da9`  
		Last Modified: Fri, 09 Dec 2022 06:06:36 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7908f81ea6f9cbbe67af97908251bbe3fcedc00404f51aea9877d58fd2bc203`  
		Last Modified: Fri, 09 Dec 2022 06:06:36 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985e7402c856a98be43526738a98d3219f5597ae049f7b7ef521bec802b01430`  
		Last Modified: Fri, 09 Dec 2022 06:06:42 GMT  
		Size: 135.3 MB (135276309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:b7c68e2d094f8ed986316fd719c849d16726c2e078fc7c4e6d10e9dc6d7910ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:8f41afc36817b80873ddbf439195bea8306e1d07b9b15cacc7fe3db63c2f6ba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365280701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a1c54200cadb166a13ca5ff49aad8675a505e2f1ec9eab62adea2263a3394`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:54:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:54:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Wed, 21 Dec 2022 11:54:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:54:28 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Wed, 21 Dec 2022 11:54:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:54:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:54:45 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:54:45 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:54:45 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:54:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:54:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea29a925d6d469af60c170c243ae635b2b44f24f708f8ec26d1ceb8fed83b0`  
		Last Modified: Wed, 21 Dec 2022 11:57:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f25799ab7bd6bd9cce3191f98c20fd7bf1d2143f5976cb9fb813f0ba6f80d`  
		Last Modified: Wed, 21 Dec 2022 11:57:56 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d939b3dc311402c3d2bc29edecea34d5d395e87dc626eec65a2194060193a7b3`  
		Last Modified: Wed, 21 Dec 2022 11:58:03 GMT  
		Size: 135.4 MB (135417178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0b8463a7237f648a135381fe814b747fe90beb9b9f159190ccef082b54bc90ec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360552059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4251b853f2a32a447e7657725de68a4c57b42c13309b55cb974ae4e3ebb00003`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 05:04:05 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Fri, 09 Dec 2022 06:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:05:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Fri, 09 Dec 2022 06:05:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:05:02 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 09 Dec 2022 06:05:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:05:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:05:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:05:12 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:05:12 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:05:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:05:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44bbb0380eb6b5cd1051003f5ce31baf496a9113c5e9927f76bcf714c433145`  
		Last Modified: Fri, 09 Dec 2022 05:18:38 GMT  
		Size: 195.2 MB (195203372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddf1b63ee1021fb4d42c559adb38c1d219199899fd8bcf7038761056f945da9`  
		Last Modified: Fri, 09 Dec 2022 06:06:36 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7908f81ea6f9cbbe67af97908251bbe3fcedc00404f51aea9877d58fd2bc203`  
		Last Modified: Fri, 09 Dec 2022 06:06:36 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985e7402c856a98be43526738a98d3219f5597ae049f7b7ef521bec802b01430`  
		Last Modified: Fri, 09 Dec 2022 06:06:42 GMT  
		Size: 135.3 MB (135276309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:ae2194998db9b5d0acc6aed68a3623b44349aa11d03fff4f02efe5c2fdf15fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:780ad48f5075d7b7c70ada3136718833de5e96605e6f5b32bd165b5ad1d0186a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 MB (460469022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49206f655eac6ec88c6806411188d042da40b17f6d1e875e64e94f22775061f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:54:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54531e7d1a7c381138fa527e1f5f22482d1687c04f237532b24fe42a1ef57491 NEO4J_TARBALL=neo4j-enterprise-4.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:54:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
# Wed, 21 Dec 2022 11:54:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:54:52 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Wed, 21 Dec 2022 11:55:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:55:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:55:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:55:14 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:55:14 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:55:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:55:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cf4cad3f428fd30dfa21e0e6e2e55da57f9aea079fba9297a44df694d1e850`  
		Last Modified: Wed, 21 Dec 2022 11:58:16 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6ab95ceef525136484b0a3ad6ae203e1fa9363f4ff05a587165721a7a36fb1`  
		Last Modified: Wed, 21 Dec 2022 11:58:16 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa80e55e3e3ede252c4a9f0b6dd729bedf037c50d110b2cb55f5a3aa26b8d0f5`  
		Last Modified: Wed, 21 Dec 2022 11:58:27 GMT  
		Size: 230.6 MB (230605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fe035722b31508838c2e45343c6f202bb38cdfb780eff5c738653ca1b075c1a6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455740012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbfff103274fe27f4f165a6823c2081bfaae5d2e6d802784b4fd90e1098e7de`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 05:04:05 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Fri, 09 Dec 2022 06:05:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54531e7d1a7c381138fa527e1f5f22482d1687c04f237532b24fe42a1ef57491 NEO4J_TARBALL=neo4j-enterprise-4.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:05:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
# Fri, 09 Dec 2022 06:05:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:05:16 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 09 Dec 2022 06:05:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:05:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:05:29 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:05:30 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:05:30 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:05:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:05:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44bbb0380eb6b5cd1051003f5ce31baf496a9113c5e9927f76bcf714c433145`  
		Last Modified: Fri, 09 Dec 2022 05:18:38 GMT  
		Size: 195.2 MB (195203372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437386a1c9ab0c608339d48a631ea93729e9ea22f147be4c6a8be740ce4a3584`  
		Last Modified: Fri, 09 Dec 2022 06:06:56 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e9611a7805dd1c1f6fd7295bafa8a7c41966fa210925efdf7be27820ccef3a`  
		Last Modified: Fri, 09 Dec 2022 06:06:56 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931de49b35611b3761e9e6485b5454e8e8743f2696cdbfb2574519c638441201`  
		Last Modified: Fri, 09 Dec 2022 06:07:05 GMT  
		Size: 230.5 MB (230464261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.15`

```console
$ docker pull neo4j@sha256:b7c68e2d094f8ed986316fd719c849d16726c2e078fc7c4e6d10e9dc6d7910ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.15` - linux; amd64

```console
$ docker pull neo4j@sha256:8f41afc36817b80873ddbf439195bea8306e1d07b9b15cacc7fe3db63c2f6ba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365280701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a1c54200cadb166a13ca5ff49aad8675a505e2f1ec9eab62adea2263a3394`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:54:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:54:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Wed, 21 Dec 2022 11:54:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:54:28 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Wed, 21 Dec 2022 11:54:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:54:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:54:45 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:54:45 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:54:45 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:54:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:54:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea29a925d6d469af60c170c243ae635b2b44f24f708f8ec26d1ceb8fed83b0`  
		Last Modified: Wed, 21 Dec 2022 11:57:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f25799ab7bd6bd9cce3191f98c20fd7bf1d2143f5976cb9fb813f0ba6f80d`  
		Last Modified: Wed, 21 Dec 2022 11:57:56 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d939b3dc311402c3d2bc29edecea34d5d395e87dc626eec65a2194060193a7b3`  
		Last Modified: Wed, 21 Dec 2022 11:58:03 GMT  
		Size: 135.4 MB (135417178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.15` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0b8463a7237f648a135381fe814b747fe90beb9b9f159190ccef082b54bc90ec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360552059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4251b853f2a32a447e7657725de68a4c57b42c13309b55cb974ae4e3ebb00003`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 05:04:05 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Fri, 09 Dec 2022 06:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:05:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Fri, 09 Dec 2022 06:05:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:05:02 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 09 Dec 2022 06:05:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:05:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:05:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:05:12 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:05:12 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:05:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:05:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44bbb0380eb6b5cd1051003f5ce31baf496a9113c5e9927f76bcf714c433145`  
		Last Modified: Fri, 09 Dec 2022 05:18:38 GMT  
		Size: 195.2 MB (195203372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddf1b63ee1021fb4d42c559adb38c1d219199899fd8bcf7038761056f945da9`  
		Last Modified: Fri, 09 Dec 2022 06:06:36 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7908f81ea6f9cbbe67af97908251bbe3fcedc00404f51aea9877d58fd2bc203`  
		Last Modified: Fri, 09 Dec 2022 06:06:36 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985e7402c856a98be43526738a98d3219f5597ae049f7b7ef521bec802b01430`  
		Last Modified: Fri, 09 Dec 2022 06:06:42 GMT  
		Size: 135.3 MB (135276309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.15-community`

```console
$ docker pull neo4j@sha256:b7c68e2d094f8ed986316fd719c849d16726c2e078fc7c4e6d10e9dc6d7910ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.15-community` - linux; amd64

```console
$ docker pull neo4j@sha256:8f41afc36817b80873ddbf439195bea8306e1d07b9b15cacc7fe3db63c2f6ba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365280701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a1c54200cadb166a13ca5ff49aad8675a505e2f1ec9eab62adea2263a3394`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:54:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:54:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Wed, 21 Dec 2022 11:54:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:54:28 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Wed, 21 Dec 2022 11:54:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:54:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:54:45 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:54:45 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:54:45 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:54:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:54:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea29a925d6d469af60c170c243ae635b2b44f24f708f8ec26d1ceb8fed83b0`  
		Last Modified: Wed, 21 Dec 2022 11:57:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f25799ab7bd6bd9cce3191f98c20fd7bf1d2143f5976cb9fb813f0ba6f80d`  
		Last Modified: Wed, 21 Dec 2022 11:57:56 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d939b3dc311402c3d2bc29edecea34d5d395e87dc626eec65a2194060193a7b3`  
		Last Modified: Wed, 21 Dec 2022 11:58:03 GMT  
		Size: 135.4 MB (135417178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.15-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0b8463a7237f648a135381fe814b747fe90beb9b9f159190ccef082b54bc90ec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360552059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4251b853f2a32a447e7657725de68a4c57b42c13309b55cb974ae4e3ebb00003`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 05:04:05 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Fri, 09 Dec 2022 06:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:05:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Fri, 09 Dec 2022 06:05:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:05:02 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 09 Dec 2022 06:05:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:05:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:05:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:05:12 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:05:12 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:05:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:05:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44bbb0380eb6b5cd1051003f5ce31baf496a9113c5e9927f76bcf714c433145`  
		Last Modified: Fri, 09 Dec 2022 05:18:38 GMT  
		Size: 195.2 MB (195203372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddf1b63ee1021fb4d42c559adb38c1d219199899fd8bcf7038761056f945da9`  
		Last Modified: Fri, 09 Dec 2022 06:06:36 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7908f81ea6f9cbbe67af97908251bbe3fcedc00404f51aea9877d58fd2bc203`  
		Last Modified: Fri, 09 Dec 2022 06:06:36 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985e7402c856a98be43526738a98d3219f5597ae049f7b7ef521bec802b01430`  
		Last Modified: Fri, 09 Dec 2022 06:06:42 GMT  
		Size: 135.3 MB (135276309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.15-enterprise`

```console
$ docker pull neo4j@sha256:ae2194998db9b5d0acc6aed68a3623b44349aa11d03fff4f02efe5c2fdf15fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.15-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:780ad48f5075d7b7c70ada3136718833de5e96605e6f5b32bd165b5ad1d0186a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 MB (460469022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49206f655eac6ec88c6806411188d042da40b17f6d1e875e64e94f22775061f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:54:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54531e7d1a7c381138fa527e1f5f22482d1687c04f237532b24fe42a1ef57491 NEO4J_TARBALL=neo4j-enterprise-4.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:54:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
# Wed, 21 Dec 2022 11:54:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:54:52 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Wed, 21 Dec 2022 11:55:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:55:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:55:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:55:14 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:55:14 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:55:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:55:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cf4cad3f428fd30dfa21e0e6e2e55da57f9aea079fba9297a44df694d1e850`  
		Last Modified: Wed, 21 Dec 2022 11:58:16 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6ab95ceef525136484b0a3ad6ae203e1fa9363f4ff05a587165721a7a36fb1`  
		Last Modified: Wed, 21 Dec 2022 11:58:16 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa80e55e3e3ede252c4a9f0b6dd729bedf037c50d110b2cb55f5a3aa26b8d0f5`  
		Last Modified: Wed, 21 Dec 2022 11:58:27 GMT  
		Size: 230.6 MB (230605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.15-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fe035722b31508838c2e45343c6f202bb38cdfb780eff5c738653ca1b075c1a6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455740012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbfff103274fe27f4f165a6823c2081bfaae5d2e6d802784b4fd90e1098e7de`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 05:04:05 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Fri, 09 Dec 2022 06:05:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54531e7d1a7c381138fa527e1f5f22482d1687c04f237532b24fe42a1ef57491 NEO4J_TARBALL=neo4j-enterprise-4.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:05:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
# Fri, 09 Dec 2022 06:05:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:05:16 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 09 Dec 2022 06:05:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:05:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:05:29 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:05:30 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:05:30 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:05:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:05:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44bbb0380eb6b5cd1051003f5ce31baf496a9113c5e9927f76bcf714c433145`  
		Last Modified: Fri, 09 Dec 2022 05:18:38 GMT  
		Size: 195.2 MB (195203372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437386a1c9ab0c608339d48a631ea93729e9ea22f147be4c6a8be740ce4a3584`  
		Last Modified: Fri, 09 Dec 2022 06:06:56 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e9611a7805dd1c1f6fd7295bafa8a7c41966fa210925efdf7be27820ccef3a`  
		Last Modified: Fri, 09 Dec 2022 06:06:56 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931de49b35611b3761e9e6485b5454e8e8743f2696cdbfb2574519c638441201`  
		Last Modified: Fri, 09 Dec 2022 06:07:05 GMT  
		Size: 230.5 MB (230464261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:e00e7fdb9fc5e6674db8fa27f9f0fc680aff1de7680e63ef9a71e86ec5e357f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:ee4b2d77cf3ffd5e6c4ae831c5bd058d9e2fa41ad0963e76a948b649e60a658c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0471a45f9a41007a1128b3cf918af56567051673f20d397c85b65421abd709b9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:52:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:52:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:52:54 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:07 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:07 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f42abb3f13626627d701ea540016be3c6d3ab0fb8a2f4a495a915d179de7f35`  
		Last Modified: Wed, 21 Dec 2022 11:56:34 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68a0ef87b6ee5b98aedacfa770d3f51a791e062695811554e1fe0b901382ff1`  
		Last Modified: Wed, 21 Dec 2022 11:56:35 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d367d623d9a4c6c38a4d94e3b962694ea2908d3e90023efd5be312715b13851`  
		Last Modified: Wed, 21 Dec 2022 11:56:40 GMT  
		Size: 114.6 MB (114606380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58bce60b97dd2dd98fa89dcdfdd69c719357a558ccd8681e653438995e0350a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335754395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3c3bead319235f58f3ee73115fc52efdcece681b9ad2702e4a7eda54708f3`
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
# Fri, 16 Dec 2022 00:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:45:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:45:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:45:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:45:45 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:45:45 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:45:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:45:45 GMT
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
	-	`sha256:e5571ed58cae932e57ef3bd2ca64315900f8585ee787f92c938c6c7b0b305bd9`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac3bb26b2bf1c39c5fd6c1f881cc86ce31225b6499409c19df707d9a3ae642`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a636e32d56069fc06e62c2b94da87c5034e3b2511f1ae4c02f50a820c3eff831`  
		Last Modified: Fri, 16 Dec 2022 00:46:43 GMT  
		Size: 114.5 MB (114466647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:e00e7fdb9fc5e6674db8fa27f9f0fc680aff1de7680e63ef9a71e86ec5e357f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:ee4b2d77cf3ffd5e6c4ae831c5bd058d9e2fa41ad0963e76a948b649e60a658c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0471a45f9a41007a1128b3cf918af56567051673f20d397c85b65421abd709b9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:52:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:52:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:52:54 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:07 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:07 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f42abb3f13626627d701ea540016be3c6d3ab0fb8a2f4a495a915d179de7f35`  
		Last Modified: Wed, 21 Dec 2022 11:56:34 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68a0ef87b6ee5b98aedacfa770d3f51a791e062695811554e1fe0b901382ff1`  
		Last Modified: Wed, 21 Dec 2022 11:56:35 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d367d623d9a4c6c38a4d94e3b962694ea2908d3e90023efd5be312715b13851`  
		Last Modified: Wed, 21 Dec 2022 11:56:40 GMT  
		Size: 114.6 MB (114606380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58bce60b97dd2dd98fa89dcdfdd69c719357a558ccd8681e653438995e0350a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335754395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3c3bead319235f58f3ee73115fc52efdcece681b9ad2702e4a7eda54708f3`
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
# Fri, 16 Dec 2022 00:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:45:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:45:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:45:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:45:45 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:45:45 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:45:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:45:45 GMT
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
	-	`sha256:e5571ed58cae932e57ef3bd2ca64315900f8585ee787f92c938c6c7b0b305bd9`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac3bb26b2bf1c39c5fd6c1f881cc86ce31225b6499409c19df707d9a3ae642`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a636e32d56069fc06e62c2b94da87c5034e3b2511f1ae4c02f50a820c3eff831`  
		Last Modified: Fri, 16 Dec 2022 00:46:43 GMT  
		Size: 114.5 MB (114466647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:cf7cd061e2652f03969cae5dbd526b3f42aad5cc48eeb0e72214b59a397d0ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7a131ac2f7e36ec5c7c9706bfd61ed750fbbc17eef66f4cac235e50559a175b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434823820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38a82df7b15af6301d7c6d2406cdba86dcba44d33dbf71223619a54b6cb770e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:53:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:53:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:53:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:53:11 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:32 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:32 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347e7e217c6e46c9595d942209e84a509d4992dae0ab8d5efc27db33f79904e3`  
		Last Modified: Wed, 21 Dec 2022 11:56:59 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433b004c6cf9ca86872ab3c9642c7096ec5cdfe7644be507bf520f9e9baf5e3`  
		Last Modified: Wed, 21 Dec 2022 11:56:59 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928be2a6d45d927b589c65bd098514e562bf244f7d041ad56f06785365923f51`  
		Last Modified: Wed, 21 Dec 2022 11:57:10 GMT  
		Size: 211.0 MB (210983441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e0194f242e44418de30c92e5d4aef46136bb475742685952e014554c15af4741
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432129984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e950e8c4d16184c757f0dd278f4351f2595cbcb5a4ccc3603a856c3b369639e`
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
# Fri, 16 Dec 2022 00:45:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:50 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:46:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:46:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:46:02 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:46:02 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:46:02 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:46:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:46:02 GMT
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
	-	`sha256:e8071d0dc16b80b644cd90edfe37ed45bf4230b603813370223b3c0dfd146be5`  
		Last Modified: Fri, 16 Dec 2022 00:47:02 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f17ac8c8583fd5ebe569eecdc368fe59dcb326161e158e20c9744bf3b71e513`  
		Last Modified: Fri, 16 Dec 2022 00:47:02 GMT  
		Size: 8.3 KB (8337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb01de83d5e887c3df94db71062b5e52951a123fa6eed0e22b708fcace816a4`  
		Last Modified: Fri, 16 Dec 2022 00:47:11 GMT  
		Size: 210.8 MB (210842235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.2`

```console
$ docker pull neo4j@sha256:fc4721030f6db684dbeb7da47bb75857cb18ffe9fc70e623f3427200613763d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2` - linux; amd64

```console
$ docker pull neo4j@sha256:7bf4d7484b5a5ad22061313ef5f737640550ff6a68b3b8147e3d4e60e53d2b10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336757432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0760912ebe09142a52df6a0d9e36dc05ca3d3050172422eb4948280999066b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:53:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Wed, 21 Dec 2022 11:53:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:53:39 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Wed, 21 Dec 2022 11:53:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:55 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:55 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ef8ff46c41092fa216c33abc7884906457b1da6dea6fa08caca970cad4f5de`  
		Last Modified: Wed, 21 Dec 2022 11:57:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d964200bd4edc29f7526638202c40049f2aa5d0148638df5b6a3f544f6ef2a`  
		Last Modified: Wed, 21 Dec 2022 11:57:22 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98cf711097de03a4e251b079fe1dd28d944503782cdf3f250d641259a644777`  
		Last Modified: Wed, 21 Dec 2022 11:57:28 GMT  
		Size: 112.9 MB (112917229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:66a86b47786f9ece3d499c8112d71916663da0dd2229f0ccbfb4652f628d2168
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3924171754e99a92127c8f1fafed34be8fc1c81da16500dc3be5e1e37431dde`
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
# Fri, 09 Dec 2022 06:04:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:04:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Fri, 09 Dec 2022 06:04:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:04:23 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Fri, 09 Dec 2022 06:04:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:04:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:04:33 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:04:33 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:04:33 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:04:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:04:33 GMT
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
	-	`sha256:4438ae9db4dc6039bc424a68c980ce15d81123c7217b787cc8f1555cd3ee9900`  
		Last Modified: Fri, 09 Dec 2022 06:05:52 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadab086183024cd7601e4f6521c502a33abac72a24df0c10394c3ada6195c0`  
		Last Modified: Fri, 09 Dec 2022 06:05:52 GMT  
		Size: 8.2 KB (8163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391d1c9dfc0b8451b1db0a957e1c30e888bd8adb73a3d600c11e261847e08805`  
		Last Modified: Fri, 09 Dec 2022 06:05:57 GMT  
		Size: 112.8 MB (112775836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.2-enterprise`

```console
$ docker pull neo4j@sha256:40cbfc27eacca66b1120f0d99ad6a734704ca272b893f8891797479a39fa1d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:40588dce444e1f992dc51a6962305e2aabb4baf8aadee5ee53af523b1b3d1d0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432853055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28b614d0c7bbbbfb4e6bc226287c0482213ec2272a07dbec425cfe57034346e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:53:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:53:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Wed, 21 Dec 2022 11:53:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:53:59 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Wed, 21 Dec 2022 11:54:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:54:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:54:20 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:54:20 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:54:20 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:54:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:54:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cbbe39e94b346b4abfd4ffd4a7f1373759270ad4f2f2a2dcf9c61969369530`  
		Last Modified: Wed, 21 Dec 2022 11:57:38 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d45d3544120ac6905fa729d41594b8249c6a9b6e3932366c0cd0aef0596117`  
		Last Modified: Wed, 21 Dec 2022 11:57:38 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af02442ed4759528239612e158fcffa760c3c476523cc329ae674c7e9600ec6e`  
		Last Modified: Wed, 21 Dec 2022 11:57:48 GMT  
		Size: 209.0 MB (209012850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2-enterprise` - linux; arm64 variant v8

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

## `neo4j:5.2.0`

```console
$ docker pull neo4j@sha256:fc4721030f6db684dbeb7da47bb75857cb18ffe9fc70e623f3427200613763d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2.0` - linux; amd64

```console
$ docker pull neo4j@sha256:7bf4d7484b5a5ad22061313ef5f737640550ff6a68b3b8147e3d4e60e53d2b10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336757432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0760912ebe09142a52df6a0d9e36dc05ca3d3050172422eb4948280999066b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:53:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Wed, 21 Dec 2022 11:53:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:53:39 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Wed, 21 Dec 2022 11:53:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:55 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:55 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ef8ff46c41092fa216c33abc7884906457b1da6dea6fa08caca970cad4f5de`  
		Last Modified: Wed, 21 Dec 2022 11:57:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d964200bd4edc29f7526638202c40049f2aa5d0148638df5b6a3f544f6ef2a`  
		Last Modified: Wed, 21 Dec 2022 11:57:22 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98cf711097de03a4e251b079fe1dd28d944503782cdf3f250d641259a644777`  
		Last Modified: Wed, 21 Dec 2022 11:57:28 GMT  
		Size: 112.9 MB (112917229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:66a86b47786f9ece3d499c8112d71916663da0dd2229f0ccbfb4652f628d2168
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3924171754e99a92127c8f1fafed34be8fc1c81da16500dc3be5e1e37431dde`
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
# Fri, 09 Dec 2022 06:04:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:04:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Fri, 09 Dec 2022 06:04:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:04:23 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Fri, 09 Dec 2022 06:04:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:04:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:04:33 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:04:33 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:04:33 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:04:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:04:33 GMT
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
	-	`sha256:4438ae9db4dc6039bc424a68c980ce15d81123c7217b787cc8f1555cd3ee9900`  
		Last Modified: Fri, 09 Dec 2022 06:05:52 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadab086183024cd7601e4f6521c502a33abac72a24df0c10394c3ada6195c0`  
		Last Modified: Fri, 09 Dec 2022 06:05:52 GMT  
		Size: 8.2 KB (8163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391d1c9dfc0b8451b1db0a957e1c30e888bd8adb73a3d600c11e261847e08805`  
		Last Modified: Fri, 09 Dec 2022 06:05:57 GMT  
		Size: 112.8 MB (112775836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.2.0-community`

```console
$ docker pull neo4j@sha256:fc4721030f6db684dbeb7da47bb75857cb18ffe9fc70e623f3427200613763d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:7bf4d7484b5a5ad22061313ef5f737640550ff6a68b3b8147e3d4e60e53d2b10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336757432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0760912ebe09142a52df6a0d9e36dc05ca3d3050172422eb4948280999066b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:53:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Wed, 21 Dec 2022 11:53:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:53:39 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Wed, 21 Dec 2022 11:53:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:55 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:55 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ef8ff46c41092fa216c33abc7884906457b1da6dea6fa08caca970cad4f5de`  
		Last Modified: Wed, 21 Dec 2022 11:57:22 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d964200bd4edc29f7526638202c40049f2aa5d0148638df5b6a3f544f6ef2a`  
		Last Modified: Wed, 21 Dec 2022 11:57:22 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98cf711097de03a4e251b079fe1dd28d944503782cdf3f250d641259a644777`  
		Last Modified: Wed, 21 Dec 2022 11:57:28 GMT  
		Size: 112.9 MB (112917229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:66a86b47786f9ece3d499c8112d71916663da0dd2229f0ccbfb4652f628d2168
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3924171754e99a92127c8f1fafed34be8fc1c81da16500dc3be5e1e37431dde`
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
# Fri, 09 Dec 2022 06:04:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 09 Dec 2022 06:04:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Fri, 09 Dec 2022 06:04:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 09 Dec 2022 06:04:23 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Fri, 09 Dec 2022 06:04:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 06:04:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 06:04:33 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2022 06:04:33 GMT
VOLUME [/data /logs]
# Fri, 09 Dec 2022 06:04:33 GMT
EXPOSE 7473 7474 7687
# Fri, 09 Dec 2022 06:04:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:04:33 GMT
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
	-	`sha256:4438ae9db4dc6039bc424a68c980ce15d81123c7217b787cc8f1555cd3ee9900`  
		Last Modified: Fri, 09 Dec 2022 06:05:52 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadab086183024cd7601e4f6521c502a33abac72a24df0c10394c3ada6195c0`  
		Last Modified: Fri, 09 Dec 2022 06:05:52 GMT  
		Size: 8.2 KB (8163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391d1c9dfc0b8451b1db0a957e1c30e888bd8adb73a3d600c11e261847e08805`  
		Last Modified: Fri, 09 Dec 2022 06:05:57 GMT  
		Size: 112.8 MB (112775836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.2.0-enterprise`

```console
$ docker pull neo4j@sha256:40cbfc27eacca66b1120f0d99ad6a734704ca272b893f8891797479a39fa1d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:40588dce444e1f992dc51a6962305e2aabb4baf8aadee5ee53af523b1b3d1d0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432853055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28b614d0c7bbbbfb4e6bc226287c0482213ec2272a07dbec425cfe57034346e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:53:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:53:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Wed, 21 Dec 2022 11:53:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:53:59 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Wed, 21 Dec 2022 11:54:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:54:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:54:20 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:54:20 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:54:20 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:54:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:54:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cbbe39e94b346b4abfd4ffd4a7f1373759270ad4f2f2a2dcf9c61969369530`  
		Last Modified: Wed, 21 Dec 2022 11:57:38 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d45d3544120ac6905fa729d41594b8249c6a9b6e3932366c0cd0aef0596117`  
		Last Modified: Wed, 21 Dec 2022 11:57:38 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af02442ed4759528239612e158fcffa760c3c476523cc329ae674c7e9600ec6e`  
		Last Modified: Wed, 21 Dec 2022 11:57:48 GMT  
		Size: 209.0 MB (209012850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2.0-enterprise` - linux; arm64 variant v8

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

## `neo4j:5.3`

```console
$ docker pull neo4j@sha256:e00e7fdb9fc5e6674db8fa27f9f0fc680aff1de7680e63ef9a71e86ec5e357f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3` - linux; amd64

```console
$ docker pull neo4j@sha256:ee4b2d77cf3ffd5e6c4ae831c5bd058d9e2fa41ad0963e76a948b649e60a658c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0471a45f9a41007a1128b3cf918af56567051673f20d397c85b65421abd709b9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:52:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:52:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:52:54 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:07 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:07 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f42abb3f13626627d701ea540016be3c6d3ab0fb8a2f4a495a915d179de7f35`  
		Last Modified: Wed, 21 Dec 2022 11:56:34 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68a0ef87b6ee5b98aedacfa770d3f51a791e062695811554e1fe0b901382ff1`  
		Last Modified: Wed, 21 Dec 2022 11:56:35 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d367d623d9a4c6c38a4d94e3b962694ea2908d3e90023efd5be312715b13851`  
		Last Modified: Wed, 21 Dec 2022 11:56:40 GMT  
		Size: 114.6 MB (114606380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58bce60b97dd2dd98fa89dcdfdd69c719357a558ccd8681e653438995e0350a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335754395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3c3bead319235f58f3ee73115fc52efdcece681b9ad2702e4a7eda54708f3`
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
# Fri, 16 Dec 2022 00:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:45:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:45:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:45:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:45:45 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:45:45 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:45:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:45:45 GMT
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
	-	`sha256:e5571ed58cae932e57ef3bd2ca64315900f8585ee787f92c938c6c7b0b305bd9`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac3bb26b2bf1c39c5fd6c1f881cc86ce31225b6499409c19df707d9a3ae642`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a636e32d56069fc06e62c2b94da87c5034e3b2511f1ae4c02f50a820c3eff831`  
		Last Modified: Fri, 16 Dec 2022 00:46:43 GMT  
		Size: 114.5 MB (114466647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.3-enterprise`

```console
$ docker pull neo4j@sha256:cf7cd061e2652f03969cae5dbd526b3f42aad5cc48eeb0e72214b59a397d0ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7a131ac2f7e36ec5c7c9706bfd61ed750fbbc17eef66f4cac235e50559a175b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434823820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38a82df7b15af6301d7c6d2406cdba86dcba44d33dbf71223619a54b6cb770e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:53:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:53:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:53:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:53:11 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:32 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:32 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347e7e217c6e46c9595d942209e84a509d4992dae0ab8d5efc27db33f79904e3`  
		Last Modified: Wed, 21 Dec 2022 11:56:59 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433b004c6cf9ca86872ab3c9642c7096ec5cdfe7644be507bf520f9e9baf5e3`  
		Last Modified: Wed, 21 Dec 2022 11:56:59 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928be2a6d45d927b589c65bd098514e562bf244f7d041ad56f06785365923f51`  
		Last Modified: Wed, 21 Dec 2022 11:57:10 GMT  
		Size: 211.0 MB (210983441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e0194f242e44418de30c92e5d4aef46136bb475742685952e014554c15af4741
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432129984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e950e8c4d16184c757f0dd278f4351f2595cbcb5a4ccc3603a856c3b369639e`
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
# Fri, 16 Dec 2022 00:45:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:50 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:46:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:46:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:46:02 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:46:02 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:46:02 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:46:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:46:02 GMT
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
	-	`sha256:e8071d0dc16b80b644cd90edfe37ed45bf4230b603813370223b3c0dfd146be5`  
		Last Modified: Fri, 16 Dec 2022 00:47:02 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f17ac8c8583fd5ebe569eecdc368fe59dcb326161e158e20c9744bf3b71e513`  
		Last Modified: Fri, 16 Dec 2022 00:47:02 GMT  
		Size: 8.3 KB (8337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb01de83d5e887c3df94db71062b5e52951a123fa6eed0e22b708fcace816a4`  
		Last Modified: Fri, 16 Dec 2022 00:47:11 GMT  
		Size: 210.8 MB (210842235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.3.0`

```console
$ docker pull neo4j@sha256:e00e7fdb9fc5e6674db8fa27f9f0fc680aff1de7680e63ef9a71e86ec5e357f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3.0` - linux; amd64

```console
$ docker pull neo4j@sha256:ee4b2d77cf3ffd5e6c4ae831c5bd058d9e2fa41ad0963e76a948b649e60a658c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0471a45f9a41007a1128b3cf918af56567051673f20d397c85b65421abd709b9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:52:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:52:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:52:54 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:07 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:07 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f42abb3f13626627d701ea540016be3c6d3ab0fb8a2f4a495a915d179de7f35`  
		Last Modified: Wed, 21 Dec 2022 11:56:34 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68a0ef87b6ee5b98aedacfa770d3f51a791e062695811554e1fe0b901382ff1`  
		Last Modified: Wed, 21 Dec 2022 11:56:35 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d367d623d9a4c6c38a4d94e3b962694ea2908d3e90023efd5be312715b13851`  
		Last Modified: Wed, 21 Dec 2022 11:56:40 GMT  
		Size: 114.6 MB (114606380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58bce60b97dd2dd98fa89dcdfdd69c719357a558ccd8681e653438995e0350a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335754395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3c3bead319235f58f3ee73115fc52efdcece681b9ad2702e4a7eda54708f3`
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
# Fri, 16 Dec 2022 00:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:45:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:45:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:45:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:45:45 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:45:45 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:45:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:45:45 GMT
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
	-	`sha256:e5571ed58cae932e57ef3bd2ca64315900f8585ee787f92c938c6c7b0b305bd9`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac3bb26b2bf1c39c5fd6c1f881cc86ce31225b6499409c19df707d9a3ae642`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a636e32d56069fc06e62c2b94da87c5034e3b2511f1ae4c02f50a820c3eff831`  
		Last Modified: Fri, 16 Dec 2022 00:46:43 GMT  
		Size: 114.5 MB (114466647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.3.0-community`

```console
$ docker pull neo4j@sha256:e00e7fdb9fc5e6674db8fa27f9f0fc680aff1de7680e63ef9a71e86ec5e357f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:ee4b2d77cf3ffd5e6c4ae831c5bd058d9e2fa41ad0963e76a948b649e60a658c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0471a45f9a41007a1128b3cf918af56567051673f20d397c85b65421abd709b9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:52:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:52:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:52:54 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:07 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:07 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f42abb3f13626627d701ea540016be3c6d3ab0fb8a2f4a495a915d179de7f35`  
		Last Modified: Wed, 21 Dec 2022 11:56:34 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68a0ef87b6ee5b98aedacfa770d3f51a791e062695811554e1fe0b901382ff1`  
		Last Modified: Wed, 21 Dec 2022 11:56:35 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d367d623d9a4c6c38a4d94e3b962694ea2908d3e90023efd5be312715b13851`  
		Last Modified: Wed, 21 Dec 2022 11:56:40 GMT  
		Size: 114.6 MB (114606380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58bce60b97dd2dd98fa89dcdfdd69c719357a558ccd8681e653438995e0350a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335754395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3c3bead319235f58f3ee73115fc52efdcece681b9ad2702e4a7eda54708f3`
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
# Fri, 16 Dec 2022 00:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:45:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:45:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:45:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:45:45 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:45:45 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:45:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:45:45 GMT
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
	-	`sha256:e5571ed58cae932e57ef3bd2ca64315900f8585ee787f92c938c6c7b0b305bd9`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac3bb26b2bf1c39c5fd6c1f881cc86ce31225b6499409c19df707d9a3ae642`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a636e32d56069fc06e62c2b94da87c5034e3b2511f1ae4c02f50a820c3eff831`  
		Last Modified: Fri, 16 Dec 2022 00:46:43 GMT  
		Size: 114.5 MB (114466647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.3.0-enterprise`

```console
$ docker pull neo4j@sha256:cf7cd061e2652f03969cae5dbd526b3f42aad5cc48eeb0e72214b59a397d0ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7a131ac2f7e36ec5c7c9706bfd61ed750fbbc17eef66f4cac235e50559a175b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434823820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38a82df7b15af6301d7c6d2406cdba86dcba44d33dbf71223619a54b6cb770e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:53:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:53:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:53:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:53:11 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:32 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:32 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347e7e217c6e46c9595d942209e84a509d4992dae0ab8d5efc27db33f79904e3`  
		Last Modified: Wed, 21 Dec 2022 11:56:59 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433b004c6cf9ca86872ab3c9642c7096ec5cdfe7644be507bf520f9e9baf5e3`  
		Last Modified: Wed, 21 Dec 2022 11:56:59 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928be2a6d45d927b589c65bd098514e562bf244f7d041ad56f06785365923f51`  
		Last Modified: Wed, 21 Dec 2022 11:57:10 GMT  
		Size: 211.0 MB (210983441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e0194f242e44418de30c92e5d4aef46136bb475742685952e014554c15af4741
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432129984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e950e8c4d16184c757f0dd278f4351f2595cbcb5a4ccc3603a856c3b369639e`
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
# Fri, 16 Dec 2022 00:45:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:50 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:46:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:46:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:46:02 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:46:02 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:46:02 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:46:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:46:02 GMT
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
	-	`sha256:e8071d0dc16b80b644cd90edfe37ed45bf4230b603813370223b3c0dfd146be5`  
		Last Modified: Fri, 16 Dec 2022 00:47:02 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f17ac8c8583fd5ebe569eecdc368fe59dcb326161e158e20c9744bf3b71e513`  
		Last Modified: Fri, 16 Dec 2022 00:47:02 GMT  
		Size: 8.3 KB (8337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb01de83d5e887c3df94db71062b5e52951a123fa6eed0e22b708fcace816a4`  
		Last Modified: Fri, 16 Dec 2022 00:47:11 GMT  
		Size: 210.8 MB (210842235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:e00e7fdb9fc5e6674db8fa27f9f0fc680aff1de7680e63ef9a71e86ec5e357f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:ee4b2d77cf3ffd5e6c4ae831c5bd058d9e2fa41ad0963e76a948b649e60a658c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0471a45f9a41007a1128b3cf918af56567051673f20d397c85b65421abd709b9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:52:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:52:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:52:54 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:07 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:07 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f42abb3f13626627d701ea540016be3c6d3ab0fb8a2f4a495a915d179de7f35`  
		Last Modified: Wed, 21 Dec 2022 11:56:34 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68a0ef87b6ee5b98aedacfa770d3f51a791e062695811554e1fe0b901382ff1`  
		Last Modified: Wed, 21 Dec 2022 11:56:35 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d367d623d9a4c6c38a4d94e3b962694ea2908d3e90023efd5be312715b13851`  
		Last Modified: Wed, 21 Dec 2022 11:56:40 GMT  
		Size: 114.6 MB (114606380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58bce60b97dd2dd98fa89dcdfdd69c719357a558ccd8681e653438995e0350a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335754395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3c3bead319235f58f3ee73115fc52efdcece681b9ad2702e4a7eda54708f3`
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
# Fri, 16 Dec 2022 00:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:45:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:45:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:45:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:45:45 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:45:45 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:45:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:45:45 GMT
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
	-	`sha256:e5571ed58cae932e57ef3bd2ca64315900f8585ee787f92c938c6c7b0b305bd9`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac3bb26b2bf1c39c5fd6c1f881cc86ce31225b6499409c19df707d9a3ae642`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a636e32d56069fc06e62c2b94da87c5034e3b2511f1ae4c02f50a820c3eff831`  
		Last Modified: Fri, 16 Dec 2022 00:46:43 GMT  
		Size: 114.5 MB (114466647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:cf7cd061e2652f03969cae5dbd526b3f42aad5cc48eeb0e72214b59a397d0ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7a131ac2f7e36ec5c7c9706bfd61ed750fbbc17eef66f4cac235e50559a175b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434823820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38a82df7b15af6301d7c6d2406cdba86dcba44d33dbf71223619a54b6cb770e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:53:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:53:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:53:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:53:11 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:32 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:32 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347e7e217c6e46c9595d942209e84a509d4992dae0ab8d5efc27db33f79904e3`  
		Last Modified: Wed, 21 Dec 2022 11:56:59 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433b004c6cf9ca86872ab3c9642c7096ec5cdfe7644be507bf520f9e9baf5e3`  
		Last Modified: Wed, 21 Dec 2022 11:56:59 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928be2a6d45d927b589c65bd098514e562bf244f7d041ad56f06785365923f51`  
		Last Modified: Wed, 21 Dec 2022 11:57:10 GMT  
		Size: 211.0 MB (210983441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e0194f242e44418de30c92e5d4aef46136bb475742685952e014554c15af4741
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432129984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e950e8c4d16184c757f0dd278f4351f2595cbcb5a4ccc3603a856c3b369639e`
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
# Fri, 16 Dec 2022 00:45:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:50 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:46:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:46:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:46:02 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:46:02 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:46:02 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:46:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:46:02 GMT
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
	-	`sha256:e8071d0dc16b80b644cd90edfe37ed45bf4230b603813370223b3c0dfd146be5`  
		Last Modified: Fri, 16 Dec 2022 00:47:02 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f17ac8c8583fd5ebe569eecdc368fe59dcb326161e158e20c9744bf3b71e513`  
		Last Modified: Fri, 16 Dec 2022 00:47:02 GMT  
		Size: 8.3 KB (8337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb01de83d5e887c3df94db71062b5e52951a123fa6eed0e22b708fcace816a4`  
		Last Modified: Fri, 16 Dec 2022 00:47:11 GMT  
		Size: 210.8 MB (210842235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:e00e7fdb9fc5e6674db8fa27f9f0fc680aff1de7680e63ef9a71e86ec5e357f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:ee4b2d77cf3ffd5e6c4ae831c5bd058d9e2fa41ad0963e76a948b649e60a658c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0471a45f9a41007a1128b3cf918af56567051673f20d397c85b65421abd709b9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:57:05 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 11:52:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 21 Dec 2022 11:52:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 21 Dec 2022 11:52:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 21 Dec 2022 11:52:54 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 21 Dec 2022 11:53:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:53:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 11:53:07 GMT
WORKDIR /var/lib/neo4j
# Wed, 21 Dec 2022 11:53:07 GMT
VOLUME [/data /logs]
# Wed, 21 Dec 2022 11:53:07 GMT
EXPOSE 7473 7474 7687
# Wed, 21 Dec 2022 11:53:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 11:53:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d6f042d4c187dc5ef35678240ad79b89963342d31898de3665a87a1568323`  
		Last Modified: Wed, 21 Dec 2022 02:09:14 GMT  
		Size: 192.4 MB (192431237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f42abb3f13626627d701ea540016be3c6d3ab0fb8a2f4a495a915d179de7f35`  
		Last Modified: Wed, 21 Dec 2022 11:56:34 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68a0ef87b6ee5b98aedacfa770d3f51a791e062695811554e1fe0b901382ff1`  
		Last Modified: Wed, 21 Dec 2022 11:56:35 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d367d623d9a4c6c38a4d94e3b962694ea2908d3e90023efd5be312715b13851`  
		Last Modified: Wed, 21 Dec 2022 11:56:40 GMT  
		Size: 114.6 MB (114606380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58bce60b97dd2dd98fa89dcdfdd69c719357a558ccd8681e653438995e0350a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335754395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3c3bead319235f58f3ee73115fc52efdcece681b9ad2702e4a7eda54708f3`
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
# Fri, 16 Dec 2022 00:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Fri, 16 Dec 2022 00:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Dec 2022 00:45:35 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Fri, 16 Dec 2022 00:45:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2022 00:45:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Dec 2022 00:45:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Dec 2022 00:45:45 GMT
VOLUME [/data /logs]
# Fri, 16 Dec 2022 00:45:45 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Dec 2022 00:45:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Dec 2022 00:45:45 GMT
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
	-	`sha256:e5571ed58cae932e57ef3bd2ca64315900f8585ee787f92c938c6c7b0b305bd9`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac3bb26b2bf1c39c5fd6c1f881cc86ce31225b6499409c19df707d9a3ae642`  
		Last Modified: Fri, 16 Dec 2022 00:46:38 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a636e32d56069fc06e62c2b94da87c5034e3b2511f1ae4c02f50a820c3eff831`  
		Last Modified: Fri, 16 Dec 2022 00:46:43 GMT  
		Size: 114.5 MB (114466647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
